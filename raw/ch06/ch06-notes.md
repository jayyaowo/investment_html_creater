# Chapter 6: Efficient Diversification (效率多角化與投資組合理論)

## 1. 多角化與投資組合風險 (Diversification and Portfolio Risk)
- **系統性風險 (Systematic Risk / Market Risk)**：由總體經濟因素（利率、通膨、景氣循環）引起，無法透過增加資產數量消除。
- **非系統性風險 (Unsystematic / Firm-Specific Risk)**：個別公司特有的風險（研發失敗、罷工），可透過多角化投資（Diversification）大幅降低甚至消除。

## 2. 兩資產投資組合 (Two-Risky-Asset Portfolio)
- 投資於資產 D（權重 w_D）與資產 E（權重 w_E = 1 - w_D）：
  - 期望報酬：E(r_p) = w_D * E(r_D) + w_E * E(r_E)
  - 變異數：sigma_p^2 = w_D^2 * sigma_D^2 + w_E^2 * sigma_E^2 + 2 * w_D * w_E * Cov(r_D, r_E)
  - 共變異數與相關係數：Cov(r_D, r_E) = rho_DE * sigma_D * sigma_E，其中相關係數 rho_DE 介於 -1 到 +1 之間。
  - **多角化核心原理**：只要 rho_DE < 1，投資組合標準差 sigma_p 就會嚴格小於個別資產標準差的加權平均；當 rho_DE = -1 時，可建構出零風險投資組合。

## 3. Markowitz 投資組合選擇模型 (Markowitz Portfolio Selection Model)
- **最小變異數前緣 (Minimum-Variance Frontier)**：在給定各種期望報酬率水準下，所能達成的最低變異數投資組合集合。
- **效率前緣 (Efficient Frontier)**：位於全域最小變異數投資組合 (Global Minimum-Variance Portfolio, GMVP) 上方的半支曲線，代表在相同風險下提供最高期望報酬的組合。
- **最佳風險性投資組合 (Optimal Risky Portfolio, P*)**：結合無風險利率 r_f，從 r_f 出發畫一條與效率前緣相切的資本配置線 (CAL)，切點即為夏普比率最大化的最佳風險性組合 P*（此切線在均衡狀態下即為資本市場線 CML）。
- **分離定理 (Separation Property)**：投資決策分為兩獨立步驟：(1) 客觀技術面決定最佳風險性組合 P*（所有投資人相同）；(2) 個人風險趨避程度決定在 r_f 與 P* 之間的資金配置比例 y。
- **缺陷與限制**：Markowitz 模型需要估計大量的共變異數矩陣參數（若有 n 檔股票，需估計 n 個期望報酬、n 個變異數、以及 n(n-1)/2 個共變異數），計算成本極高且估計誤差大（引出 Chapter 7 的單因子指數模型與 CAPM）。
