# Requirements / Verification — Version 0.11

添付仕様は第29章の末尾まで受領・確認しました。各章の対応は以下のとおりです。実装状況とブラウザ検証の範囲は分けています。

| 章 | 要件 | 対応 |
|---|---|---|
| 1–2 | 既存設計維持・3変更に限定 | v0.1をコピーして別版を作成。Macro / Micro / Compare / Overlay等を維持 |
| 3 | 整数表示 | 画面・Inspector・入力欄・比較・要約を整数表示 |
| 4 | Drag Snap・数値型 | 座標操作を整数化、保存値は数値 |
| 5 | JSON互換 | 0.1 / 0.11対応。旧小数の位置を明示編集まで保持 |
| 6 | 両軸の名前維持 | X / Yとも旧版の文字列を保持 |
| 7–8 | 0 / 25 / 50 / 75 / 100 | 両軸10 Anchor、英語名＋日本語運用説明 |
| 9 | Guide UI | MacroのAxis Guide、Calibration Inspector内にも入口 |
| 10 | Human Calibration | 自動計算なし。Guide内に人間による調整と明記 |
| 11 | 初期座標維持 | 6作品すべて完全一致を検証 |
| 12 | Note | 自由記入を維持。直前／現在／初期、保存日時、Reason / Anchor / Session記入案内 |
| 13–14 | Microの4 Edge | Primary / Coupling / Constraint / Aggregationを線と記号で区別 |
| 15 | Operator維持 | + / − / × / ▶︎の意味を維持 |
| 16 | 各作品のEcology | 指定関係を補足。Closerの元Node / Edgeは変更なし |
| 17 | Legend | 4種類をフル表記、線・記号・矢印を併用 |
| 18 | Progressive Disclosure | Overviewでは補助線を弱め、Relation種別フィルターで絞る |
| 19 | Centre Dissolution | GuideにWorking Hypothesisとして掲載。Score化しない |
| 20 | Evidence Interface維持 | 6作品の原語・情報を旧版と完全一致確認 |
| 21 | 作品追加禁止 | 6作品のみ |
| 22 | 採点変更禁止 | Element / Class / Scoreの追加・推定・再計算なし |
| 23 | Regression | 22自動検証通過。Safari実機範囲はVerification-Notes.mdに限定記載 |
| 24 | Readability | 線種・矢印・記号・テキスト併用。Guideに説明 |
| 25 | ファイル | 指定名の単体HTML、内蔵Dataset、別途data.json |
| 26 | Design Notes | 3変更とfalse precision / 反証可能性 / linear誤読対策を説明 |
| 27 | 成功条件 | 対応する構造を実装。理解向上は共同検討で検証する課題 |
| 28 | 完成物 | HTML、Dataset、設計メモ、照合表、差分、検証記録を同梱 |
| 29 | Research Integrity優先 | 仮説と測定を分離し、旧版を保持、共有可能な小規模改訂として提供 |

## 研究者が次に確認すること

同じ場面・Evidenceを使ってGuideを参照し、変更理由をNoteに残します。別の研究者のHTML / JSONと比較し、座標差が観察差・Anchor解釈差・モデルの不足のどこから生じたか検討してください。値を合わせること自体を目的にせず、反証可能な理由を共有するための版です。
