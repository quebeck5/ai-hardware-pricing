# AI Hardware Research & Performance Analysis

A comprehensive technical and financial research project evaluating hardware configurations for running Artificial Intelligence workloads (Mixture of Experts LLMs, dense inference, and fine-tuning) with realistic landed costs in Australia (delivered to Box Hill, Victoria, 3128).

🔗 **Live GitHub Pages Report:** [https://quebeck5.github.io/ai-hardware-pricing/](https://quebeck5.github.io/ai-hardware-pricing/)

---

## Featured Analysis: Budget Multi-GPU MoE Hardware Showdown

A detailed performance and economic comparison between three budget multi-GPU setups under $1,000 AUD:

1. **Setup C: 2x Nvidia Tesla P40 (24GB + 24GB = 48GB VRAM)**
   * Total Landed Cost: **$973.42 AUD** (inclusive of 2x turbine blower fan kits, 2x EPS-12V power adapters, and free delivery to Box Hill, VIC 3128).
   * Unlocks full 70-Billion parameter models (Llama-3.1-70B, Qwen-2.5-72B) and Mixtral 8x7B at Q5 with 64,000 tokens context completely in VRAM.
2. **Setup A: 1x Nvidia Tesla P40 (24GB) + 1x GeForce RTX 3060 (12GB) [36GB VRAM]**
   * Total Landed Cost: **$970.71 AUD**
   * Fits Mixtral 8x7B Q4_K_M in pure VRAM with 32k context. RTX 3060 provides direct HDMI/DP display outputs.
3. **Setup B: 2x GeForce RTX 3060 (12GB + 12GB = 24GB VRAM)**
   * Total Landed Cost: **$968.00 AUD**
   * Hits a 24GB VRAM ceiling; cannot run 47B MoE without CPU offload penalty (~4 tok/s). Excellent for 14B models (Qwen-2.5-14B) with 450 tok/s Tensor Core prefill.

### Key Architectural Insights

* **The Pascal FP16 Workaround:** While Pascal GP102 has 1:64 crippled FP16 compute, `llama.cpp` bypasses this via direct FP32 register dequantization and hardware INT8 `__dp4a` instructions (~47 TOPS), achieving full ~25 tok/s decode on Mixtral 8x7B.
* **Token Decode is Memory-Bandwidth Bound:** Tesla P40's wide 384-bit bus (345.6 GB/s) streams active expert weights at virtually the same rate as the RTX 3060's GDDR6 (360.0 GB/s).
* **Price Parity:** In Australia, all three configurations cost essentially the exact same amount (~$970 AUD landed via verified Buy-It-Now listings). Setup C provides **double the VRAM (48GB vs. 24GB)** for the same budget.

---

## Project Structure

* [`index.html`](index.html) / [`moe_gpu_comparison.html`](moe_gpu_comparison.html): Self-contained, responsive HTML comparison report.
* [`GEMINI.md`](GEMINI.md) / [`AGENTS.md`](AGENTS.md): Project rules and pricing constraints (verified Buy-It-Now only, session isolation, landed shipping).
