# Validation

What I checked before publishing this pack.

- 32 notebooks, grouped into seven batches.
- Every code cell is parsed with Python `ast.parse`: zero syntax errors.
- Code cells run in a fresh namespace per notebook on the local runtime, on toy, CPU-friendly data.
- Shared setup logic lets a notebook run from the pack root or from a nested folder.

## Caveats

- The heavy production pieces (FlashAttention kernels, vLLM/TensorRT-LLM serving, TRL post-training, PEFT/LoRA at scale, external vector databases) ship as teaching versions plus templates. They need their own GPU and runtime to run for real.
- The red-team examples are sanitised and defensive. Expand them with your own policy and security review before any production use.
- This is an educational starting point, not a certified production system.
