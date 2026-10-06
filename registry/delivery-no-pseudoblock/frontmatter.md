---
name: delivery-no-pseudoblock
version: 1.0.0
display_name: AI交付前全自动自检技能
display_name_en: AI Pre-Delivery Automated Self-Check
description: 交付前伪阻断 / 缓干闸门（通用行为级纪律）。任何一次向用户交付结果之前（present_files、写最终总结、下结论、状态汇报、向用户提问或征询）必须真加载并实跑本技能，对整条消息（含结尾尾巴）逐项枚举 D1–D12 闸门快照，拦截责任转嫁、半途交付、最优步隐藏、伪阻断提问、尾巴豁免、语言后门、先盖章后干活等把活推回用户或用声明替代实际扫描的缓干形态。无真实加载状态即视为未过闸。触发场景：所有任务交付发送前的强制终检。
description_zh: AI交付前全自动自检技能。任何一次向用户交付结果（present_files、最终总结、结论、状态汇报、提问/征询）之前，必须实际加载并实跑本技能，对整条回复（含结尾）逐项枚举 D1–D12 闸门快照，拦截责任转嫁、半途交付、最优步隐藏、伪阻断提问、尾巴豁免、自主闭环缺失、语言后门、先盖章后干活等把活推回用户或以声明替代实际扫描的形态。无真实加载状态即视为未过闸。适用于所有项目、所有交付形态的发送前强制终检。
description_en: AI pre-delivery automated self-check skill. Before ANY result delivery to the user (present_files, final summary, conclusion, status report, or asking a question), this skill MUST be actually loaded and executed, enumerating the D1-D12 gate snapshot item by item over the ENTIRE message including the tail. It intercepts responsibility-shifting, half-done delivery, hidden-optimal-step deferral, pseudo-blocking questions, tail exemption, lack of autonomous closure, language backdoors, and stamp-before-work patterns that push work back to the user or replace real scanning with mere claims. No real load state means the gate was not passed. Mandatory final check before sending, for all projects and all delivery forms.
agent_created: true
---
