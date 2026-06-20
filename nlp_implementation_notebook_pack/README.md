# NLP Implementation Notebook Pack

Implementation notebooks for the major NLP techniques, from rule-based tokenization to product evals. Each one runs on toy data and is easy to adapt to your own.

## How to use

1. Open the notebooks in order if you are revising concepts.
2. For a portfolio project, pick one business use case and adapt notebooks 00, 02, 10, and 12 first.
3. For a company prototype, start with a cheap baseline, build an eval set, then decide whether prompting, RAG, fine-tuning, or LoRA is needed.

## Notebook map

| Notebook | Covers |
|---|---|
| 00_project_setup_data_strategy | Data audit, splits, metrics, model card, approach decision tree |
| 01_rule_based_tokenization_regex_lexicon | Tokenization, regex extraction, lexicon sentiment, precision/recall |
| 02_statistical_text_classification_tfidf_ml | TF-IDF, Naive Bayes, logistic regression, SVM, thresholding, model saving |
| 03_language_modeling_ngrams_smoothing_perplexity | N-grams, add-k smoothing, interpolation, perplexity, generation |
| 04_embeddings_word2vec_glove_similarity | One-hot, co-occurrence/SVD, Word2Vec, semantic search baseline |
| 05_sequence_tagging_hmm_crf_bilstm_ner_pos | BIO tagging, HMM, Viterbi, CRF template, BiLSTM tagger |
| 06_neural_text_classification_rnn_lstm_cnn_pytorch | PyTorch text datasets, embeddings, BiLSTM classifier, CNN classifier |
| 07_attention_transformer_from_scratch_pytorch | Q/K/V attention, multi-head attention, positional encoding, tiny causal Transformer |
| 08_transformers_huggingface_bert_gpt_t5_tasks | BERT/GPT/T5 use cases, pipelines, fine-tuning templates, token classification |
| 09_pretraining_finetuning_peft_lora_posttraining | Pretraining lifecycle, LoRA from scratch, PEFT template, prompt tuning, SFT, DPO |
| 10_summarization_qa_rag_evaluation | TextRank, TF-IDF retrieval, RAG skeleton, extractive QA, ROUGE-L, faithfulness checks |
| 11_machine_translation_decoding_bleu_rouge_metrics | Toy MT, greedy/sampling/top-k/top-p/beam search, BLEU, generation controls |
| 12_product_evals_annotation_safety_monitoring | Cohen's kappa, eval buckets, output validation, PII redaction, monitoring scorecard |

## Data

The `data/` directory contains tiny toy datasets:

- `sample_customer_tickets.csv`
- `toy_ner.jsonl`

Replace these with your own company/project data.

## Suggested environment

Core notebooks use common Python libraries: numpy, pandas, scikit-learn, torch, gensim, spaCy optional.

Transformer-specific notebooks include templates that may require:

```bash
pip install transformers datasets evaluate accelerate peft sklearn-crfsuite
```

## Portfolio ideas

- Customer complaint intelligence dashboard
- Legal clause risk extractor
- RAG assistant over company docs
- Entity extraction system for invoices/contracts
- Summarisation evaluator with hallucination checks
- Fine-tuned or LoRA-adapted classifier for a niche domain

## Important product principle

Start with the smallest reliable system. Large models are useful, but product quality comes from workflow fit, data quality, evaluation, safety checks, and user trust.