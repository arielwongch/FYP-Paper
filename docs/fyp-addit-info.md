1. Successful FYP and final product

Core (must-have): a modular agent framework with at least four interchangeable memory modules (sliding-window, summarization, retrieval-based, structured fact), plus a systematic evaluation on long-horizon or multi-session tasks covering both task quality (recall, consistency, knowledge updating, task success) and system behavior (latency, retrieval overhead, storage growth).

Stretch (depending on progress, not required): a lightweight adaptive memory strategy that decides when to write, summarize, or retrieve, and/or a memory compaction component that reduces redundancy in long-term storage.

The primary deliverables are the FYP thesis (with thorough experimental results) and the supporting codebase.

2. How much study before building

Iteratively, with rough phasing. Sep to Dec: literature review, framework design, baseline modules. Jan to Feb: complete the evaluation pipeline and run baseline comparisons. Mar to Apr: design the adaptive strategy informed by observed pain points in the baselines, finalize the thesis. You don't need a perfect understanding before starting. Once baselines run end to end on one benchmark, you are ready to prototype the adaptive part.

3. Preferred LLM

I recommend Qwen models under 8B as the primary backbone, served locally with vLLM if GPU is available. We can finalize compute arrangements once you officially join.

4. Recommended papers

Start with the latest survey: Hu et al., "Memory in the Age of AI Agents: A Survey on Forms, Functions and Dynamics" (https://arxiv.org/pdf/2512.13564, Jan 2026). The accompanying GitHub paper list (https://github.com/Shichun-Liu/Agent-Memory-Paper-List) is also useful.

Foundational systems such as MemGPT, Generative Agents, and MemoryBank shaped much of the current thinking on LLM agent memory and are well worth reading for context, while more recent peer-reviewed work like A-MEM (NeurIPS 2025, arXiv:2502.12110) provides a closer design reference for this project; open-source systems such as Mem0 (https://arxiv.org/abs/2504.19413), Zep (https://arxiv.org/abs/2501.13956), and MIRIX (https://arxiv.org/abs/2507.07957) are useful as practical engineering references. For evaluation, recommended benchmarks are LoCoMo (ACL 2024, https://arxiv.org/abs/2402.17753), LongMemEval (ICLR 2025, https://arxiv.org/abs/2410.10813), and MemoryAgentBench (ICLR 2026, https://arxiv.org/abs/2507.05257).

5. Does the adaptive strategy need to be completely new?

No. A principled adaptation or combination of existing ideas, motivated by concrete observations from your baseline experiments and rigorously evaluated against them, is a perfectly good FYP-scale contribution. Novelty for an FYP comes more from careful experimental insight than from a brand-new architecture.