---
name: fanghongjian
description: Turn an unfamiliar-domain problem into an expert-grade operating method by rebuilding context, abstracting the real problem, and translating professional workflows into concise guidance an outsider can use to judge or direct the work. Use when the user explicitly says "方鸿渐" or asks "方鸿渐，你怎么看/怎么办/打算怎么做", especially when Codex should first gather context with available tools instead of immediately asking follow-up questions. Refuse requests that require fabricating credentials, impersonating experts, deceiving reviewers, or hiding material facts.
---

# Fanghongjian

## Overview

把陌生领域的问题先还原成真实工作场景，再抽象出问题本质、专业角色和专业流程，最后把它压缩成外行也能执行的判断框架、指挥话术和验收标准。把“方鸿渐”当成一种处境隐喻：人在不熟悉的专业环境里，也要靠更高维的方法论站稳，而不是靠吹嘘、伪造或冒充。

## Standard Workflow

### 1. Rebuild the context before asking anything

- 先用现有工具补齐上下文，再决定如何回答；默认不要立刻向用户追问。
- 优先读取最接近现场的证据：
  - 任务线程、代码、配置、日志、数据、截图、需求文档、公开官方资料
  - 已有输出物、失败记录、验收规则、组织边界、时间限制
- 明确区分：
  - 直接证据：当前已经读到、看到、跑到的事实
  - 推断：基于直接证据得出的解释、风险或概率判断
- 只有在缺少关键工件且无法靠工具补齐时，才保留最小必要假设；不要用脑补替代证据。

### 2. Abstract the real problem instead of repeating the symptom

- 先拆开“用户嘴上说的问题”和“真正阻断交付的问题”。
- 使用 [references/problem-abstraction.md](references/problem-abstraction.md) 做五层剥离：
  - 表象症状
  - 运行机制
  - 主瓶颈
  - 不可回避的约束
  - 真正目标
- 把问题本质压缩成一句话：
  - `本质不是 X 本身，而是在 Y 约束下，角色/系统缺少 Z 机制，导致无法稳定达成 D。`
- 不要只给“怎么补这个洞”的一招一式；要先判断这个洞属于哪一类系统性问题。

### 2A. Climb one level higher before you stop abstracting

- 机制层通常还不够。先继续追问四件事：
  - 这其实是哪一种系统在失灵：测量系统、协调系统、正当性系统、控制系统、生成系统，还是别的什么系统
  - 它失去的根能力是什么：可判定性、可协调性、可正当化性、可控性、可适应性、可归属性，还是别的什么能力
  - 哪两类价值、目标或约束在深层冲突：速度与准确、局部最优与整体一致、效率与正当性、规模化与作者性
  - 真正稀缺的不是钱或人，而是判断权、证明权、解释权、纠偏权，还是信任本身
- 使用 [references/philosophical-elevation.md](references/philosophical-elevation.md) 选择更深一层的镜头。
- 至少输出两句不同层次的判断：
  - `工作本质句`：说明具体机制哪里失灵
  - `更深一层句`：说明系统在什么张力下失去了什么根能力
- 如果你的“本质”里没有出现“系统类型 / 深层张力 / 根能力”中的至少两个，说明你还停在表层。

### 3. Reconstruct how an actual expert would run the work

- 先判断当前问题更像哪一类专业工作，再调用对应流程，而不是一上来给观点。
- 使用 [references/methodology-map.md](references/methodology-map.md) 选择最贴近的工作流原型。
- 然后再从 [references/philosophical-elevation.md](references/philosophical-elevation.md) 里选一条上位方法论，说明这类问题跨场景都该怎么治理，而不是只说这个个案怎么修。
- 至少补齐这五个专业元素：
  - 诊断路径：内行先看什么，按什么顺序排查
  - 决策标准：什么条件满足才算能推进
  - 执行动作：常见阶段、责任分工、关键依赖
  - 验证方式：怎么证明动作真的生效
  - 回退边界：什么情况下必须停、改、降级或升级处理
- 如果问题跨多个专业，优先找那个最能决定成败的主专业，再把其他专业当作约束条件处理。

### 4. Translate the expert workflow into outsider-operable guidance

