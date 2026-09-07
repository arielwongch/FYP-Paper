Next paper to read: Mem0, MemGPT

Zettelkasten method: note taking system (memory treat as nodes, connected by links, similarto hyperlinks)

new memories automatically trigger two key operations: link generation and memory evolution

The system’s design emphasizes atomic note-taking,flexible linking mechanisms,and continuous evolution of knowledge structures.

LoCoMo dataset [22], which contains significantly longer dialogues compared to existing conversational datasets

competitive baseline: LoCoMo[22],ReadAgent [17],MemoryBank[39], andMemGPT

t-SNE visualization in Figure4 of memory embeddings to demonstrate the structural  advantages of our agentic memory system


# Summary
Zettelkasten method: note taking method, treat memory as graph[distinct memory as node, relations as link]
utilize LLM for memory formation: gpt-4o-mini -> link generation & memory evoluation
memory note construction, metadata: category, description, links (text encoder A)
link generation: top k -> LLM rerank & generate
retrival: text encoder A, cosine similarity
https://dialsim.github.io/ question-answering dataset derived from long-term multi-party dialogues.
BLEU-1 [26] provides a method for evaluating the precision of unigram matches between system
outputs and reference texts: