# Enterprise decision record format

Use this format when creating or updating an enterprise decision asset.

## Decision file

```markdown
---
record_type: enterprise-decision
decision_id: D0001
decision_date: YYYY-MM-DD
status: proposed | active | completed | superseded | reversed
owner: 姓名或角色 | 待确认
confidentiality: internal | restricted | shareable
review_date: YYYY-MM-DD | null
---

# 决策标题

## 一句话决策

明确写出选择了什么，不把背景或愿望当作决策。

## 当时背景

- 已确认事实：
- 约束条件：
- 需要解决的问题：

## 决策依据

- 用户明确说明的理由：
- AI 归纳（如有，须标记）：

## 备选方案与取舍

- 考虑过的方案：
- 放弃了什么：
- 为什么接受当前代价：

## 假设与风险

- 待验证假设：
- 已知风险：
- 停止或调整条件：

## 行动与验证

- 下一步：
- 负责人：
- 截止或触发条件：
- 判断有效的证据：

## 结果时间线

- YYYY-MM-DD：新增事实、执行动作或结果；说明其来源。

## 复盘

- 结果是否符合预期：待验证
- 哪些判断被证实：待验证
- 哪些判断需要修正：待验证
- 可复用原则：待验证

## 关联决策

- 无；或使用相对链接指向相关记录。
```

Only retain fields that remain meaningful, but never omit the one-sentence decision, context, rationale, next action, and review trigger. Use `待确认` rather than guessing.

## Index

Use `企业决策资产/INDEX.md` as the canonical lookup entry. Keep records newest first.

```markdown
# 企业决策资产索引

> 记录管理层的真实选择、依据、取舍、行动与结果。AI 归纳不等于公司正式决定。

| ID | 日期 | 决策 | 状态 | 负责人 | 下次复盘 |
|---|---|---|---|---|---|
| D0001 | YYYY-MM-DD | [决策标题](YYYY-MM-DD_决策标题.md) | active | 角色 | YYYY-MM-DD |
```

## Lifecycle

- `proposed`: an option or draft awaiting a decision.
- `active`: chosen and currently being executed or observed.
- `completed`: the intended action and review are finished.
- `superseded`: replaced by a newer decision; link the replacement.
- `reversed`: explicitly withdrawn or rolled back; preserve the reason and date.

Never erase the original context or rationale when the status changes. Append dated evidence and explain the transition.

## Shareable summary

When the user requests a card or external summary, create a separate redacted representation rather than modifying the internal record. It should contain only:

- a generalized decision title;
- the decision type;
- no more than three decision criteria;
- the most important tradeoff;
- one next action;
- a short statement that the content was confirmed by the user.

Do not include names, customer details, financial figures, credentials, contracts, unreleased strategy, or other internal identifiers unless the user explicitly approves each item.
