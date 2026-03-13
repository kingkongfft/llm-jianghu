# DeepSeek (深度求索)

DeepSeek 是一家中国 AI 初创公司，专注于大模型底层技术创新，以极其高效的训练成本和强大的开源精神在 2024-2025 年震撼全球 AI 社区。

## 📅 关键里程碑 (Timeline)

### 2023: 成立与起步
- **2023年**: **DeepSeek (深度求索)** 成立，隶属于量化私募巨头**幻方量化 (High-Flyer)**。
    - *背景*: 依托幻方强大的算力储备（万卡集群），致力于探索 AGI。
- **2023年11月**: 发布 **DeepSeek Coder**。
    - *首战成名*: 这是当时开源界最强的代码模型之一，参数虽小但在 HumanEval 等榜单上表现惊艳。

### 2024: 混合专家 (MoE) 与价格屠夫
- **2024年5月**: 发布 **DeepSeek-V2**。
    - *架构创新*: 采用 **MoE (Mixture-of-Experts)** 架构，总参数 236B 但激活参数仅 21B，推理成本极低。
    - *API 价格*: 宣布 API 价格仅为 GPT-4 的 **1%** 甚至更低，引发国内外模型降价潮。
- **2024年6月**: **DeepSeek-Coder-V2** 发布。
    - *超越闭源*: 在代码能力上超越了当时的 GPT-4 Turbo，成为首个在 Coding 领域击败顶尖闭源模型的开源模型。
- **2024年12月 (圣诞礼物)**: **DeepSeek-V3** 发布。
    - *里程碑*: 671B 参数 (37B 激活)，训练成本仅 **557.6 万美元**（相比之下 Llama 3/GPT-4 动辄数亿美元）。
    - *技术细节*: 采用了 **FP8 混合精度训练** 和 **多头潜在注意力 (MLA)** 等黑科技。

### 2025: 推理模型爆发 (Reasoning Era)
- **2025年1月**: **DeepSeek-R1** 发布。
    - *对标 o1*: 这是一个拥有“思考过程 (Chain of Thought)”的推理模型，性能对标 OpenAI o1。
    - *开源蒸馏*: 同时发布了基于 Qwen/Llama 蒸馏的小尺寸 R1 (1.5B/7B/14B/32B)，让手机端也能跑“思考模型”。
- **2025年8月**: **DeepSeek-V3.2 / 3.1** 发布。
    - *混合推理*: 支持 **Think (思考模式)** 和 **Non-Think (非思考模式)** 切换，大幅提升了工具调用 (Tool Use) 和多步任务规划能力，特别是针对语音 AI 代理 (Voice AI Agents) 进行了优化。
    - *成本*: 提供了极致的推理性价比，使得全天候运行的 AI Agent 在经济上变得可行。

## 🚀 核心模型系列

| 模型 | 版本 | 参数量 (总/激活) | 特点 | 发布时间 |
| :--- | :--- | :--- | :--- | :--- |
| **DeepSeek-LLM** | 7B/67B | 7B/67B | 第一代基座模型 | 2023.11 |
| **DeepSeek-Coder** | V1/V2 | 1.3B~236B | 专精代码，V2超越GPT-4 | 2023.11+ |
| **DeepSeek-V2** | V2 | 236B/21B | MoE 架构，超低成本 | 2024.05 |
| **DeepSeek-V3** | V3/V3.2 | 671B/37B | 综合能力最强开源模型，V3.2 优化 Agent | 2024.12+ |
| **DeepSeek-R1** | R1 (及蒸馏版) | 671B/37B | 推理模型 (Reasoning)，开源 o1 | 2025.01 |

## 🔑 核心贡献与理念

1.  **开源精神 (Open Source)**: 坚持由内而外地开源，不仅开源权重，还开源了部分训练细节和中间检查点。
2.  **极致效率 (Efficiency)**:
    - **MLA (Multi-Head Latent Attention)**: 大幅降低显存占用 (KV Cache)。
    - **DeepSeekMoE**: 细粒度专家路由，极大提升推理效率。
    - **FP8 Training**: 率先在大规模集群上验证了低精度训练的可行性。
3.  **价格破坏者**: 通过技术创新将大模型推理成本降低了两个数量级，推动 AI 普惠。

## 🔗 参考来源 (Sources)
- *DeepSeek Official Website & Papers*
- *TechTarget: DeepSeek Explained*
- *Telnyx: New Open-Weight LLMs for Voice AI (DeepSeek V3.2)*
