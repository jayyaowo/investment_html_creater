---
title: 貝他係數與詹森阿法 (Beta & Alpha)
en_title: "Beta and Jensen's Alpha"
type: concept
chapters:
  - ch07
tags:
  - beta
  - alpha
  - systematic-risk
  - asset-pricing
status: active
sources:
  - raw/ch07/ch07-notes.md
updated: 2026-11-21
---

# 貝他係數與詹森阿法 (Beta & Jensen's Alpha)

## 核心定義

在 [[capm|資本資產定價模型 (CAPM)]] 框架下，評估個別資產的風險與定價合理性依賴兩個核心指標：
- **貝他係數 (Beta, $\beta_i$)**：衡量個別資產 $i$ 報酬率對市場投資組合 $M$ 波動的**系統性風險敏感度**。
- **詹森阿法 (Jensen's Alpha, $\alpha_i$)**：衡量資產實際預期報酬率超出 [[capm|證券市場線 (SML)]] 理論均衡報酬率的差額，代表資產的**錯誤定價程度（異常報酬）**。

---

## 標準 LaTeX 公式與符號定義

### 1. 貝他係數 (Beta)

$$
\beta_i = \frac{\text{Cov}(r_i, r_M)}{\sigma_M^2}
$$

### 2. 詹森阿法 (Jensen's Alpha)

$$
\alpha_i = E(r_i) - \left\{r_f + \beta_i\left[E(r_M) - r_f\right]\right\}
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $\beta_i$ | 資產 $i$ 的系統性風險係數（市場投資組合本身的 $\beta_M = 1$；無風險資產的 $\beta_f = 0$） |
| $\text{Cov}(r_i, r_M)$ | 資產 $i$ 與市場投資組合 $M$ 報酬率之共變異數 |
| $\sigma_M^2$ | 市場投資組合 $M$ 報酬率之變異數 |
| $\alpha_i$ | 資產 $i$ 的異常期望報酬率（偏離 SML 的垂直距離） |
| $E(r_i)$ | 證券分析師估計（或實際預期）的資產 $i$ 期望報酬率 |
| $r_f + \beta_i[E(r_M) - r_f]$ | CAPM / SML 給出的理論公平均衡期望報酬率 |

---

## 直覺解讀與投資判別

### 1. $\beta_i$ 的風險解讀
- **$\beta_i > 1$（攻擊型資產）**：對市場波動放大反應，系統性風險高於大盤。
- **$\beta_i = 1$（市場同步資產）**：與市場投資組合具有相同的系統性風險。
- **$0 < \beta_i < 1$（防禦型資產）**：對總體景氣波動較不敏感，系統性風險低於大盤。

### 2. $\alpha_i$ 與 SML 錯誤定價判別

| Alpha 狀態 | 在 SML 圖上的位置 | 定價判讀 | 主動投資策略 |
| :---: | :--- | :--- | :--- |
| $\alpha_i > 0$ | 位於 SML **上方** | 預期報酬高於合理要求報酬 → 價格被**低估 (Underpriced)** | **買進 (Buy)** |
| $\alpha_i = 0$ | 恰好落在 SML **線上** | 價格處於**公平均衡定價 (Fairly Priced)** | 持有／被動配置 |
| $\alpha_i < 0$ | 位於 SML **下方** | 預期報酬低於合理要求報酬 → 價格被**高估 (Overpriced)** | **賣出或放空 (Sell / Short)** |

> **市場均衡條件**：在完全競爭且達均衡的市場中，套利與買賣力量會迅速修正錯誤定價，使所有資產的 $\alpha_i = 0$。

---

## 關聯連結
- **所屬章節**：[[ch07-capm-and-apt|Ch.07 CAPM 與多因子定價理論]]
- **核心定價模型**：
  - [[capm|資本資產定價模型 (CAPM)]]（SML 定價基礎）
  - [[single-index-model|單因子指數模型]]（透過超額報酬線性回歸 $R_i = \alpha_i + \beta_i R_M + e_i$ 實證估計 $\alpha_i$ 與 $\beta_i$）
  - [[fama-french-three-factor|Fama-French 三因子模型]]（將單一 $\beta$ 擴展為市場、規模、價值三因子敏感度）
- **相關概念與比較**：
  - [[systematic-vs-unsystematic-risk|系統性風險與非系統性風險]]
  - [[sharpe-ratio|夏普比率 (Sharpe Ratio)]]（以總風險 $\sigma$ 衡量整體組合效率；$\alpha_i$ 則以系統風險 $\beta$ 評估個別證券超額表現）
  - [[cal-cml-sml-comparison|CAL、CML 與 SML 比較]]
  - [[efficient-market-hypothesis|效率市場假說 (EMH)]] 與 [[event-study-and-anomalies|事件研究法與市場異象]]（實證檢驗市場是否滿足均衡條件 $\alpha_i = 0$，以及主動型共同基金能否持續創造正 $\alpha$）
