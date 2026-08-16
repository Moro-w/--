---
name: explain-ai-pm-terms
description: "Explain unfamiliar AI product-management, machine-learning, software, data, agent, model, and adjacent business terms in clear Chinese through four dimensions: what it is, why it exists, where it operates, and how it works technically. Use when users ask what a term or acronym means, want a beginner-friendly or product-oriented concept explanation, encounter new vocabulary while learning or working as an AI PM, need to distinguish related terms, or request a causal map or ‘思维链’ to aid understanding."
---

# Explain AI PM Terms

## Goal

Turn an unfamiliar term into a compact mental model that connects definition, need, operating context, and implementation. Default to clear Chinese and retain essential English names or acronyms.

## Workflow

1. Identify the intended term and infer the most likely meaning from the user's context.
2. If the term is ambiguous, briefly state the interpretation being used. Ask a question only when choosing the wrong meaning would substantially change the explanation.
3. Match the depth to the user. Default to an AI PM perspective: explain enough technical detail to support product decisions without assuming engineering expertise.
4. Verify niche, disputed, historical, or rapidly changing claims with authoritative sources when tools are available. Never invent a term's origin; say when the origin is uncertain or merely a naming convention.
5. Explain the term with the four dimensions below.
6. Add an understanding chain only when the concept has multiple causal steps, the user requests one, or it materially improves comprehension.

## Four-Dimension Explanation

Use these headings in this order. Keep each section concise unless the user asks for depth.

### 1. 是什么

- Give the Chinese name, original English term, and full form of any acronym.
- Define the term precisely in plain language.
- Explain its origin or naming background only when known and useful.
- End with a one-sentence summary beginning with `一句话：`.
- State what the concept is not when it is commonly confused with a neighboring term.

### 2. 为什么

- Name the user, product, or engineering need it addresses.
- Describe the pain or limitation that existed without it.
- Explain the value it creates and, when relevant, the cost or tradeoff it introduces.
- Avoid saying only that it “improves efficiency”; specify what becomes faster, cheaper, safer, more accurate, or more controllable.

### 3. 在什么场景运作

- Place the term in a recognizable product or technical workflow.
- Identify the key actors or components, typical input, main action, and output.
- Give one short concrete example relevant to AI products.
- Mention where it sits in the stack or process when helpful, such as data layer, model layer, orchestration layer, application layer, evaluation, or operations.

### 4. 怎么做

- Explain the implementation from product flow to technical mechanism.
- Prefer a small sequence such as `输入 → 处理 → 输出`.
- Name the core components, data flow, algorithms, protocols, or infrastructure only when they aid understanding.
- Distinguish a conceptual pattern from a specific vendor, framework, or implementation.
- End with the main limitation, failure mode, or product decision point when relevant.

## Understanding Chain

Label this optional section `理解链（辅助理解）`, not “模型内部思维链”. Provide a concise, inspectable causal summary rather than private chain-of-thought.

Use three to six short nodes:

`现有问题 → 产生需求 → 引入机制 → 系统行为变化 → 用户或业务结果`

Omit the chain when it would merely repeat the four sections. If the user explicitly asks for a “思维链”, provide this causal map and, if useful, a compact analogy.

## Explanation Rules

- Lead with plain language; introduce jargon only after establishing the intuition.
- Use analogies as aids, not definitions. Label where an analogy stops being accurate when that boundary matters.
- Separate stable facts from interpretation or inference.
- Do not fabricate precise dates, inventors, acronym expansions, or technical mechanisms.
- Explain relationships between easily confused terms with a compact comparison only when useful.
- For multiple terms, explain each briefly, then show how they connect in one shared workflow.
- Cite authoritative sources near claims when web research was needed; do not add sources merely for decoration.
- Avoid unnecessary equations and code. Include them only when the user asks or when they are essential to the mechanism.

## Default Output Template

```markdown
## [术语]（English term / acronym）

### 1. 是什么
[定义、词义或由来]

一句话：[最短可复述定义]

### 2. 为什么
[需求、原有问题、价值与必要取舍]

### 3. 在什么场景运作
[参与者/组件、输入、动作、输出、AI 产品例子]

### 4. 怎么做
[产品流程与技术机制；必要时使用 输入 → 处理 → 输出]

### 理解链（辅助理解）
[仅在必要时出现：问题 → 需求 → 机制 → 结果]
```

Do not force every bullet into the answer. Preserve the four headings, then choose only the details that help the user form a correct mental model.
