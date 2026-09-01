<div align="center">
  <img src="assets/banner.svg" alt="alexey@rig" width="100%">
</div>

<p align="center">
  <a href="https://x.com/superalesha"><b>X / @superalesha</b></a> ·
  <a href="https://alesha.pro"><b>alesha.pro</b></a> ·
  <a href="https://t.me/fuckup_files"><b>t.me/fuckup_files</b></a>
</p>

## About

By day I run infrastructure at a bank. The rest of the time I bench LLMs on a hand-built 4x RTX 3090 rig with 96 GB of VRAM, and I publish every measurement: raw traces, exact launch commands, per-run provenance. People argue about quants and reasoning effort from vibes. I run the thing and count.

## Featured work

| Project | Stars | What it is |
|---|:---:|---|
| [**atlas**](https://github.com/alesha-pro/atlas) | ![stars](https://img.shields.io/github/stars/alesha-pro/atlas?style=flat) | Interactive canvas that takes an LLM apart tensor by tensor. Measured INT8/INT4/FP8 error, distributions, spectra and outlier channels for every weight tensor |
| [**evalatro**](https://github.com/alesha-pro/evalatro) | ![stars](https://img.shields.io/github/stars/alesha-pro/evalatro?style=flat) | The open benchmark where language models play real Balatro |
| [**4x3090-llm-benchmarks**](https://github.com/alesha-pro/4x3090-llm-benchmarks) | ![stars](https://img.shields.io/github/stars/alesha-pro/4x3090-llm-benchmarks?style=flat) | Public archive of local LLM speed measurements from the rig, with exact launch commands and per-run provenance |
| [**vllm-cross-model-kv**](https://github.com/alesha-pro/vllm-cross-model-kv) | ![stars](https://img.shields.io/github/stars/alesha-pro/vllm-cross-model-kv?style=flat) | Cross-model KV cache transfer in vLLM: a smaller model prefills, a bigger one answers from its cache |
| [**qwen38-27b-bench-4x3090**](https://github.com/alesha-pro/qwen38-27b-bench-4x3090) | ![stars](https://img.shields.io/github/stars/alesha-pro/qwen38-27b-bench-4x3090?style=flat) | Raw traces from the 67-hour Qwen3.8-27B quant grinder: GGUF sweeps plus a 288-point vLLM vs SGLang matrix |
| [**tools**](https://github.com/alesha-pro/tools) | ![stars](https://img.shields.io/github/stars/alesha-pro/tools?style=flat) | ComfyUI workflows and benchmark configs from the rig |

## The rig

- **4x RTX 3090, 96 GB VRAM.** Ampere sm_86, no native FP8. Half of the quant advice on the internet assumes datacenter silicon, and I enjoy proving it on the cards people actually own.
- **P2P verified on all 12 pairs**, 220 W per card, PCIe 3.0 x16.
- **Engines on the box:** vLLM, llama.cpp, exllamav3 + tabbyAPI. SGLang when it behaves.

## Highlights from X

- [I took Qwen3.8-27B apart to see how it works inside](https://x.com/superalesha/status/2091529279456653415). All 1,114,112 FFN neurons tapped, 3.92M tokens pushed through in 87 minutes. Neurons that fire on more than 90% of tokens: 2.
- [Settling the quant debate for Qwen3.8 27B once and for all](https://x.com/superalesha/status/2090778175970152743). 8 quants, 720 real agentic and reasoning tasks each, 5,760 runs, 67 hours on home hardware.
- [1-bit quant scoring 76.9 vs 79.1 for bf16](https://x.com/superalesha/status/2076972432473071625). The table looked too good to be true, so I downloaded the model and checked it on real agent loops.
- [Three local models shipped a game, a video and a soundtrack](https://x.com/superalesha/status/2089620381543849998). Qwen3.8 27B wrote the shooter, Minimax H3 rebuilt my run in its own render, Minimax Music 3 scored it. Zero cloud.
- [Reasoning effort, measured](https://x.com/superalesha/status/2091765603967099390). 30.9M tokens across 83 arms: xhigh burns 4.1x the tokens of off for 12 extra solved tasks out of 150.

## Numbers

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=alesha-pro&amp;show_icons=true&amp;hide_border=true&amp;bg_color=00000000&amp;title_color=58a6ff&amp;icon_color=7ee787&amp;text_color=9da7b3">
    <img height="165" alt="GitHub stats" src="https://github-readme-stats.vercel.app/api?username=alesha-pro&amp;show_icons=true&amp;hide_border=true">
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=alesha-pro&amp;layout=compact&amp;hide_border=true&amp;bg_color=00000000&amp;title_color=58a6ff&amp;text_color=9da7b3">
    <img height="165" alt="Top languages" src="https://github-readme-stats.vercel.app/api/top-langs/?username=alesha-pro&amp;layout=compact&amp;hide_border=true">
  </picture>
</p>

---

Every number on this profile comes from a real run. If it is not in a repo with raw data, I did not say it.
