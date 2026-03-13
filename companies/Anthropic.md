# Anthropic (AI Safety & Claude)

Anthropic 是一家专注于 **AI 安全 (AI Safety)** 和 **可解释性 (Interpretability)** 的研究型公司，由前 OpenAI 研究副总裁 Dario Amodei 及其团队创立。其核心产品 **Claude** 被视为 GPT 系列最有力的竞争者之一。

## 📅 关键里程碑 (Timeline)

### 2020-2022: 成立与早期研究
- **2020年**: 
    - Dario Amodei (OpenAI 前研究副总裁) 带领 GPT-3 核心团队成员离开 OpenAI。
    - **Anthropic 成立**: 获得 Skype 联合创始人 Jaan Tallinn 等人的早期投资，定位为公益性更强的 Public Benefit Corporation (PBC)。
    - *初衷*: 担忧 OpenAI 在商业化过程中可能忽视 AI 安全问题。
- **2021年**: 发表多篇关于 Transformer 可解释性 (Mathematical Framework for Transformer Circuits) 的论文，奠定了其技术路线。
- **2022年**:
    - **A轮/B轮融资**: 获得包括 Sam Bankman-Fried (FTX) 等投资者的数亿美元注资。
    - **Constitutional AI (宪法 AI)**: 提出基于规则（而非人类反馈）训练无害 AI 的新方法 (RLAIF)。
    - **Claude 早期版本**: 完成训练并在内部进行安全测试，未对外发布。

### 2023: Claude 面世与巨头结盟
- **2023年3月**: **Claude 1 发布**: 正式向受邀用户开放，因其长文本处理能力和安全性受到好评。
- **2023年5月**: **Claude 2 发布**: 支持 **100k Token** 上下文窗口（当时业界领先），可处理整本书籍。
- **2023年9月**: **Amazon 投资**: 亚马逊宣布向 Anthropic 投资 **40 亿美元**，成为主要云服务伙伴。
- **2023年10月**: **Google 投资**: 谷歌承诺投资 **20 亿美元**。Anthropic 形成“背靠两大云巨头”的独特格局。

### 2024-2026: Claude 3 与企业级应用 (Enterprise Era)
- **2024年3月**: **Claude 3 系列发布**: 推出 Haiku (快)、Sonnet (平衡)、Opus (强) 三款模型。Opus 在多项基准测试中超越 GPT-4。
- **2024年6月**: **Claude 3.5 Sonnet 发布**: 以中等模型的成本实现了超越 Opus 的性能，并在代码能力上大幅领先，推出了 **Artifacts** 功能（实时预览代码结果）。
- **2024年**:
    - **Claude Code**: 推出专为开发者设计的编码 Agent。
    - **Team / Enterprise Plan**: 全面发力企业市场。
- **2025年**:
    - **Claude 3.5 Opus / 4.5**: 发布更强推理能力的模型版本 (搜索结果提及 Sonnet 4.6/Opus 4.6)。
    - **Desktop App**: 发布桌面端应用。
    - **Palantir 合作**: 成为其机密任务中唯一使用的 AI 模型。
- **2026年**:
    - 持续优化 Agentic Workflow (代理工作流) 能力，不仅是聊天，而是替用户执行复杂任务。

## 🚀 核心模型与产品

| 系列 | 代表模型 | 特点 | 适用场景 |
| :--- | :--- | :--- | :--- |
| **Claude Opus** | Claude 3 Opus, 4.5 (预测) | 最强推理、最聪明 | 复杂任务、科学研究、高精度分析 |
| **Claude Sonnet** | Claude 3.5 Sonnet, 4.6 (预测) | 性价比之王、编码极强 | 代码开发、数据提取、日常任务 |
| **Claude Haiku** | Claude 3 Haiku | 极速、低成本 | 客服机器人、实时翻译、海量文档处理 |

## 🔑 核心技术理念

- **Constitutional AI (宪法 AI)**: 
    - 训练模型遵循一套明确的原则（如《联合国人权宣言》），而非仅仅依赖人类标注员的反馈 (RLHF)，旨在解决人类偏见和难以扩展监督的问题。
- **Context Window (长上下文)**:
    - 始终保持在长文本处理领域的领先地位（最早普及 100k/200k Token），擅长“大海捞针” (Needle In A Haystack) 测试。
- **Artifacts**:
    - 创新的 UI 交互模式，将生成的代码、文档、图表在侧边栏独立渲染，不仅是对话，更是协作生产力工具。

## 🔗 参考来源 (Sources)
- *Anthropic Official Blog: Introducing Claude*
- *Wikipedia: Anthropic*
- *Taskade: History of Claude AI & Anthropic*
