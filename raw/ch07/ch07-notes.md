# Chapter 7: Capital Asset Pricing and Arbitrage Pricing Theory (CAPM 與多因子定價理論)

## 1. 資本資產定價模型 (Capital Asset Pricing Model, CAPM)
- **核心假設**：所有投資人皆為理性均值-變異數最佳化者、單一投資期間、同質預期 (Homogeneous Expectations)、市場完全競爭無交易成本與稅負、可按無風險利率自由借貸。
- **市場投資組合 (Market Portfolio, M)**：在均衡狀態下，所有投資人持有的最佳風險性組合 P* 皆相同，即為包含市場所有風險資產的市場投資組合 M。此時連接 r_f 與 M 的切線稱為 **資本市場線 (Capital Market Line, CML)**。
- **Beta 係數 (Beta)**：衡量個別資產 i 對市場投資組合 M 的系統性風險敏感度。
  公式：beta_i = Cov(r_i, r_M) / sigma_M^2
- **證券市場線 (Security Market Line, SML)**：CAPM 的核心定價方程式，描述任何個別資產或投資組合的期望報酬與系統性風險 beta 的線性關係：
  E(r_i) = r_f + beta_i * [E(r_M) - r_f]
- **Alpha (Jensen's Alpha)**：衡量資產實際期望報酬與 SML 理論均衡報酬的差額（錯誤定價程度）。
  alpha_i = E(r_i) - { r_f + beta_i * [E(r_M) - r_f] }。在完全均衡市場下，所有資產的 alpha 應為 0。

## 2. 指數模型 (Single-Index Model)
- 為解決 Markowitz 模型共變異數估計量過大的問題，將報酬分解為系統性市場因子與公司特有殘差：
  R_i = alpha_i + beta_i * R_M + e_i （其中 R_i = r_i - r_f 為超額報酬）。
- 風險拆解：總變異數 sigma_i^2 = beta_i^2 * sigma_M^2 + sigma^2(e_i)（系統性風險 + 公司特有風險）。參數估計量從 O(n^2) 大幅降至 3n + 2 個。

## 3. CAPM 實證缺陷與多因子模型 (Multifactor Models & Fama-French)
- **CAPM 缺陷與市場異象 (Anomalies)**：實證研究發現單一市場因子 beta 無法完全解釋股票橫斷面報酬，存在**規模效應 (Size Effect，小型股報酬高於 CAPM 預測)** 與 **價值效應 (Value Effect，高帳面市值比 B/M 股票報酬較高)**。
- **Fama-French 三因子模型 (Fama-French Three-Factor Model)**：在市場因子外加入規模因子 (SMB, Small Minus Big) 與價值因子 (HML, High Minus Low)：
  R_it = alpha_i + beta_iM * R_Mt + beta_iSMB * SMB_t + beta_iHML * HML_t + e_it

## 4. 套利定價理論 (Arbitrage Pricing Theory, APT)
- **核心原理**：基於「無套利原則 (No-Arbitrage Principle)」與多因子報酬生成過程。若存在兩個系統性風險曝險相同但期望報酬不同的充分多角化投資組合，投資人可透過做多高報酬、放空低報酬組合進行無風險套利，直到價格回歸均衡。
- **與 CAPM 的比較**：APT 不需要「市場投資組合 M 必須有效率」或「常態分配／二次效用函數」等嚴苛假設，且允許存在多個系統性風險因子；但 APT 僅適用於「充分多角化投資組合」（無法保證個別股票零定價誤差），且理論本身未指定具體的風險因子為何。
