<!-- ELUCENIA technical documentation · das28 · zh · no clinical/professional/rights approval -->

# DAS28（ESR 与 CRP）

[条件、来源与许可](https://elucenia.org/zh/tools/das28)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 压痛关节数（28 个关节）

`tjc`

范围: 0–28

### 肿胀关节数（28 个关节）

`sjc`

范围: 0–28

### 患者总体健康评价（视觉量表）

`gh`

mm · 范围: 0–100

### 红细胞沉降率（ESR）

`vhs`

mm/h · 选填 · 范围: 1–150

### C 反应蛋白（CRP）

`pcr`

mg/L · 选填 · 范围: 0–300

## 方法版本

DAS28-ESR/Prevoo 1995与DAS28-CRP/Wells 2009；28关节；CRP截距0.96

## 已记录的公式

DAS28-ESR = 0.56 × √(压痛关节数) + 0.28 × √(肿胀关节数) + 0.70 × ln(ESR) + 0.014 × 总体评估.

DAS28-CRP = 0.56 × √(压痛关节数) + 0.28 × √(肿胀关节数) + 0.36 × ln(CRP + 1) + 0.014 × 总体评估 + 0.96 (CRP单位mg/L).

## 限制与适用人群

DAS28于1995年为评估类风湿关节炎活动度而开发，使用28个关节计数，并与风湿科医生的临床评估比较。C反应蛋白（CRP）版本并不自动等同于红细胞沉降率（ESR）版本；公式、单位和阈值须与所用来源及版本一致。

## 参考文献

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
