---
title: 資本配置線 (CAL)
en_title: Capital Allocation Line (CAL)
type: model
chapters:
  - ch05
tags:
  - capital-allocation
  - portfolio-theory
  - risk-return-tradeoff
status: active
sources:
  - raw/ch05/ch05-notes.md
updated: 2026-11-21
---

# 資本配置線 (Capital Allocation Line, CAL)

## 核心直覺

資本配置線 (Capital Allocation Line, CAL) 描述投資人將總資金分配在**無風險資產 (Risk-Free Asset, $F$)** 與一個既定的**風險性投資組合 (Risky Portfolio, $P$)** 之間時，所有可行的**完整投資組合 (Complete Portfolio, $C$)** 在「標準差—期望報酬」平面上所形成的投資機會集合。

透過調整投入風險組合 $P$ 的資金權重 $y$，投資人得以沿著一條直線自由選擇自己偏好的風險水準，而這條直線的斜率正是風險組合 $P$ 的 [[sharpe-ratio|夏普比率 (Sharpe Ratio)]]。

---

## 核心假設 (Key Assumptions)

1. **既定風險組合**：風險性投資組合 $P$ 的組成與其參數 $\left(E(r_P), \sigma_P\right)$ 為外生給定。
2. **無風險資產存在**：存在無違約且報酬無變異的無風險資產 $F$，其報酬率為固定常數 $r_f$（標準差 $\sigma_f = 0$，且與風險組合 $P$ 的共變異數為 $0$）。
3. **單一配置維度**：投資人僅在 $F$ 與 $P$ 之間調整配置比例 $y$（在基礎線性設定下，若允許以 $r_f$ 融資槓桿投資，則可達 $y > 1$）。

---

## 標準 LaTeX 公式與符號定義

設投入風險性投資組合 $P$ 的資金比例為 $y$，投入無風險資產 $F$ 的比例為 $1 - y$，則完整投資組合 $C$ 的期望報酬率與標準差分別為：

$$
E(r_C) = (1 - y)r_f + y\,E(r_P) = r_f + y\left[E(r_P) - r_f\right]
$$

$$
\sigma_C = y\,\sigma_P \qquad (y \ge 0)
$$

由 $\sigma_C = y\,\sigma_P$ 解出 $y = \frac{\sigma_C}{\sigma_P}$ 並代回期望報酬率公式，即可得 **CAL 在 $(\sigma, E(r))$ 平面上的直線方程式**：

$$
E(r_C) = r_f + \left[\frac{E(r_P) - r_f}{\sigma_P}\right]\sigma_C = r_f + S_P\,\sigma_C
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $C$ | 完整投資組合 (Complete Portfolio)，由無風險資產 $F$ 與風險組合 $P$ 構成 |
| $r_f$ | 無風險利率 (Risk-Free Rate)，亦為 CAL 之縱軸截距 |
| $E(r_P),\, \sigma_P$ | 既定風險性投資組合 $P$ 的期望報酬率與標準差 |
| $E(r_C),\, \sigma_C$ | 完整投資組合 $C$ 的期望報酬率與標準差 |
| $y$ | 配置於風險性投資組合 $P$ 的資金比例（$1-y$ 為配置於無風險資產的比例） |
| $S_P$ | CAL 的斜率，等於風險組合 $P$ 的 [[sharpe-ratio\|夏普比率 (Sharpe Ratio)]] $\frac{E(r_P) - r_f}{\sigma_P}$ |

### 關鍵幾何解讀
- **縱軸截距為 $r_f$**：當 $y = 0$（全數持有無風險資產）時，$\sigma_C = 0$ 且 $E(r_C) = r_f$。
- **線性風險溢酬**：由於無風險資產的變異數為零，完整投資組合的風險 $\sigma_C$ 與風險溢酬 $E(r_C) - r_f$ 皆與配置比例 $y$ 成**嚴格等比例**變動。
- **斜率即效率**：CAL 斜率 $S_P$ 越高，代表在相同總風險 $\sigma_C$ 下可獲得越高的期望報酬率，因此所有風險趨避投資人都希望找到**斜率最陡（夏普比率最大）**的 CAL。

---

## 模型缺陷與限制 (Limitations & Critiques)

1. **未解決最佳風險組合的建構問題**：CAL 僅處理「無風險資產 $F$ 與單一既定風險組合 $P$」的資金配置，但**並未說明在眾多風險性資產中，該如何挑選與決定權重以組出最佳風險性投資組合 $P^*$**（此核心問題留待 Chapter 6 解決）。
2. **以總風險作為唯一風險尺度**：CAL 使用標準差 $\sigma$ 衡量總風險，適合評估「整個完整投資組合」，但無法直接為單一證券定價（單一資產的可分散風險在市場均衡下不應獲得風險溢酬）。
3. **實務借貸利率不對稱（延伸考量）**：基礎 CAL 假設投資人可用相同的無風險利率 $r_f$ 進行借入（$y > 1$ 槓桿）與貸出（$0 \le y < 1$）；實務上借款利率高於無風險利率，將導致 CAL 在 $P$ 點右側出現折線（斜率變平緩）。

---

## 模型演進鏈 (Model Evolution)

```mermaid
flowchart LR
    A["風險與風險溢酬<br/>(Ch.05 基礎衡量)"] --> B["資本配置線 (CAL)<br/>(Ch.05：F + 既定 P)"]
    B --> C["馬可維茲投資組合理論<br/>(Ch.06：求解最佳風險組合 P*)"]
    C --> D["資本市場線 (CML) 與 CAPM<br/>(Ch.07：均衡市場組合 M 與系統性風險定價)"]
```

- **理論前身 / 基礎**：
  - [[risk-and-risk-premium|風險、風險溢酬與超額報酬]]（定義 $r_f$、$E(r)$ 與 $\sigma$）
  - [[sharpe-ratio|夏普比率 (Sharpe Ratio)]]（決定 CAL 斜率的核心比率）
- **後續修正 / 延伸模型**：
  - [[markowitz-portfolio-theory|馬可維茲投資組合理論 (Markowitz)]]（Ch.06）：利用多資產共變異數與效率前緣，找出切點最佳風險組合 $P^*$，使 CAL 斜率最大化並導出分離定理。
  - [[capm|資本資產定價模型 (CAPM)]]（Ch.07）：在市場均衡假設下，最佳風險組合收斂為市場投資組合 $M$，CAL 特化為 CML，並進一步拆解出系統性風險 $\beta$ 定價（三線完整對照見 [[cal-cml-sml-comparison|CAL、CML 與 SML 比較]]）。
- **所屬章節**：[[ch05-risk-and-return|Ch.05 風險與報酬]]
