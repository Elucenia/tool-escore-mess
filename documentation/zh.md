<!-- ELUCENIA technical documentation · escore-mess · zh · no clinical/professional/rights approval -->

# MESS（严重肢体损伤评分）

[条件、来源与许可](https://elucenia.org/zh/tools/escore-mess)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 骨骼及软组织损伤

`energia`

- `1` — 低能量（刺伤、简单骨折、手枪弹伤）
- `2` — 中等能量（开放性或多发骨折、脱位）
- `3` — 高能量（高速事故、步枪弹伤）
- `4` — 极高能量（上述情况+严重污染）

### 肢体缺血

`isquemia`

- `0` — 无缺血
- `1` — 脉搏减弱或消失，灌注正常
- `2` — 无脉搏、感觉异常、毛细血管再充盈缓慢
- `3` — 肢体冰冷、瘫痪、无感觉

### 缺血是否超过 6 小时？

`tempo`

- `0` — 否
- `1` — 是

### 休克

`choque`

- `0` — 收缩压始终\>90 mmHg
- `1` — 一过性低血压
- `2` — 持续性低血压

### 年龄

`idade`

- `0` — \< 30 岁
- `1` — 30 至 50 岁
- `2` — \> 50 岁

## 方法版本

MESS/Johansen 1990：4领域，缺血\>6 h加倍；不自动指令截肢

## 已记录的公式

MESS=骨骼/软组织损伤（1至4）+缺血（0至3，持续超过6 h则加倍）+休克（0至2）+年龄（0至2）。

## 限制与适用人群

原始MESS在下肢严重创伤的小样本人群中推导。这些人群中≥7阈值与截肢的关联并不确立普遍规则，也不构成自动指征。保肢取决于多学科评估和评分未概括的临床状况。

## 参考文献

- [Johansen K et al. Objective criteria accurately predict amputation following lower extremity trauma. J Trauma, 1990.](https://doi.org/10.1097/00005373-199005000-00007)

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
