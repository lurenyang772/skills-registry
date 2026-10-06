# WorkBuddy Skills 社区共享仓

一套在真实研究工作中长期迭代出来的 AI Agent 技能（Skills）知识条目库。
**共享的最小单位是「知识条目」而不是整个 skill 文件**——每个 `.md` 文件就是一条
可独立取用、独立改良、独立回传的方法论或实战经验。

English: A community registry of battle-tested AI-agent skill knowledge entries.
Each markdown file under `registry/<skill-name>/` is a self-contained, reusable
entry. Fork, improve an entry, and send a PR to give back.

## 目录结构

```
registry/<skill名>/<条目>.md   已授权发布的知识条目（本仓唯一内容）
README_社区协议.md             共享与回传规则
LICENSE                        MIT
```

## 怎么用

1. 按主题浏览 `registry/`，找到需要的条目；
2. 把条目内容并入你自己 skill 的 `SKILL.md`（或直接使用 WorkBuddy / qclaw /
   OpenClaw 等支持 SKILL.md 的 Agent 平台，参考条目所属主题自建 skill）；
3. 条目是方法论与实战教训（含大量已验证的坑），不含任何私有数据、路径、凭据。

## 怎么回传改良版（自愿）

如果你在使用中改进了某条条目——修正了过时结论、补了新坑、提炼了更好的流程：

1. Fork 本仓；
2. 直接修改 `registry/<skill名>/` 下对应的条目文件（**一条 PR 改一条目**，
   便于 review；新条目请放入对应 skill 目录或提议新目录）；
3. 提 Pull Request，说明改良点与验证场景；
4. 合并后你的改良会进入主线，并同步回原始迭代环境继续演进。

回传全凭自愿——直接拿去用、不回传也完全欢迎。

## 内容边界

- 本仓所有内容发布前经过多道隐私与安全闸门（机器扫描 + 人工复核），
  不含个人身份信息、内部路径、凭据或任何第三方受限来源；
- 主题以海外宏观/市场/公司研究方法论、Agent 工作流、文档工具链为主；
- 若发现任何不当内容，请开 Issue，会第一时间核实下架。

## License

MIT（见 LICENSE）。条目可自由使用、修改、再分发，保留出处即可。
