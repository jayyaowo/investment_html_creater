# Chapter 8: The Efficient Market Hypothesis (效率市場假說, EMH)

## 1. 效率市場假說核心概念 (Efficient Market Hypothesis, EMH)
- **隨機漫步 (Random Walk)**：股價變動是隨機且不可預測的，因為任何可預測的資訊都會立刻被理性投資人交易並反映在當前價格中，因此股價只會對「未預期的新資訊 (News)」做出反應。
- **效率市場三種形式 (Three Versions of EMH)**：
  1. **弱式效率 (Weak-Form EMH)**：股價已充分反映所有「歷史市場交易資訊」（過去股價、成交量、報酬率序列）。推論：技術分析 (Technical Analysis) 無效，無法賺取超額報酬。
  2. **半強式效率 (Semistrong-Form EMH)**：股價已充分反映所有「公開可得資訊」（除了歷史交易資料外，還包含財報、盈餘預測、總經數據、公司治理資訊）。推論：基本面分析 (Fundamental Analysis) 無法持續賺取超額報酬。
  3. **強式效率 (Strong-Form EMH)**：股價已充分反映「所有資訊」，包含公司內部未公開的內線消息 (Inside Information)。實證上強式效率並不成立（內線交易法規即為明證）。

## 2. 效率市場假說的實證檢驗與市場異象 (Tests and Anomalies)
- **事件研究法 (Event Study)**：衡量特定事件（如併購宣告、盈餘驚喜）發生前後的**異常報酬 (Abnormal Return, AR)** 與 **累積異常報酬 (Cumulative Abnormal Return, CAR)**。
  公式：AR_t = r_t - E(r_t)，其中預期報酬 E(r_t) 通常由 Ch.7 的 CAPM 或指數模型估算。若市場具半強式效率，CAR 應在宣告日當天瞬間跳躍並於之後維持水平。
- **常見市場異象 (Market Anomalies)**：
  1. **本益比效應 (P/E Effect)**：低本益比股票投資組合的風險調整後報酬顯著高於高本益比組合。
  2. **規模效應 (Small-Firm / Size Effect)**：小型股長期平均報酬高於 CAPM 預測（呼應 Ch.7 的 Fama-French SMB 因子）。
  3. **被忽視公司效應 (Neglected-Firm Effect)** 與 **流動性效應 (Liquidity Effect)**：缺乏分析師追蹤或流動性較差的股票往往提供較高風險溢酬。
  4. **盈餘公告後漂移 (Post-Earnings-Announcement Drift, PEAD)**：盈餘驚喜公佈後，股價並未瞬間完全反映，而是在隨後數週持續朝同方向緩慢漂移（直接挑戰半強式效率）。
- **共同基金績效實證**：統計顯示多數主動型股票基金在扣除管理費後，長期無法穩定擊敗大盤指數（如 S&P 500 或 Wilshire 5000），支持市場高度有效率的觀點。
- **缺陷與限制**：EMH 假設所有投資人皆完全理性且套利無限制（Limits to Arbitrage），無法解釋市場泡沫（如網路泡沫）或過度反應等心理現象（引出 Chapter 9 行為財務學）。
