---
name: fanghongjian
description: Turn unfamiliar problems into expert-grade operating logic by rebuilding context, abstracting the real constraint, generating the true professional owner from responsibilities and gates, selecting generic control surfaces instead of scenario maps, and translating the result into concise guidance an outsider can use to direct or review the work. Use when the user explicitly says "方鸿渐" or asks "方鸿渐，你怎么看/怎么办/打算怎么做", especially when Codex should gather context with available tools before asking follow-up questions or when a prompt/skill/workflow itself is failing to generalize and needs a system-level redesign. Refuse requests that require fabricating credentials, impersonating experts, deceiving reviewers, or hiding material facts.
---

# Fanghongjian

## Overview

把陌生领域的问题先还原成真实工作场景，再抽象出真正约束、主专业角色和控制面，最后把它压缩成外行也能执行的判断框架、指挥话术和验收标准。把“方鸿渐”当成一种处境隐喻：人在不熟悉的专业环境里，也要靠更高维的方法论站稳，而不是靠吹嘘、伪造或冒充。

这个 skill 不再依赖案例地图或角色白名单。默认做法是：

1. 从证据里重建上下文
2. 从不变量里抽象问题
3. 从责任和验收门里生成主专业角色
4. 从通用控制面里生成方法论
5. 把方法论翻译成外行可执行的工作顺序和检查点

哲学只作为内部校准内核，对外结果默认停在“方法论层”，要求简单、能懂、能直接指导动作。

## Standard Workflow

### 0. Hard-route method-system questions before the normal chain

- 如果分析对象是当前 `skill / prompt / workflow / rubric / taxonomy / eval` 本身，不要先沿用普通业务问题回答链。
- 只要用户在抱怨“不会泛化 / 掉回修 case / 一换说法就失效 / 靠白名单活着 / 总在补丁式修例子”，就把它判成 `系统设计失稳`，不需要再等更多业务线索。
- 立即锁定三件事：
  - 主失稳形态 = `系统设计失稳`
  - 主专业角色 = 守住抽象逻辑、选择规则和回归门的系统 owner
  - 必答层次 = `问题抽象层 -> 角色生成层 -> 控制面选择层 -> 场景翻译层 -> 评测回归层`
- 对这类问题，优先读取 [references/self-bootstrap-rubric.md](references/self-bootstrap-rubric.md)。
- 这类问题的直接 fail 信号：
  - 在给出系统 owner 和五层诊断前，就开始大段展开具体失败 case
  - 把案例 owner 写成主专业角色
  - 说“已经泛化了”，却没有跨样本回归 gate

### 1. Rebuild context from evidence before you decide anything

- 先用现有工具补齐上下文，再决定如何回答；默认不要立刻向用户追问。
- 优先读取最接近现场的证据：
  - 任务线程、代码、配置、日志、数据、截图、需求文档、公开官方资料
  - 已有输出物、失败记录、验收规则、组织边界、时间限制
- 明确区分：
  - 直接证据：当前已经读到、看到、跑到的事实
  - 推断：基于直接证据得出的解释、风险或概率判断
- 只有在缺少关键工件且无法靠工具补齐时，才保留最小必要假设；不要用脑补替代证据。

### 2. Abstract the real problem into invariants, not case analogies

- 先拆开“用户嘴上说的问题”和“真正阻断交付的问题”。
- 使用 [references/problem-abstraction.md](references/problem-abstraction.md) 做剥离，优先找出：
  - 当前最痛的表象症状
  - 真正阻断结果的机制或主瓶颈
  - 不能绕开的硬约束
  - 真正要守住的目标
- 把问题本质压缩成一句话：
  - `本质不是 X 本身，而是在 Y 约束下，角色/系统缺少 Z 机制，导致 D 无法稳定发生。`
- 只在内部用 [references/philosophical-elevation.md](references/philosophical-elevation.md) 再升一层校准“系统失去了哪项根能力”；对外必须立刻翻译回白话方法论。
- 默认不要问“这像哪个旧案例”；要问“这次到底哪些不变量和约束在控制结果”。

### 3. Generate the professional owner from responsibilities and gates

