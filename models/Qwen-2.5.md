# Qwen 2.5

**Qwen 2.5** is Alibaba Cloud's extensive family of large language models, released in September 2024, with a powerful "Max" version following in January 2025. It is widely regarded as one of the most capable open-weights model families available, particularly in coding and mathematics.

## Technical Specifications

- **Release Date**: September 19, 2024 (Base/Instruct), January 2025 (Max)
- **Developer**: [Alibaba Cloud](../companies/Alibaba.md)
- **Architecture**: Dense Transformer (with MoE variants)
- **Parameters**: 0.5B, 1.5B, 3B, 7B, 14B, 32B, 72B (Open); "Max" (Proprietary/API only)
- **Context Window**: 128,000 tokens (up to 1M in some variants)
- **License**: Apache 2.0 (for most sizes), proprietary for Max

## Key Features

- **Coding Powerhouse**: The "Qwen 2.5-Coder" variants are specifically optimized for programming tasks, often rivaling much larger proprietary models.
- **Qwen 2.5-Max**: The flagship API model (released Jan 2025) claims to outperform DeepSeek-V3 and challenge GPT-4o in reasoning and coding benchmarks.
- **Multilingual Mastery**: Exceptional performance in Chinese and English, with strong support for over 29 other languages.
- **Ecosystem**: Includes specialized "Math" and "Coder" models alongside the general-purpose "Instruct" models.

## Benchmarks (Qwen 2.5-Max / 72B Instruct)

| Benchmark | Score (Max) | Score (72B) | Notes |
| :--- | :--- | :--- | :--- |
| **Arena-Hard** | 89.4% | ~81.2% | Preference benchmark |
| **MMLU-Pro** | - | 71.6% | Advanced General Knowledge |
| **HumanEval** | - | 86.6% | Coding capability |
| **MATH** | - | 83.1% | Mathematical reasoning |

## Impact

Qwen 2.5 cemented Alibaba's position as the leader in the Chinese open-source AI ecosystem. The 72B model became the "gold standard" for deployable open-weights models in late 2024, offering the best balance of performance and hardware requirements before the release of DeepSeek-V3.
