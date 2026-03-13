# DeepSeek-R1

**DeepSeek-R1** is a state-of-the-art open-weights reasoning model developed by DeepSeek, known for matching or exceeding the performance of proprietary models like OpenAI's o1 while being significantly more efficient and cost-effective.

## Technical Specifications

- **Release Date**: January 20, 2025
- **Developer**: [DeepSeek](../companies/DeepSeek.md)
- **Architecture**: Mixture-of-Experts (MoE)
- **Parameters**: 671 Billion (Total), 37 Billion (Active)
- **Context Window**: 128,000 tokens
- **Output Limit**: 8,192 tokens (standard), extensible
- **License**: MIT License (Open Weights)

## Key Features

- **Reasoning Capabilities**: Uses a specialized "Chain of Thought" (CoT) process to break down complex problems in math, coding, and logic.
- **Distilled Models**: Released alongside a family of smaller, distilled models (based on Qwen and Llama architectures) ranging from 1.5B to 70B parameters, bringing high-level reasoning to consumer hardware.
- **Cost Efficiency**: The API pricing was disruptively low at launch ($0.55/1M input tokens), triggering an industry-wide price war.
- **Open Weights**: Fully open weights allow researchers and developers to fine-tune and deploy the model locally.

## Benchmarks

| Benchmark | Score | Notes |
| :--- | :--- | :--- |
| **MMLU** | 90.8% | General Knowledge (5-shot) |
| **MATH** | 97.3% | Mathematical reasoning (Pass@1) |
| **HumanEval** | 96.3% | Coding capability (Python) |
| **AIME 2024** | 79.8% | Advanced Mathematics Competition |

## Impact

DeepSeek-R1's release was a watershed moment for open-source AI, proving that open models could compete with the best closed-source models in complex reasoning tasks. Its aggressive pricing and permissive license accelerated the commoditization of intelligence and forced major Western labs to reconsider their closed strategies.
