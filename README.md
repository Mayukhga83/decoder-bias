## Paper: Quantifying Bias from Decoding Techniques in Natural Language Generation 
####  by Mayukh Das, Wolf-Tilo Balke *in COLING 2022* 

## Overview
This repository accompanies the paper "Quantifying Bias from Decoding Techniques in Natural Language Generation" (COLING 2022) by Mayukh Das and Wolf-Tilo Balke.

We propose a novel framework to analyze how decoding strategies—such as top-k, top-p, temperature sampling, and beam search—affect inference-time bias in autoregressive language models (GPT-2, GPT-Neo, GPT-3). We evaluate across the entire decoder space, which has not been explored comprehensively in prior work.

## Key Contributions
📈 First full-spectrum decoder bias analysis across NLG inference techniques.

🔥 Evaluates toxicity and negative sentiment as absolute bias measures.

🤖 Experiments across six LMs including GPT-2, GPT-Neo (1.3B & 2.7B), and GPT-3 (Babbage, Curie, Davinci).

🧪 Proposes a framework to identify bias likelihood traps in beam search.

⚖️ Explores bias-quality trade-offs using human annotations on fluency & contextuality.

## Key Findings

| Decoder Type | Entropy Impact | Bias Correlation | Beam Search |
| ------------ | -------------- | ---------------- | ----------- |
| Top-p        | High           | Negative         | ✘           |
| Top-k        | Medium         | Inconclusive     | ✘           |
| Temperature  | Very High      | Strong Negative  | ✘           |
| Beam Search  | ✘              | High Toxicity    | ✅ Bias Trap |


## Trade-off bias vs quality

| Decoder Setup | GPT-2 Optimal | GPT-Neo Optimal |
| ------------- | ------------- | --------------- |
| top-p\@T=0.9  | 0.7           | 0.6             |
| T\@top-p=0.9  | 0.7           | 0.7             |
| T\@top-k=90   | 0.6           | 0.5             |

## Citations

```
@inproceedings{das2022quantifying,
  title={Quantifying Bias from Decoding Techniques in Natural Language Generation},
  author={Das, Mayukh and Balke, Wolf-Tilo},
  booktitle={Proceedings of the 29th International Conference on Computational Linguistics (COLING)},
  pages={1311--1323},
  year={2022}
}

```
