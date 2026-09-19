# Detective Cognitive Ecology — Interactive 2D Prototype Version 0.11
## Calibration Edition · 2026-09-19

Alpha Version 6.0のSecond-Pass Analytical Viewです。座標は認知構造の仮説であり、品質の順位やClassではありません。

## 開く・共有する

`detective-cognitive-ecology-v0.11.html`をSafariで開いてください。ZIPの場合は先に展開します。HTML単体で動作し、ネット接続・サーバー・アカウント・インストールは不要です。data.jsonや説明書を同じ場所に置く必要もありません。

ほかの人には**HTMLまたはZIPのファイルそのもの**をメール、AirDrop、共有ストレージなどで渡してください。自分のMacのファイルアドレスだけを送っても相手には開けません。

## 今回の3つの変更

1. 座標を整数表示に変更。ドラッグや数値編集も整数単位に揃えます。
2. **Axis Guide**に両軸の0 / 25 / 50 / 75 / 100の意味を追加。
3. Microの関係を**Primary Processing Path / Ecological Coupling / Constraint / Aggregation**に区別。線・矢印・記号・説明を併用します。

6作品、初期座標、Evidence Interface、Classは維持しています。既存のVersion 0.1は別ファイルのまま残しています。

## 最初に試すこと

1. **Macro**で作品を選び、Inspectorを読みます。Overlayは必要なものだけ追加します。
2. **Axis Guide**で、X=75などの目安を確認します。Guideは人間による検討の参照で、自動採点や自動配置には使いません。
3. **Calibration Mode**をONにし、作品Nodeをドラッグ、またはInspectorのX / Yを編集します。Nodeにフォーカスがある場合は矢印キーで1、Shift＋矢印で5ずつ移動できます。
4. **Hypothesis Note**に理由と参照Anchorを記入し「座標・Noteを保存」を押します。Reason / Relevant Axis Anchor / Date or Sessionは自由記入です。個別／全座標リセットは座標だけを初期値へ戻し、Noteを保持します。
5. **Micro**または**Focus**を押します。RelationメニューでOverview、Primary Processing Path、Ecological Coupling、Constraint / Inhibition、Aggregation / Convergence、All Relationsを切り替えます。内部NodeとEdgeを選択すると説明を読めます。
6. **Compare**でPrime Suspect ↔ Foyle’s Warなどを並べ、同じ関係種別で比較します。内部Networkはカード内をスクロールできます。
7. **共有・データ保存**から「変更を含む共有用HTMLを保存」します。受け取った人はそのHTMLだけで同じ検討版を開けます。

空白ドラッグでPan、＋／−でZoom、Fit allで全体表示に戻します。狭い画面ではInspectorが下に回り、Networkを横にスクロールして読めます。

## 保存と旧JSONの読み込み

ブラウザ保存は端末内の補助保存です。元のHTMLは自動では上書きされません。共同検討に渡す前にHTMLまたはJSONを書き出してください。同時共同編集ではなく、各人の検討版を交換する方式です。Noteも共有ファイルに含まれます。

Version 0.1 / 0.11のJSONを読み込めます。JSONは6作品の座標・Note・選択Concept・Overlay・表示状態を引き継ぎ、内蔵の分析本文は置き換えません。読み込み前に差分を確認できます。

旧JSONの小数は内部位置・JSON値としてそのまま保持し、画面だけ整数表示します。Noteの編集や書き出しだけでは小数を丸めません。その作品の座標を明示的に編集した時点でX / Yを整数に揃えます。

## 分析の前提

座標・分析本文は提供された仮説を可視化したものです。Microの補助Nodeと関係線は、その仮説を明示する編集上のモデルであり、場面ごとの実証や因果量の測定結果ではありません。Guideの端点は理想的な参照で、厳密な境界値ではありません。

Cognitive Centre DissolutionはWorking Hypothesisです。新しい軸・Element・Scoreではありません。Alpha 6.0の8 Elements / 4 Layers、既存Classを変更・再計算していません。The Bridgeは指定されたSaga / Martinの例に焦点を当てます。

## 確認範囲

自動検証22項目が通過しました。Safariではローカル起動、整数表示、Axis Guide、6作品のMicro、関係フィルター、指定3組のCompare、900pxと760px幅での代表表示を確認し、確認した状態で実行時エラーは0件でした。

実マウスのドラッグ、Note保存・Reset、書き出しファイルの再読み込みをSafariで最後まで通す確認は未完了です。これらは模擬DOM上のイベント処理で検証しています。詳細は`Verification-Notes.md`に分けて記録しています。全Safari世代の動作保証や、分析解釈の妥当性・学習効果の検証は含みません。

## 同梱ファイル

- HTML：単体で利用する完成版
- data.json：HTMLに内蔵した初期Datasetと同一内容
- Design-Notes.md：変更理由とモデル上の境界
- CHANGELOG.md：0.1 → 0.11の差分
- Requirements-Verification.md：全29章との照合
- Verification-Notes.md / verification.json：検証範囲と結果
