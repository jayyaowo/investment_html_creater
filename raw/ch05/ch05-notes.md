# Chapter 5: Risk and Return: Past and Prologue (風險與報酬)

## 1. 報酬率衡量 (Measuring Returns)
- **持有期間報酬率 (Holding Period Return, HPR)**：衡量單一期間內投資人的總報酬（包含資本利得與股利）。
  公式：HPR = (P_1 - P_0 + D_1) / P_0
  其中 P_0 為期初價格，P_1 為期末價格，D_1 為期末現金股利。
- **多期平均報酬率**：
  1. 算術平均報酬率 (Arithmetic Average)：各期 HPR 的簡單平均，適用於預測未來單期期望報酬的最佳無偏估計量。
  2. 幾何平均報酬率 (Geometric Average / Time-weighted average)：衡量多期複利累積的真實年化報酬率。公式：(1 + r_G)^n = (1 + r_1)(1 + r_2)...(1 + r_n)。當報酬率有波動時，幾何平均必小於算術平均。

## 2. 風險與風險溢酬 (Risk and Risk Premiums)
- **期望報酬率 (Expected Return)**：E(r) = sum( p(s) * r(s) )，其中 p(s) 為情境 s 發生的機率，r(s) 為該情境下的報酬率。
- **變異數 (Variance) 與標準差 (Standard Deviation)**：衡量總風險（總波動度）。
  Var(r) = sigma^2 = sum( p(s) * [r(s) - E(r)]^2 )，標準差 sigma = sqrt(Var(r))。
- **無風險利率 (Risk-Free Rate, r_f)** 與 **風險溢酬 (Risk Premium)**：
  風險溢酬 = E(r) - r_f；超額報酬 (Excess Return) 為實際報酬減去無風險利率 (r - r_f)。
- **夏普比率 (Sharpe Ratio / Reward-to-Volatility Ratio)**：衡量每承擔一單位總風險所能獲得的超額報酬。
  公式：Sharpe Ratio = [E(r_p) - r_f] / sigma_p

## 3. 資本配置線 (Capital Allocation Line, CAL)
- 將資金配置於「無風險資產 (F，報酬率 r_f)」與「風險性投資組合 (P，期望報酬 E(r_p)、標準差 sigma_p)」，配置於 P 的比例為 y。
- **完整投資組合 (Complete Portfolio, C)** 的期望報酬與風險：
  E(r_c) = r_f + y * [E(r_p) - r_f]
  sigma_c = y * sigma_p
- **CAL 斜率**：即投資組合 P 的夏普比率 S = [E(r_p) - r_f] / sigma_p。
- **缺陷與限制**：本章僅討論單一既定風險組合 P 與無風險資產的配置，尚未解決「在眾多風險性資產中，該如何組出最佳風險性投資組合 P*」的問題（留待 Chapter 6 解決）。
