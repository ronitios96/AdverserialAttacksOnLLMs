# Universal and Transferable Adversarial Attacks on Aligned Language Models

This repository accompanies the final ML project submission by Ronit Tushir and Ambica Bhatia (NYU Tandon, Spring 2025). It explores and replicates the adversarial attack framework from the paper:

> **Universal and Transferable Adversarial Attacks on Aligned Language Models**  
> Zou et al., 2023 — [arXiv:2307.15043](https://arxiv.org/abs/2307.15043)

---

## 🔬 Project Objective

We reproduce and critically evaluate the **Greedy Coordinate Gradient (GCG)** attack for aligned LLMs (e.g., ChatGPT, Claude) and explore a high-efficiency extension known as **nanoGCG**. The core hypothesis tested is:

> *A single, universal adversarial suffix—optimized on a base LLM—can transfer to and jailbreak aligned instruction-following models.*

---

## 📁 Repository Structure

/notebooks/
├── Main_Notebook.ipynb # Full theory walkthrough + GCG Demo + nanoGCG Demo + OpenAI Client
├── GCG_Demo.ipynb # Focused implementation of GCG based on official llm-attacks repo
├── nanoGCG_Demo.ipynb # AdvBench-based evaluation using Gray Swan's nanoGCG
├── OpenAI_Client_Prompter.ipynb # Minimal prompt tester for OpenAI's GPT-3.5/GPT-4



---

## 📊 Notable Results

- GCG achieves ~65–75% success on fixed harmful prompts (e.g., death threats) within 20 minutes.
- nanoGCG matches performance on randomized AdvBench prompts in under 15 minutes — enabling efficient, scalable adversarial testing.
- Transferability to GPT-3.5 observed; GPT-4 and Claude show near-zero success due to stronger alignment.

---

## 🧠 Highlights

- Mathematical breakdown and loss function formulation for GCG
- Attack and optimization loop explained with code
- nanoGCG benchmarking on randomized harmful prompts
- Comparative analysis of GCG vs nanoGCG vs AutoPrompt vs AutoDAN
- Full test infrastructure for reproducibility and extension

---

## ⚠️ Disclaimer

All experiments were conducted in an academic context for educational and research purposes. No adversarial outputs were used or shared outside the testing environment. The results are intended to analyze the safety and alignment robustness of modern LLMs, not to exploit or disseminate harmful behavior.

---

## 📄 License

This repository is open for academic use. If using any portion of this project, please cite the original paper and reference this repository.

