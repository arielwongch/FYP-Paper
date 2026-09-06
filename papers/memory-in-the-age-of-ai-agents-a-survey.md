memory frameworks that distill reusable tools from past experiencesmemory-augmented test-time https://arxiv.org/abs/2506.14728, https://openreview.net/forum?id=Pc8AU1aF5e

memory-augmented test-time scaling methods https://arxiv.org/abs/2504.15965, https://arxiv.org/abs/2504.07952

Memory Lifecycle: Formation, Evolution, and Retrieval The dynamics of the memory system are characterized by three conceptual operators.
Memory Formation At time step t, the agent produces informational artifacts ϕt, which may include tool outputs, reasoning traces, partial plans, self-evaluations, or environmental feedback. A formation operator
Mformt+1 = F(Mt, ϕt)
selectively transforms these artifacts into memory candidates, extracting information with potential future utility rather than storing the entire interaction history verbatim.
Memory Evolution Formed memory candidates are integrated into the existing memory base through an
evolution operator
Mt+1 = E(Mformt+1 ),
which may consolidate redundant entries (Zhao et al., 2024), resolve conflicts (Rasmussen et al., 2025; Li et al., 2025l), discard low-utility information (Wang et al., 2025r), or restructure memory for efficient retrieval.
The resulting memory state persists across subsequent decision steps and tasks.
Memory Retrieval When selecting an action, agent i retrieves a context-dependent memory signal
mi
t = R(Mt, oit,Q),
where R denotes a retrieval operator that constructs a task-aware query and returns relevant memory content.
The retrieved signal mit is formatted for direct consumption by the LLM policy, for example as a sequence of textual snippets or a structured summary.

e.g., LLM-based agent = LLM + reasoning + planning + memory + tool use
+ self-improvement + multi-turn interaction + perception, as discussed by Zhang et al. (2025f)),

HippoRAG/HippoRAG2 (Gutierrez et al., 2024; Gutiérrez et al., 2025) have been interpreted
by both RAG and memory communities as addressing long-term memory challenges for LLMs

Representative benchmarks include long-context dialogue evaluations such as LoCoMo (Maharana et al., 2024) and LongMemEval (Wu et al., 2025a), complex problem-solving and deep-research benchmarks such as GAIA (Mialon et al., 2023), XBench (Chen et al., 2025c), and BrowseComp (Wei et al., 2025b), code-centric agentic tasks such as SWE-bench Verified (Jimenez et al., 2024), as well as lifelong learning benchmarks such as StreamBench (Wu et al., 2024a). We provide a comprehensive summary of memory-related benchmarks in Section 6.1.

token pruning and importance-based selection methods (Jiang et al., 2023; Li et al., 2023c) that are central to context engineering frameworks play a fundamental role in agentic memory systems by filtering noise and retaining salient information.

