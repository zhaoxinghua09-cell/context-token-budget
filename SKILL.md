---
name: context-token-budget
description: "Guard AI context usage with a fail-closed token budget — stop burning tokens. 用 fail-closed 的 token 预算守护 AI 上下文，防止积分烧光。"
version: 1.0.0
license: MIT
category: 效率
author: SynomosAI (LGD initiative)
platforms: [windows, macos, linux]
tags: [context,token,budget]
slug: context-token-budget
risk_tier: medium
---

# Context Token Budget (上下文预算守护)

> **Estimate tokens, enforce a budget, fail closed before overspend.**
> **估算 token、执行预算、超额前 fail-closed。**
> 理论根基：LGD 三律（有籍·有证·有门禁）

## 功能 / Capabilities
- CJK/English-aware token estimation
- Fail-closed budget enforcement with verdict
- SHA-256 content anchor for reproducibility
- 中英文感知的 token 估算
- fail-closed 预算执行与判定
- SHA-256 内容锚点保证可复现

## 用法 / Usage
```bash
python scripts/budget.py <file-or-text> [--limit N] [--json]
```

## 三律对齐 / LGD alignment
| 律 | 本技能如何满足 |
|---|---|
| 有籍 Registered | frontmatter 完整（name/description/license/version），作者与命名空间明确 |
| 有证 Evidenced | 输出可复现（SHA-256 锚点/结构化 JSON），含验证方式 |
| 有门禁 Gated | 最小权限、fail-closed 退出码、危险操作默认拒绝 |

## 安全边界 / Safety boundary
- 只做静态分析，不自动执行任何外部命令
- 检出风险即 FAIL（fail-closed），由人决策
- 不代用户删除/修改/发布任何内容

## Standard alignment / 标准对齐
- **Agent Skills open standard**: compatible with [agentskills.io](https://agentskills.io) format (SKILL.md + scripts/, frontmatter name/description). Adopted by Claude/Codex and the broader agent ecosystem.
- **AEO**: llms.txt / AGENTS.md friendly (AI-agent discoverable).

## Skill card / 技能卡（对标 NVIDIA Verified Agent Skills）
- **Ownership / 所有权**: SynomosAI initiative — Steven Zhao (ORCID 0009-0001-0512-1237)
- **Dependencies / 依赖**: none (Python 3 stdlib only)
- **Limitations / 限制**: static analysis only; not a substitute for runtime verification
- **Verification status / 验证状态**: self-reported PASS via skill-quality-gate; not a certification or endorsement
- **Security posture / 安全姿态**: no network calls, no destructive operations, fail-closed exit codes

## License & attribution
**分层许可（务必并读；代码许可不覆盖文档与理论文本）**

| 层 | 载体 | 许可 |
|---|---|---|
| 代码 | `scripts/*.py` | **MIT** |
| 文档与理论文本 | 本 `SKILL.md`、`README.md` 及理论表述 | **All rights reserved** |

```
© 2026 赵兴华 / Steven Zhao·China (ORCID 0009-0001-0512-1237). All rights reserved.
理论署名 (attribution) : LGD（Lifecycle Governance Doctrine / 全程治理论）— SynomosAI initiative
名称状态 (name status)  : "SynomosAI" / "MedXpert" — 未申请实体注册、未申请商标注册
生产参考部署 (production reference, self-reported) : MedXpert（非认证、非背书、非监管认可）
引用格式 (cite as)      : 本资产无 DOI
```
（上列为《LGD 对外表述规范》§3.2 统一块，整体复制、未删改；发布/重提前须照最新版本复核。）
