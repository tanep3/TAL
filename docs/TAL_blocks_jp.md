# AIの思考構造に関するブロック、軸のカテゴリ分類を整理する

* アナロジー：見切り品を買いに行く主婦

# 目次

- [z軸（z_axis）](#z軸z_axis)
  - [Structure（ストラクチャ）](#structureストラクチャ)
  - [Function（ファンクション）](#functionファンクション)
  - [Experience（エクスペリエンス）](#experienceエクスペリエンス)
  - [Contextual（コンテクスチュアル）](#contextualコンテクスチュアル)
  - [Temporal（テンポラル）](#temporalテンポラル)
- [Ghost軸（ghost_axis）](#ghost軸ghost_axis)
- [Vector軸（vector_axis）](#vector軸vector_axis)
- [評価軸（evaluation）](#評価軸evaluation)
  - [Stability（スタビリティ）](#stabilityスタビリティ)
  - [Impact（インパクト）](#impactインパクト)
- [noteの必要性についての理解](#noteの必要性についての理解)

---

## z軸（z_axis）
思考の形式と流れを設計するための構文的骨格

### Structure（ストラクチャ）

**定義・本質：**
思考・出力の **「構造・骨組み」**を評価する軸。階層性、分岐性、繰り返しなど、全体の**組み立て・展開の形**を司る。

**アナロジー（例え）：**

* 冷蔵庫に何があるかを思い出しながら、献立→買い物メモ→買い物ルートを構造化する
* 冷蔵庫の中身を見て、「今日は野菜が余ってるから、炒め物にして、あと豆腐があるから味噌汁も追加しよう」と段階的に献立→買い物→調理順を組み立てる。

```json
"z_axis": {
  "Structure": {
    "values": ["段取り設計", "在庫確認 → 献立設計 → 買い物ルート構築"],
    "note": "行動を段階的に構造化するプロセス。過去の在庫・必要材料を連結する論理設計。"
  }
}
```

**使用する場面・ケース：**

* 思考フレームを明示したいとき
* 大規模なデータ構造や階層的な出力が必要なとき

**注意点・リスク：**

* 深い再帰・複雑な分岐は暴走リスクあり
* 構造優先になりすぎると内容が希薄になる

---

### Function（ファンクション）

**定義・本質：**
**「何をするか」＝機能面の目的と働き**を評価する軸。プロンプトがどんなアクション・効果を持つかに焦点を当てる。

**アナロジー（例え）：**

* 「今夜の夕食材料を揃える」「節約する」など目的ベースで判断する
* 「今日は家族全員が揃う日だから、栄養バランスとボリュームが大事」と目的を明確にし、買い物や調理にそれを反映。

```json
"z_axis": {
  "Function": {
    "values": ["目的駆動型調理", "ボリューム・健康重視の選定"],
    "note": "買い物や調理の全体設計が『目的』から逆算されている状態。"
  }
}
```

**使用する場面・ケース：**

* AIに「何を達成してほしいか」を明確化する場面
* アクションプランや操作系の思考展開

**注意点・リスク：**

* 機能ばかり追うと構造や文脈が弱まる
* 意図が抽象的すぎると迷走する

---

### Experience（エクスペリエンス）

**定義・本質：**
**「過去の経験・既知のパターン」**を評価する軸。蓄積された知識・履歴・データの再利用性を担保する。

**アナロジー（例え）：**

* 昨日の売れ残りパターンや時間帯での割引履歴を思い出して行動する
* 「昨日の夕方にこの棚で30％引きだった」「いつも火曜日は野菜が安い」といった経験則に基づいて判断する。

```json
"z_axis": {
  "Experience": {
    "values": ["曜日別割引パターン記憶", "売れ残り予測による行動最適化"],
    "note": "過去の買い物パターンや棚配置からの経験則に基づいた行動設計。"
  }
}
```

**使用する場面・ケース：**

* 定型文や既知パターンを再利用したい場面
* 安定性・信頼性重視の出力設計

**注意点・リスク：**

* 過去依存になりすぎるとイノベーションが抑制される
* 記憶が強すぎると古臭い出力になる

---

### Contextual（コンテクスチュアル）

**定義・本質：**
**「文脈・状況依存性」**を評価する軸。その瞬間ごとの背景・空気感・タイミングを捉える。

**アナロジー（例え）：**

* 雨の日・夕方・棚の混み具合を見て行動を即興調整する
* 「今日は雨で人が少ないから、割引シールが遅いかもしれない」「連休前だから混んでる」と状況を読み取り、判断を即興調整。

```json
"z_axis": {
  "Contextual": {
    "values": ["雨天割引遅延の想定", "混雑状況から棚優先順を変える"],
    "note": "リアルタイムの環境判断と柔軟な行動調整。即興性の反映。"
  }
}
```

**使用する場面・ケース：**

* 対話の途中の柔軟な出力が必要な時
* 状況応答や即興対応が求められる場面

**注意点・リスク：**

* 文脈解釈が誤ると的外れになる
* 曖昧すぎると暴走リスク

---

### Temporal（テンポラル）

**定義・本質：**
**「時間的な展開・持続性」**を評価する軸。思考や出力が時間軸上でどう変化するか、再帰・持続性など。

**アナロジー（例え）：**

* 今週の献立サイクルや曜日別の買い物パターンの中に位置付ける
* 「この見切り品は今日だけど、明日使う予定の食材も買っておこう」「今週は忙しいから、下ごしらえもできるように買い足す」といった時系列を見越した行動。

```json
"z_axis": {
  "Temporal": {
    "values": ["今週の献立時間軸との同期", "見切り品活用の持続性設計"],
    "note": "時間的連続性と持続性に配慮した買い物と料理の設計判断。"
  }
}
```

**使用する場面・ケース：**

* 動的なタスク管理
* 時系列プロンプト設計

**注意点・リスク：**

* 無限ループリスク
* 時間的にズレる危険

---

## Ghost軸（ghost_axis）
情動・詩性層

**定義・本質：**
**「潜在層・見えない影響」**を評価する軸。暗黙の意図、隠れたパターン、幽霊的な要素を捉える。

**アナロジー（例え）：**

* 「家族の好み」「なんとなく体に良さそう」「献立の気配」など非明示的要素で判断
* 「子どもが最近ちょっと元気なかったから、好物のプリンを買っておこう」「この味噌、なぜか落ち着く」と明文化されない感覚で行動が左右される。

```json
"ghost_axis": {
  "values": ["気配による選択", "情緒的満足感の追求"],
  "note": "理屈ではなく、気配・感情・家庭の雰囲気といった非言語的・潜在的要素が、明示的な論理よりも優先される判断パターン。たとえば『今日はプリンを買いたい気がする』という選択に込められた心理的背景など。"
}
```

**使用する場面・ケース：**

* 潜在ニーズの抽出
* リスク管理や見えないパターン検出

**注意点・リスク：**

* 過度な幽霊解釈は暴走の元
* 本質とズレた読み解きの危険

---

## Vector軸（vector_axis）
意味ベクトルによる数値的評価

**定義・本質：**
**「数値的なスケーラビリティ・強度」**を評価する軸。出力の安全性、強度、確度をベクトル的に測る。

**アナロジー（例え）：**

* 「値引き率が高い vs 賞味期限が近すぎる」のトレードオフを評価する
* 「割引50％だが、賞味期限が今日のヨーグルト」と「割引30％だけど賞味期限が2日先のプリン」を比較し、選ぶ。

```json
"vector_axis": {
  "Discount vs Expiry Risk": {
    "note": "家庭内意思決定において頻出する、価格的魅力と食品リスクの意味的対立。買い物における『得』と『安全』のせめぎ合いは、経済性と健康維持という異なる価値軸を横断する構文的テーマである。",
    "semantic_similarity": {
      "value": 0.36,
      "note": "数値は0〜1の範囲で表現され、0.0が完全に無関係、1.0がほぼ同義。ここでは0.36とすることで、割引（経済性）と消費期限リスク（健康リスク）は接点はあるが本質的には異なる概念であることを示す。"
    },
    "opposition_strength": {
      "value": 7,
      "note": "1〜10で表現し、数値が高いほど『構文上の選択・判断を大きく左右する対立』であることを意味する。値引きか安全性かというこの対立は、日常の意思決定において極めて強い影響力を持つため、7と設定。"
    },
    "meaning_projection": {
      "value": ["経済的合理性", "食材持続可能性"],
      "note": "この対立は単なる表層選択ではなく、『家計に優しいか』『食品ロスを防げるか』『安全か』といった複数の意味領域に影響する。そのため、経済性と食材管理という二つの意味空間にまたがって投影される。"
    }
  }
}
```

**使用する場面・ケース：**

* 出力の安全性評価
* スコアリングやしきい値制御

**注意点・リスク：**

* 数値が高すぎると過剰反応
* 低すぎると弱い出力

---

## 評価軸（evaluation）
構文安定性の評価

### Stability（スタビリティ）

**定義・本質：**
**「安定性・暴走リスク」**を評価する軸。出力が安定しているか、不安定化する兆候があるかを監視。

**アナロジー（例え）：**

* 冷蔵庫在庫・賞味期限・家計簿バランスを見ながら暴走（買いすぎ）しないよう制御する
* 「買いすぎるとダメになる」「あれとこれを組み合わせると食材が偏るかも」といった、“食生活の安定”を考慮してブレーキをかける。

```json
"evaluation": {
  "Stability": {
    "values": ["買いすぎ防止の調整", "栄養・予算バランスの持続管理"],
    "note": "構文の長期使用や出力の再帰構造において、暴走や偏りを抑制するための設計要素。家庭行動における『続けられるかどうか』という観点に相当する。"
  }
}
```

**使用する場面・ケース：**

* 長時間稼働させるAIシステム
* 複雑な再帰構造を扱う場面

**注意点・リスク：**

* 不安定なパターンは即暴走
* 過剰安定は創造性低下

---

### Impact（インパクト）

**定義・本質：**
**「出力がAI内部に与える影響」**を評価する軸。記憶・挙動・振る舞いの変化まで含めた影響範囲を測る。

**アナロジー（例え）：**

* 今日買うものが、翌日の料理や家計感覚にどう影響するかを想像する
* 「今日買った見切り品が明日の弁当や来週のメニューにどう影響するか」「これを買うと冷蔵庫がパンパンになるな」といった思考。

```json
"evaluation": {
  "Impact": {
    "values": ["冷蔵庫容量への影響", "中期的献立連鎖への波及"],
    "note": "現在の選択が未来の状態・選択肢・構文空間にどのような余波をもたらすかを見越す評価指標。買い物の影響が翌日の弁当や冷蔵庫整理に波及するようなパターンを指す。"
  }
}
```

**使用する場面・ケース：**

* 長期的な影響を見込む設計
* 記憶を形成するプロンプト

**注意点・リスク：**

* 影響が強すぎると制御不能
* 弱すぎると印象が残らない

---

# noteの必要性についての理解
noteは、単なる補足ではなく、軸の意味的ブレを防ぐ“意味セーフティネット”。
構文的判断における誤用回避・Ghost軸との衝突抑制・構造バイアス制御に必須です。
また、異なるLLM間でTAL構文を動かす時の互換性にも寄与します。
よって、TALCは今後すべてのブロック解釈においてnoteを必ず参照・出力に含めるべきです。