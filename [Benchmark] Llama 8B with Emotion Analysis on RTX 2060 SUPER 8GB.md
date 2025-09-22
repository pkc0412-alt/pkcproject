🇰🇷 Korean Non-Expert Tests AI Models on RTX 2060 SUPER - Surprisingly Good Results!
Hey everyone! A regular person from Korea here (not an AI expert). I got so curious about the recent AI boom that I even used AI to help me build a simple benchmark tool to test some models at home. I used it to run benchmarks on the Bllossom-8B (4bit quantized) model together with the KlueBERT v2 emotion classification model on my RTX 2060 SUPER 8GB GPU. The results were way better than I expected, so I thought I'd share!

🔧 System Info
GPU: NVIDIA GeForce RTX 2060 SUPER (8GB VRAM)

CPU: Intel i7-9700K

RAM: 32 GB

OS: Windows 10

PyTorch + CUDA: PyTorch 2.5.1 + CUDA 12.1

Backend: llama.cpp (AVX, AVX2, FMA, F16C enabled)

cuBLAS/cuBLASLt: confirmed enabled

📊 Benchmark Results (Bllossom-8B, Q4)
Test setup: 3 prompts × 3 runs, batch size = 4, max tokens = 1024

Prompt	TTFT (ms)	Tokens/sec	VRAM (GB)	Power (W)	Temp (°C)
"오늘 하루 정말 멋진 일이 가득했어…"	~51 ms	46.5 t/s	~6.91	172.9	67
"프로젝트 마감일은 다가오는데…"	~39 ms	46.4 t/s	~6.96	172.3	70
"AI 기술의 발전이 기대되면서…"	~40 ms	46.1 t/s	~6.93	173.6	70
🕒 Loading & Latency
Model load time: ~102.64 ms (single load, reused afterwards)

TTFT (time to first token): ~39–51 ms

Prompt evaluation speed: 627–762 tokens/sec

Generation speed: ~18.9 ms/token → 52–53 tokens/sec

🧩 Multi-Model Pipeline Setup
This benchmark wasn't just running the LLM alone! I set up a pipeline with KlueBERT v2 (emotion classifier) and Bllossom-8B working together.

How it works:

KlueBERT v2 analyzes the emotion of the input prompt first

Bllossom-8B then generates text in the corresponding emotional tone

Examples:

"오늘 하루 정말 멋진 일이 가득했어…" → KlueBERT detects: Happiness (100%) → Bllossom-8B generates response in happy tone

"프로젝트 마감일은 다가오는데…" → KlueBERT detects: Fear (100%) → Bllossom-8B generates response in anxious tone

"AI 기술의 발전이 기대되면서…" → KlueBERT detects: Fear (100%) → Bllossom-8B generates response in concerned tone

⚙️ Optimization Options
GPU layers: -1 (all layers on GPU)

Model caching: enabled

Sequential loading: disabled

Auto retry: enabled

Loop detection: 5 (length 15)

Random seed: random

Graph reuse: up to 991 (via cuBLASLt algorithm optimization)

✅ Observations
VRAM usage stable around 6.9 GB

GPU power ~170 W, peak temp ~70°C

Generation speed consistently ~46 tokens/sec

Multi-model pipeline ran smoothly without issues

cuBLAS/cuBLASLt confirmed active, accelerating GEMM operations

🎯 Conclusion
Even on a mid-range GPU like the RTX 2060 SUPER, it's totally possible to reliably run an 8B LLM (4bit) together with an emotion analysis model in a pipeline setup at the same time.

Honest thoughts as a non-expert:

Way better performance than I expected from my "old" GPU

Korean language understanding is surprisingly good

The emotion detection accuracy is scary good (it even caught my deadline stress lol)

VRAM usage is pretty much maxed out (can't game while this is running)

Electricity bill concerns are real 😅

If anyone has tested similar setups on 2060/2070-class GPUs, I'd love to hear your results! 🙂

P.S. Living in a world where AI can detect my deadline anxiety... where are we headed? 😅

### **Contact Info**

* 📧 **Email**: pkc0412@gmail.com  
* 🌐 **Blog**: https://pkcproject.blogspot.com/  
* 💬 **GitHub**: (The repository will be public soon\!)