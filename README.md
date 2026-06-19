# NLP / LLM from scratch

Calling an API is easy. I wanted to know what happens underneath it.

So I sat down and implemented the modern NLP and LLM stack from first principles. Not to reinvent it. To understand it well enough that nothing about a model feels like magic. This is the result: 45 runnable notebooks, from a regex tokenizer to RLHF.

There are two packs.

## 1. NLP implementation (13 notebooks)

The arc from classic NLP to transformers, one technique at a time. You build each thing, run it on small data, and see why the next thing exists.

- Tokenization, regex, lexicon sentiment
- TF-IDF with Naive Bayes, logistic regression, SVM
- N-gram language models, smoothing, perplexity
- Word2Vec / GloVe embeddings and semantic search
- Sequence tagging: HMM, Viterbi, CRF, BiLSTM
- Neural text classification in PyTorch (BiLSTM, CNN)
- Attention and a tiny Transformer, written by hand
- BERT / GPT / T5 with Hugging Face
- Pretraining, fine-tuning, LoRA, SFT, DPO
- Summarization, QA, a RAG skeleton, ROUGE and faithfulness checks
- Machine translation, decoding (greedy, top-k, top-p, beam), BLEU
- Product evals: annotation, Cohen's kappa, PII redaction, monitoring

## 2. Advanced LLM systems (32 notebooks)

The systems layer. How a modern LLM is actually built, served, and kept honest.

- Tokenizers, embeddings, RoPE / ALiBi, attention, multi-head attention
- Transformer blocks, training a mini-former, sampling, speculative decoding
- KV cache, MQA / GQA / MLA, long context, FlashAttention, hardware budgets
- Mixture of experts, sparse and state-space models, diffusion LMs
- Synthetic data, scaling laws, SFT / DPO / RLHF / GRPO, quantization, serving
- Eval harnesses, RAG, tool use and agents, vision-language adapters, interpretability
- Red-teaming, and a capstone that wires it together

## The point

I'm a PM now, but I don't want to manage what I can't reason about. Building these meant I can sit in a room and argue about context windows, eval design, or why a model hallucinates, from the implementation up, not from a blog post.

## Running it

Most notebooks run on a CPU with toy data and no model downloads. Heavy production pieces (FlashAttention kernels, vLLM serving, full RLHF) ship as small teaching versions plus production templates you can grow into.

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
# open the notebooks in order
```

Every code cell parses clean. The classic notebooks run end to end. The heavy ones need their own GPU setup.

## Honest caveats

These are teaching implementations and reusable templates, not a certified production system. Before you point any of this at real data, do your own security, privacy, and domain evaluation.
