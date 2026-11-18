# Supercompute Labs

**Datacenter speed, desk-side hardware.**

We tune local LLM inference on consumer GPUs and publish every result as a reproducible *dyno sheet*. Each sheet includes:
- the hardware, model, quant and engine version;
- before → after numbers;
- the exact flags;
- a quality gate;
- raw logs, failures included.

## Dyno sheets

| # | Model | Hardware | Engine | Result |
|---|---|---|---|---|
| 001 | [Qwen3.8-Flash-Next UD-IQ4_XS](https://github.com/supercompute-labs/basalt-flashnext-5080) | RTX 5080 16 GB + 60 GB RAM | Basalt 0.4.1 | **55 → 149 tok/s** decode |

## How we measure
- Cold prompts every request; no prompt-cache reuse.
- One change at a time, with interleaved baseline controls.
- Engine-reported token counts, never stream chunks.
- Quality and long-context needle gates before any config is called "best".
- Lossy speedups are labeled as lossy.
