## 一、环境：官方脚本在 Windows 上不可用，需自建 venv

`<plugin_root>/scripts/wb/local/setup-html-to-docx.sh` 有两处 Windows 不兼容：

1. 它校验解释器 `$VENV_DIR/bin/python`，而 Windows 上 `uv venv` 产出的是 `Scripts/python.exe` → 每跑一次就 `rm -rf` 重建，随后必然失败。
2. 未装 uv 时会 `curl https://astral.sh/uv/install.sh`（常超时/被拦）。

因此直接自建。**注意**：不要在 `<plugin_root>/skills/html-to-docx/scripts/` 下建 `.venv`（跨机器 shebang 失效）。

```powershell
# 1) 用托管 Python 建隔离 venv（远离 plugin 目录）
$py   = "$env:USERPROFILE\.workbuddy\binaries\python\versions\3.13.12\python.exe"
$venv = "$env:USERPROFILE\.workbuddy\binaries\python\envs\html-to-docx"
& $py -m venv $venv

# 2) 装依赖：强制仅 wheel，避免 lxml 源码构建失败
$req = "<plugin_root>\skills\html-to-docx\scripts\requirements.txt"
& "$venv\Scripts\python.exe" -m pip install --only-binary=:all: --disable-pip-version-check -q -r $req
```

**依赖的模块名坑**：`requirements.txt` 里的 `html-for-docx` 1.x，其**导入名是 `html4docx`**（不是 `htmldocx`）。官方 setup 脚本的冒烟测试写的是 `import htmldocx`，会误报失败——实际可用。自检请用：

```powershell
& "$venv\Scripts\python.exe" -c "import docx, html4docx, bs4, lxml, httpx, PIL, click; print('OK')"
```

