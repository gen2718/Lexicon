# Verification Notes — Version 0.11

確認日：2026-09-19

## 自動回帰検証：22 / 22通過

旧版の13項目を維持し、今回の変更を含む9項目を追加しました。Datasetと実装のイベント処理を模擬DOMで実行した結果です。実ブラウザの入力・描画を網羅するものではありません。詳細な項目は`verification.json`に収録しています。

- 6座標、Class、Evidence、主要分析本文、旧Node / Edge / Concept IDの維持。
- 6作品のInspectorとMicro、30通りの異なる2作品比較。
- Overlay全8組合せ、同時表示時のMacroラベル枠の非重複。
- Pointerドラッグと整数スナップ、キーボード、Pan / Zoom / Fit all、境界値、個別／全体Reset、Note保持。
- 両軸10 Anchor、Guide開閉、Working HypothesisとScoreの分離。
- 4 Edge種別の矢印・無方向Coupling・抑制バー・共通合流点。
- 6 Network × 6 Relationフィルター × 2レイアウト、および指定3比較ペア。
- 実装の非同期Importハンドラーで旧JSONの小数を読み込み、確認前プレビューと確定後の値を検証。
- Noteのみの変更・Exportでは旧小数を保持し、明示的な座標編集では整数化。
- JSON往復、選択Concept・Overlay・メタデータ、JSON / テキスト書き出し。
- 不正Importの拒否、文字列の安全な表示、外部依存・端末固有パス不在。

## 実Safariで確認した範囲

ローカルHTMLをSafariで開いて確認しました。

- Version 0.11の起動と6作品Macro、作品選択、整数表示。
- Axis Guideの開閉と全10 Anchorの視認。
- 全6作品のMicroへの移動とEcological Couplingフィルター。
- Prime SuspectのOverviewで4種類の線とInstitutionを視認。
- Prime Suspect ↔ Foyle’s War、Granada Holmes ↔ The Closer、Endeavour ↔ The BridgeのCompare。
- 通常ウィンドウとResponsive Design Modeの900 × 900、760 × 900で代表画面を確認。760pxのMacroは縦配置になり、ラベルが表示されることを目視。
- 確認した状態で画面の実行時エラーカウンターは0。

## 実Safariでは未完了の範囲

実マウスによるドラッグ・Pan、数値編集とNote保存・Resetの一連の操作、すべてのOverlay組合せ、JSON実ファイル選択、HTML / JSONダウンロード後の再読込の全工程は、今回Safari上での確認を完了していません。これらに対応する処理は上記の自動検証で確認していますが、同じ検証範囲ではありません。

ネイティブ操作ツールがウィンドウ取得またはクリップボード読み取りで断続的に失敗し、Safari入力操作の一部を最後まで確認できませんでした。これはアプリ内のJavaScriptエラーとして観測されたものではありません。

全Safari世代、全端末サイズ、VoiceOverでの完全な操作性は未検証です。外部ネットワーク要求を使わない構成とローカル起動は確認しましたが、OS全体のオフライン切替試験は行っていません。

## 研究上の成功条件

GuideのAnchor、制度全体の制約、歴史の継続作用、Environment / Border / Character Pairの関係、The Closerの強い中心を実装しました。実際に研究者がX=70と80の違いを説明できるか、線の意味を一貫して読めるかは、人による共同検討が必要です。実装テストを分析仮説の実証とは扱いません。
