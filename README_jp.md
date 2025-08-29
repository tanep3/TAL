
# TAL (Tree-structured Assembly Language)

🌍 English README is available here: [README.md](./README.md)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15379276.svg)](https://zenodo.org/records/15379276)
[![Paper](https://img.shields.io/badge/PDF-TAL%20Paper-blue)](https://zenodo.org/records/15379276)

## 📖 概要

「AIに命令するな。考え方を示せ。」  

**TAL（Tree-structured Assembly Language）** は、大規模言語モデル（LLM）における**思考フレームワークを構造的に提示するプロンプト手法**です。  

従来の命令型プロンプトではなく、**AIの推論プロセスそのものを明示的に設計**できるOS的インターフェースを目指しています。  

---

| ![従来プロンプト](./img/conventional_prompt_small.png) | ![Powered by TAL](./img/tal_generated_small.png) |
|:-----------------------------------------------:|:------------------------------------:|
| **従来のプロンプト**<br>この画像は、一般的な自然言語プロンプトで生成されました。シーンやキャラクターの表情、やり取りなどはAIによる解釈に任されるため、構図が曖昧になったり、キャラクター同士の関係性や動きに不明瞭さが残ることがあります。 | [**Powered by TAL**](./img/TAL_tiktok_dance.json)<br>この画像は、TAL（ツリー構造アセンブリ言語）プロンプトで生成されました。キャラクターの位置や感情、動的なやり取りが明確かつ論理的に表現され、シーン全体が一貫性をもって意図通りに再現されています。 |

---

## ✨ 特徴

1. **命令ではなく考え方をAIに与える** 👉️AIが辞書的応答から思考した応答に変化する  

2. **構造化された文法** JSON構造、z軸、Vector軸により、プロンプトの曖昧さを排除 👉️AIが回答を迷わない 👉️人が求める出力が得られる  

3. **Ghost軸**により、AIの応答に感情を盛り込める 👉️人間的な回答を得られる  

4. **既存のCoT等の有益なプロンプトをラッピング拡張できる** 👉️有益プロンプトにTALの他の機能で拡張できる  

5. **TALはモジュール化できる** 👉️単機能のTALプロンプトを複数つくって、それらを再利用して組み合わせて、より複雑なタスクを作れる 👉️[TAL-Libs](https://github.com/tanep3/TAL-Libs)  

6. **フロー制御（条件分岐、再帰、並列処理）ができる** 👉️プロンプトでありながら、AIの思考をプログラミングできる  

7. **メタ言語である（自己記述性がある）** 👉️TALを使って別のTALを生成できる  

8. **TALCコンパイラを提供している** 👉️初心者でも知識不要でTALCに自然言語で話しかけるだけで、内部的にTALでAIが思考するようになる  

9. 要約、対話、翻訳、創作など、**多様なAI活用領域にTALを適用可能**  

10. 将来的には、**AIの深層制御や倫理的ガードレールの設計言語**としての拡張も期待される  

---

## 📝 日本語論文 PDF

➡️ [TAL 日本語論文 PDF](https://raw.githubusercontent.com/tanep3/TAL/main/docs/tal_paper_jp.pdf)

---

## 🌐 英語版プレプリント

Zenodoにて英語版が公開されています：  

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15379276.svg)](https://zenodo.org/records/15379276)

---

## 📚 ドキュメント一覧

### 🚀 TALの構造説明
- 📖 [TAL Blocks 解説書 (JP)](docs/TAL_blocks_jp.md)  
- 🔁 [再帰構文設計ガイド (JP)](docs/Recursion_jp.md)  
- ⏩ [TALにおける並列処理 (JP)](docs/Parallel_Processing_in_TAL_jp.md)  

### 🚀 FAQ

- ❓ [FAQ（よくある質問）(JP)](docs/FAQ_jp.md)  

### 🚀 バイブコーディング（AIを使ったシステム開発）ガイド

- 🤖 [TALによるシステム開発ガイド (JP)](docs/TALC_for_System_Manual_jp.md)

### 🚀 世界初のAIのためのプロンプトOS・TALOS解説

- 🧠 [TALOSの導入と使い方 (JP)](docs/README_TALOS_jp.md)

---

## 🤖 TALコンパイラ（TALC）

ChatGPTのGPTsにて、TALC（TALコンパイラ）公開中！  
➡️ [TALC](https://chatgpt.com/g/g-67f90502ff0c819199365f5bd3703e51-talc-tal-compiler)  

TALCを使えば、TALプロンプトを簡単に生成できます。  
またTALCは、TALについての疑問もその場で解決できる、対話型マニュアルとしても機能します！  

---

## 🧩 TAL-Libs — 思考モジュール集

[TAL-Libs](https://github.com/tanep3/TAL-Libs) は、TALで記述された **単機能の思考モジュール集** です。  
モジュールを組み合わせることで、AIに「命令」ではなく「考え方」を与え、複雑な思考プロセスを自在にデザインできます。  
詳細な説明と合成例は、TAL-LibsのREADMEをご覧ください。  

---

## 💬 ディスカッション

TALについての感想・活用事例・構文案・疑問など、なんでも気軽に話せる場所を開設しました。  

🗣 こちらから参加できます！  
➡️ [GitHub Discussions](https://github.com/tanep3/TAL/discussions)

---

## 🙌 コントリビューション

Issue・Pull Request歓迎です！質問や提案がある方もお気軽にどうぞ。  
構文の改善・追加・バグ修正・構文テンプレートの共有など、貢献も大歓迎です！  

✍️ Issue投稿やPRはこちら：  
➡️ [GitHub Issues](https://github.com/tanep3/TAL/issues)  
➡️ [Pull Requests](https://github.com/tanep3/TAL/pulls)  

---

## 📚 TALをもっと知りたい方へ

### 🌸 日本語ブログ（たねちゃんねるテクノロジー WEB版）  
📝 [Official Blog (JP)](https://tanep.work/tanech/)

TAL（Tree-structured Assembly Language）について、日本語で丁寧に解説しています。

---

## 👤 著者

たねちゃんねるテクノロジー / Tane Channel Technology

➡️ [x.com/tanep3 (旧 Twitter)](https://x.com/tanep3)

---

## ⚖️ ライセンス / License

本プロジェクトは **CC BY 4.0（表示-継承）** ライセンスで公開されています。  
➡️ https://creativecommons.org/licenses/by/4.0/