# Supercompute Labs

**AI research and development solutions. Engineered for the impossible.**

## ⚓ [Flagship](https://github.com/supercompute-labs/flagship): our inference stack

Flagship gets large models running fast on hardware that shouldn't be able to run them. It has three parts:
- **Tools:** cold-prompt benchmarking, A/B tuning with controls, and quality gates.
- **Method:** a documented process for finding the fast settings and proving they're real. See [METHODOLOGY](https://github.com/supercompute-labs/flagship/blob/main/docs/METHODOLOGY.md).
- **Recipes:** tuned, reproducible configs, with raw data and failures included.

| Recipe | Model | Hardware | Result |
|---|---|---|---|
| [001](https://github.com/supercompute-labs/flagship/tree/main/recipes/qwen38-flashnext-rtx5080-basalt) | Qwen3.8-Flash-Next (91 GB MoE) | 1× RTX 5080 16 GB | **47 → 149 tok/s** decode @ 64k |
| 002 | DeepSeek-V4.1-Flash | 1× RTX 5080 16 GB | *in progress* |

**Cold or it didn't happen** · **One change at a time** · **Lossy is labeled lossy** · **Publish the failures**
