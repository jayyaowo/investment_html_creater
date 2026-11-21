---
title: 系統性風險與非系統性風險
en_title: Systematic vs. Unsystematic Risk
type: concept
chapters:
  - ch06
  - ch07
tags:
  - diversification
  - systematic-risk
  - unsystematic-risk
  - portfolio-risk
status: active
sources:
  - raw/ch06/ch06-notes.md
  - raw/ch07/ch07-notes.md
updated: 2026-11-21
---

# 系統性風險與非系統性風險 (Systematic vs. Unsystematic Risk)

## 核心定義

在 [[risk-and-risk-premium|風險、風險溢酬與超額報酬]] 中以標準差 $\sigma$ 衡量的「總風險」，在投資組合層面可進一步拆解為兩種性質截然不同的風險來源：

| 比較維度 | 系統性風險 (Systematic Risk) | 非系統性風險 (Unsystematic Risk) |
| :--- | :--- | :--- |
| **別稱** | 市場風險 (Market Risk)、不可分散風險 | 公司特有風險 (Firm-Specific Risk)、可分散風險 |
| **成因** | 總體經濟共同衝擊（利率變動、通貨膨脹、景氣循環） | 個別公司專屬事件（研發失敗、工廠罷工、經營失誤） |
| **多角化效果** | **無法**透過增加投資組合內的資產數量消除 | **可以**透過多角化投資 (Diversification) 大幅降低甚至趨近於零 |
| **均衡風險溢酬** | 市場給予風險溢酬補償（由 $\beta$ 衡量） | 均衡下**不給予**額外風險溢酬（因投資人可免費分散） |

---

## 標準 LaTeX 公式與符號定義

### 1. 兩資產投資組合之多角化降險公式（Ch.06）
設投資組合由資產 $D$（權重 $w_D$）與資產 $E$（權重 $w_E = 1 - w_D$）組成：

$$
E(r_P) = w_D E(r_D) + w_E E(r_E)
$$

$$
\sigma_P^2 = w_D^2 \sigma_D^2 + w_E^2 \sigma_E^2 + 2 w_D w_E\,\text{Cov}(r_D, r_E)
$$

$$
\text{Cov}(r_D, r_E) = \rho_{DE}\,\sigma_D\,\sigma_E \qquad (-1 \le \rho_{DE} \le 1)
$$

### 2. 單因子模型下之總風險定量拆解（Ch.07）
在 [[single-index-model|單因子指數模型]] 下，個別資產 $i$ 的總變異數可精確分解為系統性與非系統性兩部分：

$$
\sigma_i^2 = \underbrace{\beta_i^2 \sigma_M^2}_{\text{系統性風險}} + \underbrace{\sigma^2(e_i)}_{\text{非系統性（公司特有）風險}}
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $w_D,\, w_E$ | 資產 $D$ 與資產 $E$ 之投資權重（$w_D + w_E = 1$） |
| $\text{Cov}(r_D, r_E)$ | 資產 $D$ 與資產 $E$ 報酬率之共變異數 (Covariance) |
| $\rho_{DE}$ | 資產 $D$ 與資產 $E$ 報酬率之相關係數 (Correlation Coefficient)，介於 $-1$ 至 $+1$ |
| $\beta_i^2 \sigma_M^2$ | 來自市場共同波動的系統性變異數 |
| $\sigma^2(e_i)$ | 公司特有殘差項 $e_i$ 之變異數（非系統性風險） |

---

## 多角化核心原理與極端情況

將 $\text{Cov}(r_D, r_E) = \rho_{DE}\sigma_D\sigma_E$ 代入兩資產變異數公式可看出相關係數 $\rho_{DE}$ 的關鍵作用：
- **完全正相關 ($\rho_{DE} = +1$)**：$\sigma_P = w_D \sigma_D + w_E \sigma_E$，此時**無任何多角化降險效果**，組合標準差恰好等於個別標準差的加權平均。
- **非完全正相關 ($\rho_{DE} < 1$)**：只要相關係數嚴格小於 $1$，投資組合標準差 $\sigma_P$ **必定嚴格小於**個別資產標準差的加權平均（$\sigma_P < w_D \sigma_D + w_E \sigma_E$），這就是多角化的數學核心。
- **完全負相關 ($\rho_{DE} = -1$)**：$\sigma_P = |w_D \sigma_D - w_E \sigma_E|$，可透過適當權重 $w_D = \frac{\sigma_E}{\sigma_D + \sigma_E}$ 建構出**零風險投資組合 ($\sigma_P = 0$)**。

---

## 關聯連結
- **所屬章節**：[[ch06-efficient-diversification|Ch.06 效率多角化]]、[[ch07-capm-and-apt|Ch.07 CAPM 與多因子定價理論]]
- **前置概念**：[[risk-and-risk-premium|風險、風險溢酬與超額報酬]]
- **核心應用模型**：
  - [[markowitz-portfolio-theory|馬可維茲投資組合理論]]（利用資產間共變異數建構效率前緣）
  - [[single-index-model|單因子指數模型]]（量化拆解系統性與非系統性變異數）
  - [[capm|資本資產定價模型 (CAPM)]] 與 [[beta-and-alpha|Beta 與 Alpha]]（僅對系統性風險定價）
