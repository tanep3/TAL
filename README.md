
# TAL (Tree-structured Assembly Language)

🇯🇵 日本語版READMEはこちら: [README_jp.md](./README_jp.md)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15379276.svg)](https://zenodo.org/records/15379276)
[![Paper](https://img.shields.io/badge/PDF-TAL%20Paper-blue)](https://zenodo.org/records/15379276)

## 📖 Overview

"Don't command the AI. Show it how to think."

TAL is a novel prompt methodology that presents structured thinking frameworks for Large Language Models (LLMs).

Instead of imperative commands, TAL serves as an OS-like interface to explicitly design the reasoning process of AI.

---

| ![Conventional Prompt](./img/conventional_prompt_small.png) | ![Powered by TAL](./img/tal_generated_small.png) |
|:-----------------------------------------------:|:------------------------------------:|
| **Conventional Prompt**<br>This image was generated using a typical natural language prompt. The scene, character expressions, and interactions are generally interpreted by the AI, resulting in less precise composition and some ambiguity in character relationships and actions. | [**Powered by TAL**](./img/TAL_tiktok_dance.json)<br>This image was generated using a TAL (Tree-structured Assembly Language) prompt. The characters' positions, emotions, and dynamic interactions are clearly and logically expressed, resulting in a more coherent scene and faithful realization of the intended concept. |

---

## ✨ Features

1. **Provide ways of thinking, not commands** 👉 AI shifts from dictionary-like answers to thought-driven responses.

2. **Structured grammar** With JSON structure, Z-axis, and Vector-axis, ambiguity in prompts is eliminated 👉 AI won’t hesitate 👉 Outputs align more closely with what users expect.

3. **Ghost-axis** enables emotional nuance in AI’s responses 👉 More human-like answers are achieved.

4. **Extend existing useful prompts (e.g., CoT)** 👉 Wrap them in TAL and enhance with additional TAL features.

5. **Modular design** 👉 Create multiple single-function TAL prompts, reuse and combine them to build more complex tasks 👉 [TAL-Libs](https://github.com/tanep3/TAL-Libs)

6. **Flow control (branching, recursion, parallelism)** 👉 Even as prompts, TAL can *program AI’s thinking*.

7. **Meta-language (self-descriptive)** 👉 TAL can be used to generate other TAL code.

8. **TALC compiler available** 👉 Beginners can simply talk to TALC in natural language, and it will internally compile to TAL for AI reasoning.

9. Applicable to diverse AI domains: summarization, dialogue, translation, creative writing, and more.

10. Future potential as a **design language for deep AI control and ethical guardrails**.

---

## 🌐 English Preprint

The English preprint is published on [Zenodo](https://zenodo.org/records/15379276):

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15379276.svg)](https://zenodo.org/records/15379276)

---

## 📚 Documentation Index

### 🚀 Structural explanation of TAL
- 📖 [TAL Blocks Documentation (EN)](docs/TAL_blocks.md)  
- 🔁 [TAL Recursion Guide (EN)](docs/Recursion.md)  
- ⏩ [Parallel Processing in TAL (EN)](docs/Parallel_Processing_in_TAL.md)  

### 🚀 FAQ

- ❓ [FAQ (EN)](docs/FAQ.md)

### 🚀 Vibe Coding Guide

- 🤖 [System Development with TAL (EN)](docs/TALC_for_System_Manual.md)

### 🚀 TALOS: The world's first prompt OS for AI

- 🧠 [TALOS Installation & Usage Guide (EN)](docs/README_TALOS.md)

---

## 🤖 TAL Compiler (TALC)

A public GPTs-based tool named TALC (TAL Compiler) is available here:  
➡️ [TALC](https://chatgpt.com/g/g-67f90502ff0c819199365f5bd3703e51-talc-tal-compiler)  

You can use TALC to generate TAL prompts easily, and also to ask questions about the TAL framework itself.  
It serves as both a prompt generator and an interactive guide to TAL's core concepts.  

---

## 🧩 TAL-Libs — Thinking Module Collection

[TAL-Libs](https://github.com/tanep3/TAL-Libs) is an official collection of **single-function thinking modules** written in TAL.  
By combining these modules, you can give AI *ways of thinking* rather than commands, and design complex cognitive processes with ease.  
For detailed explanations and composition examples, please see the README in the TAL-Libs repository.  

---


## 💬 Discussions

Discussions are open for your thoughts, feedback, ideas, and use-cases related to TAL.

➡️ [GitHub Discussions](https://github.com/tanep3/TAL/discussions)

---

## 🙌 Contributions

Feel free to open issues or pull requests. Feedback and suggestions are welcome!  
We're happy to welcome contributions such as improvements, new syntax ideas, or bug fixes.  

➡️ [GitHub Issues](https://github.com/tanep3/TAL/issues)  
➡️ [Pull Requests](https://github.com/tanep3/TAL/pulls)  

---

## 📚 Learn More about TAL 

### 🌍 English Article on Medium  
📝 [Medium (EN)](https://tanep3.medium.com/)

TAL is a prompt OS that gives AI structured thought instead of commands. This article introduces the idea in English with clear logic and practical examples.

---

### 🌸 Japanese Blog  
📝 [Official Blog (JP)](https://tanep.work/tanech/)

---

## 👤 Author

Tane Channel Technology

➡️ [x.com/tanep3](https://x.com/tanep3)

---

## ⚖️ License

This project is licensed under **CC BY 4.0 (Attribution)**.  
➡️ https://creativecommons.org/licenses/by/4.0/