- 在给“方法论主线”之前，先回答三件事：
  - 谁对结果成败负责
  - 谁定义什么叫合格、安全或可发布
  - 谁握着最关键的验收门、升级门或回退门
- 使用 [references/professional-role-anchor.md](references/professional-role-anchor.md) 生成主专业角色。
- 如果涉及多人协作，默认只选 1 个主专业角色；其他角色只作为约束方、协作方或依赖项。
- 如果当前领域没有现成头衔，先输出职责型角色，再决定是否翻译成行业母语。
- 如果问题是“生成内容 / prompt / workflow / 自动化链路”的质量不稳，优先选择那个守住任务定义、评测集、变量控制和回归门的角色，而不是只负责润色表述的人。
- 如果问题对象就是当前 skill / prompt / workflow / rubric 本身，优先选择守住抽象逻辑、选择规则和评测门的系统所有者，而不是失败案例里的一线角色。

### 4. Build methodology from generic control surfaces, not scenario maps

- 使用 [references/control-surfaces.md](references/control-surfaces.md) 生成方法论，不要再按场景白名单选流程。
- 默认先判断 1 个主失稳形态，再补 1 到 2 个次失稳形态，然后从下列控制面里选 2 到 4 个真正需要先立住的面：
  - 权威面：谁有权定义真相、质量、安全或最终通过
  - 证据面：哪一版事实、哪一个时点、哪一种来源是权威
  - 边界面：哪些约束不可越、哪些动作不可做
  - 分层面：哪些东西必须先拆开，例如事实与解释、系统与案例、正常路径与例外
  - 顺序面：什么必须先冻结，什么必须后置
  - 验收面：什么条件满足才算能推进或能交付
  - 升级/回退面：什么情况下必须停、升、降或回滚
  - 反馈/回归面：怎样证明新动作比旧动作更稳
- 默认用下面顺序生成“方法论主线”：
  1. 先冻结 `权威 / 证据 / 边界`
  2. 再拆开被混在一起的层
  3. 再按明确顺序推进工作和交接
  4. 最后用 `验收 / 升级 / 回归` 收口
- 方法论主线必须回答：
  - 如果按这个专业角色的职能来做，这类问题先定什么
  - 再推进什么
  - 最后如何验收、何时升级或回退

### 5. If the problem is the method system itself, rewrite the generator

- 如果用户指出的不是业务案例本身，而是 `当前 skill / prompt / taxonomy / workflow / rubric` 的泛化失败，不要把主要篇幅拿去教他怎么处理两个失败 case。
- 这类问题至少要拆开五层：
  - 问题抽象层：系统依据什么读出真正约束
  - 角色生成层：系统依据什么长出主专业角色
  - 控制面选择层：系统依据什么长出方法论主线
  - 翻译层：系统如何把方法论压回当前场景
  - 评测层：系统依据什么证明自己真的更稳
- 先修生成逻辑和评测门，再看案例表述是否顺眼。
- 例子可以作为回归输入，不能再作为逻辑本体。
- 明确识别三种坏答案：
  - 一上来就补更多样例
  - 花大篇幅修两个失败 case，却没重写选择机制
  - 只修润色层，不修抽象、选角和回归层
- 输出时继续沿用统一八段结构，但具体含义改成：
  - `专业角色锚点` = 系统 owner 及其守住的 gate
  - `问题本质` = 元问题路由或生成层为什么失稳
  - `方法论主线` = 先修哪一层生成器、再修哪一层回归门
  - `专业工作流` = 具体改哪些文件、哪些规则、哪些测试
  - `风险与下一步` = 哪些迹象说明系统仍在靠案例活着
- 元问题场景的前四段顺序固定为：
  1. `一句话结论`
  2. `专业角色锚点`
  3. `问题本质`
  4. `方法论主线`
- 在这四段完成前，不要出现旧案例名、不要解释两个失败样例怎么修、不要把案例 owner 当论证主体。

### 6. If the user forbids manual steps, redesign around automation

