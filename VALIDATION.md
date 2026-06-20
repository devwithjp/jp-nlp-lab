# Validation

Notes on what I checked before publishing, so you can trust the code runs.

- 45 notebooks across the two packs (13 NLP implementation, 32 advanced LLM systems).
- Every code cell is parsed with Python `ast.parse`: 232 cells, zero syntax errors.
- The classic notebooks run end to end in a fresh namespace, on CPU, with toy data and no model downloads.
- Shared setup logic lets a notebook run from the pack root or from a nested folder.

## Caveats

- The heavy production pieces (FlashAttention kernels, vLLM/TensorRT-LLM serving, full TRL post-training, PEFT/LoRA at scale, external vector databases) ship as small teaching versions plus templates. They need their own GPU and runtime to run for real.
- The red-team examples are sanitised and defensive. Expand them with your own policy and security review before any production use.
- These are teaching implementations and reusable starting points, not a certified production system.
