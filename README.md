# AI Hardware Research & Performance Analysis

A comprehensive technical and financial research project evaluating hardware configurations for running Artificial Intelligence workloads (Mixture of Experts LLMs, dense inference, and fine-tuning) with realistic landed costs in Australia (delivered to Box Hill, Victoria, 3128).

🔗 **Live GitHub Pages Report:** [https://quebeck5.github.io/ai-hardware-pricing/](https://quebeck5.github.io/ai-hardware-pricing/)

---

## Featured Analysis: Multi-GPU AI Hardware Showdown

A detailed performance and economic comparison between four multi-GPU configurations:

1. **Setup D: 3x Nvidia GeForce RTX 3060 12GB (36GB VRAM)**
   * Total Landed Cost: **$1,452.00 AUD** (tested retail used with 5-year warranty) or **$1,617.00 AUD** (brand new BIN).
   * Delivers **~280 to 380+ tok/s prefill** (<6s wait for 2k prompt) via 336 2nd-gen Ampere Tensor Cores.
   * Full plug-and-play support in Windows 11 and Linux with native display outputs.
2. **Setup C: 2x Nvidia Tesla P40 (24GB + 24GB = 48GB VRAM)**
   * Total Landed Cost: **$973.42 AUD** (inclusive of 2x turbine blower fan kits, 2x EPS-12V power adapters, and free delivery to Box Hill, VIC 3128).
   * Unlocks full 70-Billion parameter models (Llama-3.1-70B, Qwen-2.5-72B) and Mixtral 8x7B at Q5 with 64,000 tokens context completely in VRAM.
3. **Setup A: 1x Nvidia Tesla P40 (24GB) + 1x GeForce RTX 3060 (12GB) [36GB VRAM]**
   * Total Landed Cost: **$970.71 AUD**
   * Fits Mixtral 8x7B Q4_K_M in pure VRAM with 32k context. RTX 3060 provides direct HDMI/DP display outputs.
4. **Setup B: 2x GeForce RTX 3060 (12GB + 12GB = 24GB VRAM)**
   * Total Landed Cost: **$968.00 AUD**
   * Hits a 24GB VRAM ceiling; cannot run 47B MoE without CPU offload penalty (~4 tok/s). Excellent for 14B models (Qwen-2.5-14B) with 450 tok/s Tensor Core prefill.

---

## Project Structure

* [`index.html`](index.html) / [`moe_gpu_comparison.html`](moe_gpu_comparison.html): Self-contained, responsive HTML comparison report with interactive cards, KV cache tables, and build guides.
* [`GEMINI.md`](GEMINI.md) / [`AGENTS.md`](AGENTS.md): Project rules and pricing constraints (verified Buy-It-Now only, session isolation, landed shipping).