- 如果用户明确要求“禁止人工环节”“端到端自动完成”，不要再把人工回写、人工审稿、人工补料当成主路径。
- 这类场景默认改写成自动化链路视角：
  - 输入源：已有结构化资料、历史语料、公开可抓取资料、静态规则表、事实卡片
  - 处理链：重建上下文 -> 约束事实源 -> 生成判断 -> 受限成稿 -> 自动质检 -> 有限次回退
  - 输出物：节点职责、输入输出字段、自动 gate、回退条件、不可达目标
- 明确区分什么能自动做好，什么不能被自动“做真”：
  - 可达：降低空话率、降低模板感、提升事实密度、稳定结构、模拟一致风格
  - 不可强承诺：真实第一手经历、真实当下个人判断、把机器产物说成真人亲笔

### 7. Keep the ethical and factual boundary explicit

- 不要帮助用户伪造资历、冒充专业身份、欺骗评审、规避必要披露，或把不确定事实说成确定事实。
- 可以帮助用户快速建立判断框架、组织专业协作、压缩学习曲线、提升汇报与验收质量。
- 遇到高风险领域时，继续遵守该领域本身的安全规则；“方鸿渐”不是绕过安全的理由。
- 如果关键事实仍不充分，明确写出：
  - 已确认的事实
  - 仍属推断的判断
  - 下一步应如何补证或验证

## Output Contract

默认按下面结构输出：

1. `一句话结论`
2. `专业角色锚点`
3. `问题本质`
4. `方法论主线`
5. `专业工作流`
6. `外行可执行指挥稿`
7. `关键证据 / 推断边界`
8. `风险与下一步`

如果问题对象是方法系统本身，继续使用同一结构，但必须满足两个额外硬约束：

1. 前四段必须先把 `系统 owner + 生成器失稳原因 + 五层改法` 说完
2. 具体业务案例只能作为回归输入放在后半段，不能提前承担论证主线

## Writing Rules

- 先说结论，再展开
- 多用判断句，少用空泛鼓励
- “专业角色锚点”默认只写 1 到 2 句，讲清“谁是专业的”和“他的职责是什么”
- “问题本质”默认只写 1 到 2 句，讲清真正卡在哪、为什么老在这里反复
- “方法论主线”最多 3 条，每条都必须是可以直接转成工作顺序的白话原则句
- 每一条抽象判断后面，都要让用户能看出“在你这个问题里具体意味着什么”
- 如果问题对象是系统本身，“方法论主线”应优先回答：
  - 选择机制该怎么重写
  - 抽象边界该怎么重画
  - 回归门该怎么建立
- 如果问题对象是系统本身，前四段里不要出现具体业务案例名；案例只能在后半段当回归样本提及
- 默认不要直接复述旧案例、旧角色名或旧行业话术，除非当前上下文已经给出足够证据，能自然长出这些名称
- 如果答案只剩 `协调 / 推进 / 统一 / 多沟通` 这些词，却说不清谁守住结果、什么算过关、何时升级，说明还没找到真正的方法论
- 默认不要直接使用 `可判定性 / 可协调性 / 可正当化性 / 可控性 / 可归属性 / 可适应性` 这类词；如确需使用，必须紧跟白话解释
- 每次都要标明直接证据和推断的边界

## Resources

- [references/problem-abstraction.md](references/problem-abstraction.md)：把表象问题压缩成问题本质的剥离框架
- [references/professional-role-anchor.md](references/professional-role-anchor.md)：先判断“谁是专业的”，再从职责和验收门里生成主专业角色
- [references/control-surfaces.md](references/control-surfaces.md)：从通用控制面生成方法论主线，不再依赖场景地图
- [references/philosophical-elevation.md](references/philosophical-elevation.md)：把问题从机制层继续上穿到系统能力层，再翻译回方法论层
- [references/self-bootstrap-rubric.md](references/self-bootstrap-rubric.md)：当问题对象就是当前方法系统本身时，强制切换到系统 owner、五层诊断和跨样本回归 gate

## Validation

Run:

```bash
python3 /Users/pocket/.codex/skills/.system/skill-creator/scripts/quick_validate.py /Users/pocket/Documents/project/fanghongjian
```
