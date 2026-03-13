# Mistral Large 2

**Mistral Large 2** is Mistral AI's flagship frontier model, released in July 2024. With 123 billion parameters, it was designed to deliver GPT-4o-level performance while remaining significantly more efficient and cost-effective than its predecessors.

## Technical Specifications

- **Release Date**: July 24, 2024
- **Developer**: [Mistral AI](../companies/Mistral-AI.md)
- **Architecture**: Dense Transformer (Single-model architecture, not MoE)
- **Parameters**: 123 Billion
- **Context Window**: 128,000 tokens
- **Output Limit**: 8,192 tokens
- **License**: Mistral Research License (Non-Commercial), Available on API and Weights for Research

## Key Features

- **Efficiency Focus**: Designed specifically to fit on a single node of 8xH100 GPUs for inference, maximizing throughput.
- **Multilingual Powerhouse**: Exceptional performance across dozens of languages, including European languages (French, German, Spanish, Italian) and coding languages (Python, Java, C++, etc.).
- **Function Calling**: State-of-the-art capabilities in function calling and tool use, often surpassing GPT-4o in reliability.
- **Reasoning**: Strong mathematical reasoning capabilities (MATH score 76.9%).

## Benchmarks

| Benchmark | Score | Notes |
| :--- | :--- | :--- |
| **MMLU** | 84.0% | General Knowledge (5-shot) |
| **MATH** | 76.9% | Mathematical reasoning |
| **HumanEval** | 92.0% | Coding capability |
| **Multilingual MMLU** | ~80%+ | Average across FR, DE, ES, IT |

## Impact

Mistral Large 2 proved that a focused, "mid-sized" (123B) model could compete directly with massive models like Llama 3.1 405B and GPT-4o. Its release demonstrated that specialized architecture and high-quality data could yield better results than simply scaling up parameter counts indiscriminately.
