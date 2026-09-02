<div align="center">
  <img src="assets/banner.svg" alt="alexey@rig" width="100%">
</div>

<p align="center">
  <a href="https://x.com/superalesha"><b>X / @superalesha</b></a> ·
  <a href="https://alesha.pro"><b>alesha.pro</b></a> ·
  <a href="https://t.me/fuckup_files"><b>t.me/fuckup_files</b></a>
</p>

## About

By day I run infrastructure. The rest of the time I bench LLMs on a hand-built 4x RTX 3090 rig with 96 GB of VRAM, and I publish every measurement with raw traces and per-run provenance attached. People argue about quants and reasoning effort from vibes. I run the thing and count.

## Featured work

| Project | Stars | What it is |
|---|:---:|---|
| [**atlas**](https://github.com/alesha-pro/atlas) | ![stars](https://img.shields.io/github/stars/alesha-pro/atlas?style=flat) | Interactive canvas that takes an LLM apart tensor by tensor. It measures INT8/INT4/FP8 error, distributions, spectra and outlier channels on every weight tensor |
| [**evalatro**](https://github.com/alesha-pro/evalatro) | ![stars](https://img.shields.io/github/stars/alesha-pro/evalatro?style=flat) | The open benchmark where language models play real Balatro |
| [**4x3090-llm-benchmarks**](https://github.com/alesha-pro/4x3090-llm-benchmarks) | ![stars](https://img.shields.io/github/stars/alesha-pro/4x3090-llm-benchmarks?style=flat) | Public archive of local LLM speed measurements from the rig, with exact launch commands and per-run provenance |
| [**vllm-cross-model-kv**](https://github.com/alesha-pro/vllm-cross-model-kv) | ![stars](https://img.shields.io/github/stars/alesha-pro/vllm-cross-model-kv?style=flat) | Cross-model KV cache transfer in vLLM: a smaller model prefills, a bigger one answers from its cache |
| [**qwen38-27b-bench-4x3090**](https://github.com/alesha-pro/qwen38-27b-bench-4x3090) | ![stars](https://img.shields.io/github/stars/alesha-pro/qwen38-27b-bench-4x3090?style=flat) | Raw traces from the 67-hour Qwen3.8-27B quant grinder, GGUF sweeps plus a 288-point vLLM vs SGLang matrix |
| [**tools**](https://github.com/alesha-pro/tools) | ![stars](https://img.shields.io/github/stars/alesha-pro/tools?style=flat) | ComfyUI workflows and benchmark configs from the rig |

## The rig

The rig is 4x RTX 3090 with 96 GB of VRAM in total. P2P is verified on all 12 pairs, the cards run at 220 W each on PCIe 3.0 x16. Engines on the box: vLLM, llama.cpp, exllamav3 + tabbyAPI, plus SGLang when it behaves. Ampere sm_86 has no native FP8, and most quant advice out there assumes everyone owns a Hopper. I enjoy measuring what actually wins on these cards.

## Highlights from X

- [I took Qwen3.8-27B apart to see how it works inside](https://x.com/superalesha/status/2091529279456653415). I tapped every FFN neuron, all 1,114,112 of them, and pushed 3.92M tokens through in 87 minutes. Neurons that fire on more than 90% of tokens: 2.
- [Settling the quant debate for Qwen3.8 27B once and for all](https://x.com/superalesha/status/2090778175970152743). I ran 8 quants through 720 real agentic and reasoning tasks each. That is 5,760 runs and 67 hours on home hardware.
- [1-bit quant scoring 76.9 vs 79.1 for bf16](https://x.com/superalesha/status/2076972432473071625). The table looked too good to be true, so I downloaded the model and checked it on real agent loops.
- [Three local models shipped a game, a video and a soundtrack](https://x.com/superalesha/status/2089620381543849998). Qwen3.8 27B wrote the shooter, Minimax H3 rebuilt my run in its own render, Minimax Music 3 scored it. Three local models, one apartment, zero cloud.
- [Reasoning effort, measured](https://x.com/superalesha/status/2091765603967099390). I burned 30.9M tokens across 83 arms. xhigh costs 4.1x the tokens of off for 12 extra solved tasks out of 150.

## Numbers

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=alesha-pro&amp;hide_border=true&amp;theme=github-dark-blue">
    <img height="170" alt="GitHub streak" src="https://streak-stats.demolab.com?user=alesha-pro&amp;hide_border=true">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=alesha-pro&amp;theme=github_dark">
    <img height="170" alt="GitHub stats" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=alesha-pro">
  </picture>
</p>

---

Every number on this profile comes from a real run. If it is not in a repo with raw data, I did not say it.
