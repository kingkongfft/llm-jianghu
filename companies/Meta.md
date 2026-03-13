# Meta AI (Llama)

Meta AI 是开源大模型领域的绝对领导者。通过 Llama 系列，Meta 成功将“开源”变成了大模型生态的主流选择，推动了全球私有化部署和微调技术的繁荣。

## 📅 关键里程碑 (Timeline)

### 2013-2022: FAIR 与早期积累
- **2013年**: Mark Zuckerberg 成立 **FAIR (Facebook AI Research)**，由图灵奖得主 **Yann LeCun** 领导。
    - *理念*: 致力于开放科学研究，推动 AI 基础理论发展。
- **2016年**: 开发 **PyTorch** 深度学习框架，凭借其易用性和动态图特性，逐渐取代 TensorFlow 成为学术界首选。
- **2022年**: 发布 **OPT** (Open Pre-trained Transformer) 和 **Galactica** (科学大模型)，但在因产生错误信息被网友群嘲后迅速下架，这成为 Llama 诞生的前奏。

### 2023: Llama 横空出世
- **2023年2月**: **LLaMA (Large Language Model Meta AI)** 1 发布。
    - *事件*: 最初仅面向科研人员申请，但权重迅速在 4chan 和 BT 站泄露，引发了开源社区的“寒武纪大爆发”。
    - *影响*: 证明了较小参数模型 (7B/13B) 通过高质量数据训练也能达到卓越性能 (Chinchilla Scaling Laws)。
- **2023年7月**: **Llama 2** 发布。
    - *特点*: 正式宣布**开源免费可商用**，并与 Microsoft 达成深度合作。将上下文扩展至 4k。

### 2024-2026: Llama 3 与多模态生态
- **2024年4月**: **Llama 3** 发布。
    - *规格*: 8B/70B 版本，使用了 15T token 进行训练，性能大幅提升。
- **2024年7月**: **Llama 3.1** 发布。
    - *里程碑*: 推出 **405B** 版本，这是首个开源的“前沿级 (Frontier-level)”模型，对标 GPT-4o。上下文扩展至 128k。
- **2025年**:
    - **Llama 4**: 
        - **Llama 4 Maverick**: 400B MoE (17B 激活)，性能超越 GPT-4o。
        - **Llama 4 Scout**: 109B MoE (17B 激活)，拥有 **10M Token** 超长上下文窗口，专为代码库分析和长文档设计。
    - **AI Studio**: Meta 推出平台，允许用户基于 Llama 创建个性化 AI 角色 (Characters)。
- **2026年**:
    - 持续推动 **Llama 生态系统**，包括端侧设备 (On-device) 运行和小模型 (SLM) 优化。
    - 强化与雷朋智能眼镜 (Ray-Ban Meta) 等硬件的结合。

## 🚀 核心模型系列

| 模型 | 版本 | 参数量 | 特点 | 发布时间 |
| :--- | :--- | :--- | :--- | :--- |
| **Llama 1** | LLaMA | 7B/13B/33B/65B | 开源鼻祖，验证 Scaling Laws | 2023.02 |
| **Llama 2** | Llama 2 | 7B/13B/70B | 正式商用许可，RLHF 对齐 | 2023.07 |
| **Llama 3** | Llama 3/3.1/3.2 | 8B/70B/405B | 性能怪兽，405B 挑战闭源最强 | 2024.04+ |
| **Llama 4** | Llama 4 (Maverick/Scout) | 109B/400B (MoE) | MoE 架构，**10M** 超长上下文 | 2025 (预测) |

## 🔑 核心贡献

1.  **PyTorch**: 现代 AI 研究的基石。
2.  **Open Weights (权重开源)**: 打破了 OpenAI/Google 的垄断，让每个人都能在本地运行大模型。
3.  **Yann LeCun 的愿景**: 坚持“世界模型 (World Models)”和“开源 AI 才是未来”的理念，反对过度监管 AI 开源。

## 🔗 参考来源 (Sources)
- *Meta AI Blog: Introducing Llama 3*
- *Wikipedia: Llama (language model)*
- *Towards AI: Roadmap to 2026*
- *Codingscape: Most powerful LLMs in 2026*
