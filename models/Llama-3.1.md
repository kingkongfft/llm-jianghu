# Llama 3.1

**Llama 3.1** is Meta's groundbreaking family of open-weights models, released in July 2024. The series, particularly the 405B variant, marked the first time an open-source model achieved performance parity with the best closed-source frontier models (like GPT-4o).

## Technical Specifications

- **Release Date**: July 23, 2024
- **Developer**: [Meta](../companies/Meta.md)
- **Architecture**: Dense Transformer (Mixture-of-Experts for 405B estimated, though technically "standard Transformer with Grouped-Query Attention")
- **Variants**:
    - **8B**: Lightweight, runs on consumer GPUs.
    - **70B**: Powerful general-purpose model.
    - **405B**: Frontier-class model.
- **Context Window**: 128,000 tokens
- **License**: Custom Community License (Permissive for most uses)

## Key Features

- **Massive Scale**: The 405B model was trained on over 15 trillion tokens using 16,000 H100 GPUs.
- **Multilingual**: Supports 8 languages out of the box.
- **Tool Use**: Strong capabilities in zero-shot tool use and function calling.
- **Distillation**: Meta explicitly encouraged using the 405B model to distill knowledge into smaller models, a departure from restrictive licenses of competitors.

## Benchmarks (405B)

| Benchmark | Score | Notes |
| :--- | :--- | :--- |
| **MMLU** | 88.6% | General Knowledge (5-shot) |
| **MATH** | 73.8% | Mathematical reasoning |
| **HumanEval** | 89.0% | Coding capability |
| **GPQA** | 50.8% | Graduate-level reasoning |

## Impact

Llama 3.1 405B shattered the "open-source ceiling," proving that open weights could match the performance of proprietary models. Mark Zuckerberg described it as the "Linux moment" for AI, predicting that open source would eventually become the industry standard.
