---
title: Ch.05 風險與報酬
en_title: "Chapter 5: Risk and Return: Past and Prologue"
type: chapter
chapters:
  - ch05
tags:
  - risk-and-return
  - portfolio-basics
  - capital-allocation
status: active
sources:
  - raw/ch05/ch05-notes.md
updated: 2026-11-21
---

# Ch.05 風險與報酬 (Risk and Return: Past and Prologue)

## 本章核心問題與學習地圖

本章建立整門《投資學》最基礎的計量語言，依序回答三個核心問題：
1. **如何正確衡量報酬？** 區分單期報酬與多期複利報酬的差異。
2. **如何量化風險與風險補償？** 以機率分佈衡量總風險，並評估每單位風險換得的超額報酬。
3. **如何在無風險資產與風險組合間分配資金？** 透過資本配置線描繪風險與報酬的線性權衡。

```mermaid
flowchart LR
    A["報酬率衡量<br/>(HPR / 算術平均 / 幾何平均)"] --> B["風險與風險溢酬<br/>(期望報酬 / 標準差 / 超額報酬)"]
    B --> C["夏普比率<br/>(每單位總風險之溢酬)"]
    C --> D["資本配置線 (CAL)<br/>(無風險資產 + 既定風險組合 P)"]
    D -.-> E["未解問題：如何組出最佳風險組合 P*？<br/>(銜接 Ch.06)"]
```

---

## 本章核心知識拆解

### 1. 報酬率衡量
- 詳見 [[return-measurement|報酬率衡量：HPR、算術與幾何平均]]
- 重點摘要：
  - 單期總報酬以持有期間報酬率 (Holding Period Return, HPR) 衡量，同時涵蓋資本利得與現金股利。
  - 多期評估須區分**算術平均報酬率 (Arithmetic Average)**（預測未來單期期望報酬的最佳無偏估計量）與**幾何平均報酬率 (Geometric Average)**（反映真實多期複利年化績效；只要報酬存在波動，幾何平均必小於算術平均）。

### 2. 風險、風險溢酬與績效比率
- 詳見 [[risk-and-risk-premium|風險、風險溢酬與超額報酬]]、[[sharpe-ratio|夏普比率 (Sharpe Ratio)]]
- 重點摘要：
  - 透過情境分析計算期望報酬率 $E(r)$、變異數 $\sigma^2$ 與標準差 $\sigma$（衡量資產的總風險）。
  - 明確區分**事前預期**的風險溢酬 $E(r) - r_f$ 與**事後實現**的超額報酬 $R = r - r_f$。
  - 以 [[sharpe-ratio|夏普比率 (Sharpe Ratio)]] $S_P = \frac{E(r_P) - r_f}{\sigma_P}$ 衡量承擔每一單位總風險所獲得的風險溢酬。

### 3. 資本配置線與完整投資組合
- 詳見 [[capital-allocation-line|資本配置線 (CAL)]]
- 重點摘要：
  - 將資金依比例 $y$ 配置於既定風險性投資組合 $P$、比例 $1-y$ 配置於無風險資產 $F$，形成完整投資組合 (Complete Portfolio, $C$)。
  - 完整投資組合的風險—報酬軌跡為一條直線，即資本配置線 (Capital Allocation Line, CAL)，其截距為 $r_f$、斜率正好等於風險組合 $P$ 的 [[sharpe-ratio|夏普比率]] $S_P$。

---

## 核心公式速查

$$
\text{HPR} = \frac{P_1 - P_0 + D_1}{P_0}, \qquad (1 + r_G)^n = \prod_{t=1}^{n}(1 + r_t)
$$

$$
E(r) = \sum_{s} p(s)\,r(s), \qquad \sigma^2 = \sum_{s} p(s)\left[r(s) - E(r)\right]^2
$$

$$
E(r_C) = r_f + y\left[E(r_P) - r_f\right], \qquad \sigma_C = y\,\sigma_P \implies E(r_C) = r_f + \underbrace{\frac{E(r_P) - r_f}{\sigma_P}}_{S_P}\,\sigma_C
$$

---

## 跨章節脈絡銜接

- **本章限制**：[[capital-allocation-line|資本配置線 (CAL)]] 假設風險性投資組合 $P$ 為**既定給定**，只解決了「無風險資產 vs. 單一風險組合」的資金配置問題。
- **銜接 [[ch06-efficient-diversification|Ch.06 效率多角化與投資組合理論]]**：透過 [[markowitz-portfolio-theory|馬可維茲投資組合理論]] 與 [[systematic-vs-unsystematic-risk|多角化降險原理]]，解決「如何從眾多風險性資產中找出使 [[sharpe-ratio|夏普比率]] 最大的**最佳風險性投資組合 $P^*$**」之問題。
- **銜接 [[ch07-capm-and-apt|Ch.07 CAPM 與多因子定價理論]]**：當所有投資人皆持有市場投資組合 $M$ 作為最佳風險組合時，CAL 特化為資本市場線 (CML)，並進一步導出 [[capm|資本資產定價模型 (CAPM)]]（詳見 [[cal-cml-sml-comparison|CAL、CML 與 SML 比較]]）。
