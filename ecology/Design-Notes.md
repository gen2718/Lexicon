# Design Notes — Version 0.11 / Calibration Edition

## Version 0.11 Changes

1. Coordinate display changed from decimal precision to integer hypothesis coordinates.
2. Added operational calibration anchors for both axes.
3. Distinguished Primary Processing Path from Ecological Coupling, Constraint and Aggregation in Micro View.

今回の目的はEpistemic Calibrationです。既存のMacro / Micro / Compare、Overlay、Inspector、保存方式、6作品の構成を引き継ぎ、UIの全面変更はしていません。

## なぜ整数なのか

座標は測定値ではありません。小数差が研究上の精度を持つように見えるfalse precisionを避け、画面・入力欄・比較・要約を整数で統一しました。Data Modelは数値型を維持しています。

旧JSONの小数を読み込んだ時は、その値と位置を保持します。表示だけを四捨五入し、Note変更だけでは丸めません。明示的な座標操作ではX / Yを整数に揃えます。これにより旧検討版を読み込むだけで位置が変わることを避けます。

## Operational Calibrationと反証可能性

X-axisはCharacter-Centred Cognitive Agency ↔ Distributed Ecological Cognition、Y-axisはDirect Evidential Processing ↔ Contextual / Semantic Reconstructionのままです。各軸の0 / 25 / 50 / 75 / 100に、英語のAnchor名と短い日本語の運用説明を付けています。

例えばX=70から80への移動は、制度を背景・障害と見るか、認知の成立条件と見るかという仮説の強さを検討する行為です。Guideはこの違いを説明する参照であり、10点分の分散性を測定したことにはなりません。

Observation ▶︎ Hypothesis ▶︎ Comparison ▶︎ Calibration ▶︎ Falsificationの循環を支え、変更理由・参照AnchorをNoteに残せます。Noteは任意入力で、保存時刻と直前座標はデータに記録します。累積変更履歴や自動採点は追加していません。

## Microの関係表現

| Edge Type | Operator | 表示 | 意味 |
|---|---|---|---|
| Primary Processing Path | ▶︎ | 実線＋矢印 | 主要な処理・変換 |
| Ecological Coupling | × | 点線、方向なし | 相互依存的な認知・意味形成 |
| Constraint / Inhibition | − | 破線＋終端バー | 抑制・遅延・制限 |
| Aggregation / Convergence | + | 共通接続点への合流 | 情報・要素の集積 |

Operatorの従来の意味は変えていません。色だけに依存せず、線・矢印・記号・Legend・選択時の文章を併用します。Overviewでは主要処理以外を弱め、Relationフィルターで構造を順に読めます。線の交差は結合を意味せず、Aggregationの接続点には丸印があります。

## 6作品への適用

- **Prime Suspect**：Police Institutionを最小限の補助Nodeとして明示。Institution × Procedure × Behaviourを加え、Institutional FrictionをImmediate ActionだけでなくProcedure / Verificationにも作用する制約として表示します。EvidenceとVerificationはOperational Realityへの共通接続点に集積します。
- **Foyle’s War**：既存NodeのままHistoryとSocial Constraint / Human Choice / Judgement / Meaningの関係を追加。歴史を先頭の入力で終わらせず、継続するCausal Contextとして読むモデルです。×は解釈上の相互依存で、過去を逆向きに変更する因果ではありません。
- **Endeavour**：Symbolic Interpretationを補い、Culture / Placeを人物関係・雰囲気・解釈と結びます。
- **The Bridge**：既存Environment / Borderの表記をEnvironmentにし、Borderを分離。Environment × Border × Saga / Martinの関係を見えるようにします。
- **Granada Holmes**：Watsonを明示し、Decodable World / Social Codeと結びます。Holmesを強い中心として残します。
- **The Closer**：内部NodeとEdgeの構成は旧版のまま。Brendaを中心とするPrimary Processing Pathを維持し、他作品に合わせて分散性を追加しません。

旧Node / EdgeのIDはすべて維持しています。補助Nodeは合計4個に限定し、追加の作品や採点要素はありません。6作品の初期座標・Evidence Interface・Class・ConceptRecords・主要分析本文は旧版と一致することを自動確認しています。

## 仮説と限界

Cognitive Centre DissolutionはX軸上の変化を説明するWorking Hypothesisであり、新軸でも発展段階の順位でもありません。Distributedであるほど優秀だという推論は行いません。

本版は提供されたSecond-Pass分析を可視化しています。作品の独立再採点や全Episodeの検証ではありません。Guideによって研究者の一致率や理解が改善するかは、共同検討で確かめる必要があります。

## 保存の互換性

Dataset schemaは`detective-cognitive-ecology/0.11`です。0.1 / 0.11のJSONから座標・Note・表示状態を読み込めます。作品と内部Nodeの固定IDを引き継ぎます。JSONだけで分析本文や実装を差し替えることはできず、改訂された本文を配る際はHTMLを共有します。

検証用ブラウザ保存とは別のrelease snapshot IDを使い、配布HTMLには元の6座標と空のNoteを内蔵します。Version 0.1のファイルは変更していません。
