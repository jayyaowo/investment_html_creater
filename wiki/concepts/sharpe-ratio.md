---
title: 夏普比率 (Sharpe Ratio)
en_title: Sharpe Ratio (Reward-to-Volatility Ratio)
type: concept
chapters:
  - ch05
tags:
  - performance-evaluation
  - risk-adjusted-return
  - sharpe-ratio
status: active
sources:
  - raw/ch05/ch05-notes.md
updated: 2026-11-21
---

# 夏普比率 (Sharpe Ratio)

## 核心定義

夏普比率 (Sharpe Ratio)，在 BKM 教材中亦稱**報酬對波動比率 (Reward-to-Volatility Ratio)**，用來衡量投資組合「**每承擔一單位總風險 ($\sigma_P$)，所能換取的風險溢酬 ($E(r_P) - r_f$)**」。數值越高，代表該投資組合的風險調整後效率越佳。

---

## 標準 LaTeX 公式與符號定義

$$
S_P = \frac{E(r_P) - r_f}{\sigma_P}
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $S_P$ | 投資組合 $P$ 的夏普比率 (Sharpe Ratio) |
| $E(r_P)$ | 風險性投資組合 $P$ 的期望報酬率 |
| $r_f$ | 無風險利率 (Risk-Free Rate) |
| $E(r_P) - r_f$ | 投資組合 $P$ 的 [[risk-and-risk-premium\|風險溢酬 (Risk Premium)]] |
| $\sigma_P$ | 投資組合 $P$ 的標準差（衡量總風險） |

---

## 直覺解讀與幾何意義

1. **即為資本配置線的斜率**：在 $(\sigma, E(r))$ 座標平面上，連接無風險資產 $(0, r_f)$ 與風險組合 $(\sigma_P, E(r_P))$ 的 [[capital-allocation-line|資本配置線 (CAL)]] 斜率恰好就是 $S_P$。
2. **橫跨投資決策的核心目標函數**：
   - 在 Ch.05 中，$S_P$ 決定了一條既定 CAL 的優劣。
   - 在 Ch.06 的 [[markowitz-portfolio-theory|馬可維茲投資組合理論]] 中，尋找「最佳風險性投資組合 $P^*$」在數學上即等價於「調整各風險資產權重以**最大化夏普比率 $S_P$**」。
   - 在 Ch.07 的 [[capm|CAPM]] 均衡下，市場投資組合 $M$ 的夏普比率 $S_M$ 即為 [[cal-cml-sml-comparison|資本市場線 (CML)]] 的斜率。
3. **適用範圍提醒**：由於分母使用總風險 $\sigma_P$，夏普比率最適合用來評估**整體投資組合**；若評估單一個別證券或主動選股能力，則常改用基於系統性風險 $\beta$ 的指標（詳見 [[beta-and-alpha|貝他係數與詹森阿法 (Beta & Alpha)]]）。

---

## 關聯連結
- **所屬章節**：[[ch05-risk-and-return|Ch.05 風險與報酬]]
- **基礎構成**：[[risk-and-risk-premium|風險、風險溢酬與超額報酬]]
- **直接應用與延伸模型**：
  - [[capital-allocation-line|資本配置線 (CAL)]]（$S_P$ 為 CAL 斜率）
  - [[markowitz-portfolio-theory|馬可維茲投資組合理論]]（最大化 $S_P$ 求得最佳風險組合 $P^*$）
  - [[cal-cml-sml-comparison|CAL、CML 與 SML 比較]]（$S_M$ 為 CML 斜率）
  - [[beta-and-alpha|貝他係數與詹森阿法 (Beta & Alpha)]]（個別資產之系統風險與異常報酬衡量）
- **未來跨章節延伸（待建立）**：
  - Ch.18 投資組合績效評估（與 Treynor Ratio、Information Ratio 之完整比較）