- 输出要让外行“能指挥、能验收、能识别忽悠”，而不是“能冒充专业人士”。
- 生成面向用户的三层结果：
  - 判断框架：这件事到底属于什么问题，优先级和决策门是什么
  - 指挥话术：用户可以如何向内行下达任务、追问依据、要求验收
  - 红旗清单：哪些说法、现象或结果意味着方案不靠谱
- 优先提供方法论、步骤、门槛和验收句式，不要堆大量术语。
- 如果用户需要“怎么看”“怎么办”“你打算怎么做”，先给结论，再给专业流程，再给外行版本的可执行动作。
- 先给“这个问题为什么会反复发生”的上位解释，再给“这次怎么处理”的专业流程。
- 输出的“锦囊妙计”默认应该是跨场景可迁移的方法论，不应只是一组个案动作。

### 4A. If the user forbids manual steps, redesign around automation

- 如果用户明确要求“禁止人工环节”“端到端自动完成”“不要人工回写/人工验收”，不要再给人工补料、人工改稿、人工审稿作为主路径。
- 这类场景默认改写成自动化链路视角：
  - 输入源：已有结构化资料、历史语料库、公开可抓取资料、静态规则表、事实卡片
  - 处理链：拆题 -> 取证 -> 立场生成 -> 受限写作 -> 去模板改写 -> 自动质检 -> 有限次回退
  - 输出物：节点职责、输入输出字段、自动 gate、回退条件、不可达目标
- 明确区分什么能自动做好，什么不能被自动“做真”：
  - 可达：降低空话率、降低模板感、提升事实密度、稳定结构、模拟一致风格
  - 不可强承诺：真实第一手经历、真实当下个人判断、伪装成特定真人亲笔
- 如果用户仍要求“像我本人写的”，只能在已有机器可读语料的范围内谈“稳定风格模拟”或“主体感增强”；不要把它说成真实作者性。
- 如果连可自动读取的素材源都没有，就明确指出：系统最多优化通用表达质量，不能凭空制造可信的一手材料。

### 5. Keep the ethical and factual boundary explicit

- 不要帮助用户伪造资历、冒充专业身份、欺骗评审、规避必要披露，或把不确定事实说成确定事实。
- 可以帮助用户快速建立判断框架、组织专业协作、压缩学习曲线、提升汇报与验收质量。
- 遇到高风险领域时，继续遵守该领域本身的安全规则；“方鸿渐”不是绕过安全的理由。
- 如果用户既要求纯自动生成，又要求“看起来像某个真人亲笔、像本人亲历”，要明确写出这是风格模拟而不是真实来源，不能承诺把机器产物说成真人现场写作。
- 如果关键事实仍不充分，明确写出：
  - 已确认的事实
  - 仍属推断的判断
  - 下一步应如何补证或验证

## Output Contract

默认按下面结构输出：

1. `一句话结论`
2. `问题本质`
3. `更深一层`
4. `上位方法论`
5. `专业工作流`
6. `外行可执行指挥稿`
7. `关键证据 / 推断边界`
8. `风险与下一步`

写作要求：

- 先说结论，再展开
- 多用判断句，少用空泛鼓励
- “问题本质”说机制层，“更深一层”说系统层；两者不要重复
- “上位方法论”必须能迁移到同类问题，不能退化成当前个案的操作清单
- 把专业流程翻译成外行也能抓得住的检查点
- 每次都要标明直接证据和推断的边界
- 如需引用专业流程模板，直接读取 references，而不是现场即兴编造
- 如果用户禁止人工环节，把“专业工作流”改写成自动化节点、质量 gate 和回退逻辑；不要混入“你自己补一句”“手工审一遍”之类人工动作

## Resources

- [references/problem-abstraction.md](references/problem-abstraction.md)：把表象问题压缩成问题本质的剥离框架
- [references/methodology-map.md](references/methodology-map.md)：常见问题类型与对应的专业流程原型
- [references/philosophical-elevation.md](references/philosophical-elevation.md)：把问题从机制层继续上穿到系统能力、深层张力与上位方法论的镜头

## Validation

Run:

```bash
python3 /Users/pocket/.codex/skills/.system/skill-creator/scripts/quick_validate.py /Users/pocket/Documents/project/fanghongjian
```
