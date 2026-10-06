---
name: verify-before-claim
slug: verify-before-claim
displayName: 完成声明验证
display_name: 完成声明验证
display_name_en: Verify Before Claim
summary: 宣告「改完/部署完」前，用机械判据证明动作真落到实体上，覆盖七类假成功形态（空结果 / 回显 / 退出码 / HTTP / 元数据 / 探测 / 锚）。核心方法：报 PASS 的检查器必须先自证能报 FAIL —— 先跑必然失败的对照再采信 PASS；多通道少数否决。判据库 76 条自带反例；结论三态（已证 / 已证伪 / 无法判定），弃答合法且被鼓励。交付可落证据包（`evidence_pack.py`）供第三方复跑；`env_fingerprint.py` 判环境可否沿用；`candidate_gate.py` 令新判据反例实跑，跑不出 FAIL 不入库。纯只读零依赖，不依赖模型内部状态。
description: 对 agent 的完成声明做落地校验：宣告「改完 / 部署完 / 跑完」之前，证明检查手段本身没骗人。覆盖空结果、成功回显、退出码、HTTP 响应体、元数据、探测手段、断言无锚七类假成功形态，横跨本机文件与脚本、远端服务器与 cron、代码仓库、云端文档接口与推送链路。当用户说「没生效 / 改了没变 / 部署了没用 / 跑了但结果不对 / 返回空 / 还是旧的 / 数据没更新 / 看着跑完了但没效果」，或提到「动作幻觉 / 执行幻觉」（自称做完、实际没生效）时使用；断言本身说不清要验什么（「已检查过」「都改完了」「已是最新」）时也用它；多条验证通道结果不一致、或要判断「多处一致」是否可信时也用它；换了机器 / 换了环境、或要沿用别人采集的证据与结论时也用它。不用于页面渲染类故障（页面打不开 / 转圈 / 白屏 / 数字不对）——那属浏览器侧排障，先取浏览器证据定位；也不用于**事实性 / 忠实性**幻觉的核查（内容有没有编造、摘要是否忠于原文）——那属语义核查。
description_zh: 对 Agent 的完成声明做落地校验：宣告「改完 / 部署完 / 跑完」之前，先证明检查手段本身没骗人。覆盖空结果、成功回显、退出码、HTTP 响应体、元数据、探测手段、断言无锚七类假成功形态，横跨本机文件与脚本、远端服务器与 cron、代码仓库、云端文档接口与推送链路。当用户说「没生效 / 改了没变 / 部署了没用 / 跑了但结果不对 / 返回空 / 还是旧的 / 数据没更新 / 看着跑完了但没效果」，或提到「动作幻觉 / 执行幻觉」（自称做完、实际没生效）时使用。核心方法：报 PASS 的检查器必须先自证能报 FAIL —— 先跑必然失败的对照再采信 PASS；多通道验证要求通道独立性与少数否决。判据库 76 条自带反例，结论按三态输出（已证 / 已证伪 / 无法判定），弃答合法。交付可复跑的证据包与环境指纹，纯只读零依赖。
description_en: Ground-truth verification for agent completion claims - before saying "done", prove the check behind it cannot lie. Covers seven classes of false success (empty results, success echoes, exit codes, HTTP response bodies, metadata, probe artifacts, anchorless assertions) across local files and scripts, remote servers and cron, code repositories, cloud document APIs and push pipelines. Use it when a user says "nothing changed / the deploy did nothing / it ran but the result is wrong / it returned empty", or mentions action hallucination (claimed done, never took effect). Core rule - a checker reporting PASS must first prove it can report FAIL - run a known-failing control before trusting a PASS; multi-channel checks require channel independence and minority veto. Ships 76 criteria each with its own counterexample, tri-state verdicts (proven / disproven / undetermined), a re-runnable evidence pack and an environment fingerprint. Read-only, zero dependency.
version: 0.4.2
license: MIT
author: johnsmithCA-sta
homepage: https://github.com/johnsmithCA-sta/verify-before-claim
agent_created: true
tags:
  - 假成功
  - 静默失败
  - 完成声明验证
  - 阴性对照
  - agent 行为纪律
  - 部署核验
  - 环境自适配
---
