---
title: 風險、風險溢酬與超額報酬
en_title: "Risk, Risk Premium, and Excess Return"
type: concept
chapters:
  - ch05
tags:
  - risk
  - risk-premium
  - excess-return
  - expected-return
status: active
sources:
  - raw/ch05/ch05-notes.md
updated: 2026-11-21
---

# 風險、風險溢酬與超額報酬 (Risk, Risk Premium & Excess Return)

## 核心定義

投資決策面對未來的不確定性，在情境分析 (Scenario Analysis) 架構下，我們以**期望報酬率 (Expected Return)** 衡量潛在平均回報，以**變異數 (Variance)** 與**標準差 (Standard Deviation)** 衡量報酬圍繞平均值的離散程度（即**總風險**）。同時，為評估承擔風險是否值得，需將資產報酬與**無風險利率 (Risk-Free Rate, $r_f$)** 比較，衍生出**風險溢酬 (Risk Premium)** 與**超額報酬 (Excess Return)** 兩個關鍵概念。

---

## 標準 LaTeX 公式與符號定義

### 1. 期望報酬率 (Expected Return)
在離散情境 $s$ 下，各種情境報酬率以發生機率加權平均：

$$
E(r) = \sum_{s} p(s)\,r(s)
$$

### 2. 變異數 (Variance) 與標準差 (Standard Deviation)
衡量報酬偏離期望報酬的程度，代表資產的**總風險（總波動度）**：

$$
\text{Var}(r) = \sigma^2 = \sum_{s} p(s)\left[r(s) - E(r)\right]^2
$$

$$
\sigma = \sqrt{\text{Var}(r)} = \sqrt{\sigma^2}
$$

### 3. 風險溢酬 (Risk Premium) 與超額報酬 (Excess Return)

$$
\text{Risk Premium} = E(r) - r_f
$$

$$
R = r - r_f
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $s$ | 未來可能發生的經濟情境 (Scenario) |
| $p(s)$ | 情境 $s$ 發生的機率（滿足 $\sum_s p(s) = 1$） |
| $r(s)$ | 在情境 $s$ 下資產的實現報酬率 |
| $E(r)$ | 資產的期望報酬率 (Expected Return) |
| $\sigma^2,\, \sigma$ | 報酬率的變異數與標準差，衡量總風險（$\sigma$ 與報酬率同單位，便於直接比較） |
| $r_f$ | 無風險利率 (Risk-Free Rate)，通常以短期國庫券 (T-Bills) 利率作為實務代理 |
| $E(r) - r_f$ | **風險溢酬 (Risk Premium)**：投資人承擔風險所**預期**獲得的額外補償 |
| $R = r - r_f$ | **超額報酬 (Excess Return)**：資產**實際實現**報酬率減去無風險利率之差額 |

---

## 關鍵辨析：風險溢酬 vs. 超額報酬

實務與考題中極易混淆「風險溢酬」與「超額報酬」，兩者的核心差異在於**時間視角（事前 vs. 事後）**：

| 項目 | 公式 | 時間視角 | 經濟意義與正負性 |
| :--- | :---: | :---: | :--- |
| **風險溢酬 (Risk Premium)** | $E(r) - r_f$ | **事前預期 (Ex-ante)** | 風險趨避投資人願意承擔風險的誘因，均衡下通常為**正值** |
| **超額報酬 (Excess Return)** | $R = r - r_f$ | **事後實現 (Ex-post)** | 事後實際表現相對無風險資產的差額，受市場波動影響，**可能為正亦可能為負** |

> 兩者的關係：風險溢酬正是超額報酬的期望值，即 $E(R) = E(r - r_f) = E(r) - r_f$。

---

## 關聯連結
- **所屬章節**：[[ch05-risk-and-return|Ch.05 風險與報酬]]
- **前置概念**：[[return-measurement|報酬率衡量：HPR、算術與幾何平均]]
- **延伸指標與模型**：
  - [[sharpe-ratio|夏普比率 (Sharpe Ratio)]]（將風險溢酬除以標準差 $\sigma$，標準化每單位總風險的報酬補償）
  - [[capital-allocation-line|資本配置線 (CAL)]]（以 $r_f$ 為起點，探討風險溢酬與總風險 $\sigma_C$ 的線性配置關係）
  - [[systematic-vs-unsystematic-risk|系統性風險與非系統性風險]]（將本章「總風險 $\sigma^2$」進一步拆解為可分散與不可分散風險）
  - [[capm|資本資產定價模型 (CAPM)]] 與 [[single-index-model|單因子指數模型]]（以市場風險溢酬 $E(r_M) - r_f$ 與超額報酬 $R_i = r_i - r_f$ 作為核心定價變數）
