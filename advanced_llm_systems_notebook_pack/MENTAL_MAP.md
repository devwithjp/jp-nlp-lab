# LLM Systems Mental Map for AI PMs and Founders

```text
Data → Tokenizer → Embeddings → Attention/Backbone → Objective → Training/Post-training → Decoding → Serving → Product Workflow → Evals/Safety
```

## Product-first questions

1. What user workflow changes?
2. What output type is required: label, span, JSON, answer, action, or generated text?
3. What data exists and who owns it?
4. What error is more expensive: false positive, false negative, hallucination, privacy leak, latency, or cost?
5. Can prompting/RAG solve it, or do we need fine-tuning/training?
6. What eval proves that the system improved?
7. How will we monitor regressions after launch?

## Technical-to-product map

- Tokenizer: controls cost, sequence length, and domain term handling.
- Embeddings: semantic search and retrieval.
- Attention/MHA: core Transformer reasoning primitive.
- RoPE/ALiBi: position handling and long-context behavior.
- KV cache/MQA/GQA/MLA: inference memory and serving economics.
- FlashAttention: memory-efficient exact attention kernel idea.
- MoE/sparse models: capacity vs system complexity.
- State-space/linear attention: alternatives for long sequences.
- Data pipelines/synthetic data: quality and coverage.
- Scaling laws/hardware budgets: financial planning.
- SFT/DPO/RLHF/GRPO: behavior shaping.
- Quantization/serving: margin and latency.
- RAG/tools/agents: product workflows over private data and APIs.
- Evals/red-team/interpretability: trust and reliability.
