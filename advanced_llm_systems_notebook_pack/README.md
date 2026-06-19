# Advanced LLM Systems Implementation Notebook Pack

This pack contains 32 implementation notebooks for learning modern NLP/LLM systems from first principles and turning them into company or portfolio projects.

## Structure: five topics at a time

The notebooks are grouped into batches of five topics so you can study them in loops:

### Batch 01 — Foundations: tokens, embeddings, attention
1. Build a tokenizer
2. Learn embeddings
3. Implement RoPE / ALiBi
4. Hand-wire attention
5. Build MHA

### Batch 02 — Transformer and decoding
6. Build a Transformer block
7. Train a mini-former
8. Compare objectives
9. Build sampling
10. Speculative decoding

### Batch 03 — Inference memory and long-context efficiency
11. KV cache
12. MQA / GQA / MLA
13. Long context
14. FlashAttention
15. Hardware budgets

### Batch 04 — Sparse and alternative architectures + data pipeline basics
16. Toy MoE
17. Sparse model trade-offs
18. State-space / linear attention
19. Diffusion language models
20. Data pipelines

### Batch 05 — Data, scaling, post-training, deployment economics
21. Synthetic data
22. Scaling laws
23. SFT / DPO / RLHF / GRPO
24. Quantization
25. Serving stacks

### Batch 06 — Product system layer
26. Eval harnesses
27. RAG
28. Tool use / agents
29. Vision-language adapters
30. Interpretability

### Batch 07 — Safety and capstone
31. Red-team suite
32. Full capstone model system

## How to use

1. Create a fresh environment.
2. Install requirements: `pip install -r requirements.txt`.
3. Start with notebook 01 and run each notebook in order.
4. For portfolio work, fork a notebook into a new project and replace the toy data with real or domain-specific data.
5. For company work, add evals and privacy review before connecting production data.

## Design choices

- Most notebooks are runnable locally on CPU with toy data.
- Heavy production topics are implemented as small teaching versions plus production templates.
- No notebook requires external model downloads by default.
- Production extras such as `transformers`, `peft`, `trl`, `bitsandbytes`, `vllm`, and vector databases are listed as optional.

## Suggested capstone projects

- Internal policy RAG assistant with citations and red-team suite.
- Support-ticket classifier + synthetic data generator + eval harness.
- Tiny GPT from scratch with tokenizer, sampling, KV cache, and dashboard.
- MoE routing visualization app.
- Quantization and serving-cost calculator for model selection.
- Tool-using AI PM assistant that can retrieve docs, calculate budgets, and produce structured PRDs.

## Consolidated references

- RoPE: RoFormer / Rotary Position Embedding, arXiv:2104.09864.
- ALiBi: Train Short, Test Long, arXiv:2108.12409.
- FlashAttention: Dao-AILab FlashAttention repository and papers.
- GQA: Grouped-Query Attention, EMNLP 2023 / arXiv:2305.13245.
- MLA: DeepSeek-V2 paper, arXiv:2405.04434.
- Mamba/state-space models: Linear-Time Sequence Modeling with Selective State Spaces, arXiv:2312.00752.
- MoE: Switch Transformers, JMLR/arXiv:2101.03961.
- Scaling laws: Kaplan et al. 2020; Chinchilla / Hoffmann et al. 2022.
- RAG: Hugging Face Transformers RAG docs.
- Tool use: OpenAI function calling and tools docs.
- PEFT/LoRA/quantization: Hugging Face PEFT and Transformers quantization docs.
- DPO/GRPO/RLHF templates: Hugging Face TRL docs.
- Serving: vLLM and NVIDIA TensorRT-LLM docs.
- Evals/red-team: OpenAI Evals, EleutherAI lm-evaluation-harness, Inspect AI, and NVIDIA garak.
- Interpretability: TransformerLens documentation.
- Vision-language adapters: LLaVA / Visual Instruction Tuning.

## Caveats

These notebooks are educational and reusable templates. They are not a substitute for production security review, legal review, privacy review, or domain-specific evaluation.
