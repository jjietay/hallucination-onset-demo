# Hallucination Onset Demo

Live demo: https://jjietay.github.io/hallucination-onset-demo/

This page shows how we find the token where a language model starts to hallucinate. SmolLM2-1.7B writes an answer to a question. A BiLSTM-CRF tagger reads the model's hidden states and tags each token:

- `O`: the token is safe.
- `B-HALL`: the hallucination begins at this token (the onset).
- `I-HALL`: the hallucination continues.

The page then compares the tagger's output with the labels.

The demo is recorded. All questions and outputs come from an earlier saved run, and no model runs live.
