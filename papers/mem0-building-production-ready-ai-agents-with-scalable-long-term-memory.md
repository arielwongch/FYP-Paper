# Mem0

## Summary
evaluated on LOCOMO against:
1. established memory-augmented systems
2. retrieval-augmented generation (RAG) with varying chunk sizes and k-values
3. a full-context approach that processes the entire conversation history
4. an open-source memory solution
5. a proprietary model system
6. a dedicated memory management platform.

phrase 1: extraction
1. a conversation summary S retrieved from the database that encapsulates the semantic content of the entire conversation history
2. a sequence of recent messages {mt−m,mt−m+1, ...,mt−2} from the conversation history
3. new message pair (mt−1,mt)
forms a comprehensive prompt P = (S, {mt−m, ...,mt−2},mt−1,mt) for an extraction function ϕ implemented via an LLM

LLM itself determines which of four distinct operations to execute: 
1. ADD for creation of new memories when no semantically equivalent memory exists;
2. UPDATE for augmentation of existing memories with complementary information; 
3. DELETE for removal of memories contradicted by new information; 
4. NOOP when the candidate fact requires no modification to the knowledge base

Mem0g
memories are represented as a directed labeled graph G = (V, E, L), where:
• Nodes V represent entities (e.g., Alice, San_Francisco)
• Edges E represent relationships between entities (e.g., lives_in)
• Labels L assign semantic types to nodes (e.g., Alice - Person, San_Francisco - City)

entity extractor
relationship generator

LLM-as-a-Judge

## Evaluation

Dataset: LOCOMO

Benchmark
1. F1 
2. BLEU1
other: ROUGE-L, ROUGE-2, METEOR, and SBERT Similarity

Compared Framework:
LOCOMO ReadAgent MemoryBank MemGPT AMem Mem0