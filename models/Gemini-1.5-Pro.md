# Gemini 1.5 Pro

**Gemini 1.5 Pro** is Google's multimodal powerhouse, released in February 2024. It introduced a paradigm shift in context length, handling input windows of up to 2 million tokens, enabling the analysis of entire codebases, long videos, and books in a single pass.

## Technical Specifications

- **Release Date**: February 15, 2024 (Announced), subsequent updates in May and June.
- **Developer**: [Google](../companies/Google.md)
- **Architecture**: Mixture-of-Experts (MoE)
- **Context Window**: 1,000,000 to 2,000,000 tokens (Standard and Experimental)
- **Output Limit**: 8,192 tokens
- **Knowledge Cutoff**: January 2024 (at launch)

## Key Features

- **Long Context Understanding**: Achieved near-perfect recall (99%+) in "Needle in a Haystack" evaluations up to 10 million tokens.
- **Multimodality**: Natively understands text, images, audio, and video (up to 1 hour of video or 11 hours of audio).
- **Efficiency**: Uses significantly less compute than Gemini 1.0 Ultra while outperforming it on most benchmarks.
- **Tools**: Deep integration with Google Workspace and Search Grounding.

## Benchmarks

| Benchmark | Score | Notes |
| :--- | :--- | :--- |
| **MMLU** | 81.9% | General Knowledge (5-shot) |
| **MATH** | 58.5% | Mathematical reasoning |
| **HumanEval** | 71.9% | Coding capability |
| **Video MME** | 75.2% | Video understanding (SOTA) |

## Impact

Gemini 1.5 Pro redefined the limits of what LLMs could process, moving from "reading a page" to "reading a library." Its long-context capabilities opened new use cases in legal analysis, codebase refactoring, and video comprehension that were previously impossible.
