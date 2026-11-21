---
title: 報酬率衡量：HPR、算術與幾何平均
en_title: "Return Measurement: HPR, Arithmetic and Geometric Average"
type: concept
chapters:
  - ch05
tags:
  - return-measurement
  - hpr
  - compounding
status: active
sources:
  - raw/ch05/ch05-notes.md
updated: 2026-11-21
---

# 報酬率衡量：HPR、算術與幾何平均

## 核心定義

衡量投資績效分為「單一期間」與「多期跨期」兩個層次：單期總報酬以**持有期間報酬率 (Holding Period Return, HPR)** 計算；跨越多個期間時，則依分析目的選用**算術平均報酬率 (Arithmetic Average)** 或**幾何平均報酬率 (Geometric Average)**。

---

## 標準 LaTeX 公式與符號定義

### 1. 持有期間報酬率 (Holding Period Return, HPR)
衡量投資人在單一持有期間內所獲得的總報酬率，同時涵蓋價格變動（資本利得／損失）與現金股利收入：

$$
\text{HPR} = \frac{P_1 - P_0 + D_1}{P_0} = \underbrace{\frac{P_1 - P_0}{P_0}}_{\text{資本利得率}} + \underbrace{\frac{D_1}{P_0}}_{\text{股利殖利率}}
$$

### 2. 算術平均報酬率 (Arithmetic Average Return)
將 $n$ 個期間的各期持有期間報酬率 $r_1, r_2, \dots, r_n$ 取簡單平均：

$$
\bar{r}_A = \frac{1}{n}\sum_{t=1}^{n} r_t
$$

### 3. 幾何平均報酬率 (Geometric Average / Time-Weighted Average Return)
將多期報酬以複利方式連乘並開 $n$ 次方根，衡量期初投入 1 元在期末累積成相同終值所需的固定年化複利報酬率：

$$
(1 + r_G)^n = (1 + r_1)(1 + r_2)\cdots(1 + r_n) = \prod_{t=1}^{n}(1 + r_t)
$$

$$
r_G = \left[\prod_{t=1}^{n}(1 + r_t)\right]^{\frac{1}{n}} - 1
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $P_0,\, P_1$ | 資產的期初價格與期末價格 |
| $D_1$ | 持有期間期末配發之現金股利（或現金流入） |
| $r_t$ | 第 $t$ 期的持有期間報酬率 ($\text{HPR}_t$) |
| $n$ | 觀測總期數 |
| $\bar{r}_A$ | 算術平均報酬率 (Arithmetic Average Return) |
| $r_G$ | 幾何平均報酬率 (Geometric Average Return)，亦稱時間加權平均報酬率 (Time-Weighted Average) |

---

## 算術平均 vs. 幾何平均：適用情境與波動差異

| 比較維度 | 算術平均報酬率 ($\bar{r}_A$) | 幾何平均報酬率 ($r_G$) |
| :--- | :--- | :--- |
| **計算邏輯** | 各期報酬率之簡單平均（忽略複利） | 各期報酬因子連乘開方（反映複利累積） |
| **核心用途** | **向前預測**：估計未來**單一期間**期望報酬率的最佳無偏估計量 | **向後檢視**：衡量過去多期實際財富複利成長的真實年化報酬率 |
| **大小關係** | 當各期報酬完全相同時 $\bar{r}_A = r_G$；**只要報酬率存在波動，必滿足 $r_G < \bar{r}_A$** | 永遠小於或等於算術平均，且波動度 ($\sigma^2$) 越大，兩者差距越大 |

### 直覺解讀：為何有波動時 $r_G < \bar{r}_A$？
假設某資產第一年上漲 $50\%$、第二年下跌 $50\%$：
- 算術平均：$\bar{r}_A = \frac{0.50 + (-0.50)}{2} = 0\%$（看似沒賺沒賠）。
- 實際財富變化：$(1 + 0.50)(1 - 0.50) = 0.75$（本金其實虧損 $25\%$）。
- 幾何平均：$r_G = \sqrt{0.75} - 1 \approx -13.4\%$，才能真實反映複利折損（波動拖累）。

---

## 關聯連結
- **所屬章節**：[[ch05-risk-and-return|Ch.05 風險與報酬]]
- **延伸概念**：[[risk-and-risk-premium|風險、風險溢酬與超額報酬]]（從歷史樣本報酬進一步過渡至機率情境下的期望報酬與變異數）
