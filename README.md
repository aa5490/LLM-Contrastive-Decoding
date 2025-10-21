# LLM-Contrastive-Decoding
This repo contains a clean, reproducible implementation of **Contrastive Decoding** for open‑ended text generation (Li et al. referenced). It demonstrates how contrasting an **expert** LM against an **amateur** LM improves coherence and specificity while suppressing generic, high‑probability but uninformative continuations.

The core notebook is: **`LLMsContrastiveDecoding.ipynb`**.

---

## What’s inside

- **Contrastive decoding** between two Hugging Face causal LMs (e.g., `gpt2-xl` as *expert* and `gpt2` as *amateur*).
- A small evaluation harness over prompts with the following metrics:
  - **Perplexity** (fluency proxy)
  - **MAUVE** (distributional distance for quality/diversity)
  - **Distinct‑n** (lexical diversity, n‑gram uniqueness)
- Clear, modular functions so you can plug in different models/datasets.
