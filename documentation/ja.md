<!-- ELUCENIA technical documentation · das28 · ja · no clinical/professional/rights approval -->

# DAS28（ESR・CRP）

[条件・出典・許諾](https://elucenia.org/ja/tools/das28)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 圧痛関節数（28関節）

`tjc`

範囲: 0–28

### 腫脹関節数（28関節）

`sjc`

範囲: 0–28

### 患者による全般的健康評価（視覚尺度）

`gh`

mm · 範囲: 0–100

### 赤血球沈降速度（ESR）

`vhs`

mm/h · 任意 · 範囲: 1–150

### C反応性蛋白（CRP）

`pcr`

mg/L · 任意 · 範囲: 0–300

## 方法の版

DAS28-ESR/Prevoo 1995とDAS28-CRP/Wells 2009；28関節；CRP切片0.96

## 記載された計算式

DAS28-ESR = 0.56 × √(圧痛数) + 0.28 × √(腫脹数) + 0.70 × ln(ESR) + 0.014 × 全般評価.

DAS28-CRP = 0.56 × √(圧痛数) + 0.28 × √(腫脹数) + 0.36 × ln(CRP + 1) + 0.014 × 全般評価 + 0.96 (CRP単位mg/L).

## 限界・対象集団

1995年のDAS28は、関節リウマチの活動性を評価するため、28関節の数とリウマチ専門医による臨床評価との比較を用いて開発されました。C反応性蛋白（CRP）を用いる型は、赤血球沈降速度（ESR）を用いる型と自動的に同等になるわけではありません。式、単位、閾値は、使用する出典と版に一致している必要があります。

## 参考文献

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
