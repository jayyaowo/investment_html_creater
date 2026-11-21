# 《投資學》知識庫總目錄 (Investments Wiki Index)

> **教材**：Bodie, Kane, Marcus — *Essentials of Investments*
> **架構規範**：詳見專案根目錄 `agents.md` ｜ **操作日誌**：詳見 [[log|wiki/log.md]]
> **最後更新**：2026-11-22

---

## 統計總覽

| 類別 | 目錄 | 頁面數 |
| :--- | :--- | :---: |
| 章節總覽 (Chapters) | `wiki/chapters/` | 6 |
| 財務模型 (Models) | `wiki/models/` | 9 |
| 核心概念 (Concepts) | `wiki/concepts/` | 9 |
| 比較與綜合 (Comparisons) | `wiki/comparisons/` | 3 |
| 圖文 HTML 簡報 (Slides) | `slides/` | 1 |
| 待核對 OCR 項目 | 標記 `needs-review` | 0 |

---

## ⚠️ 待核對清單（OCR 推斷還原）

> 凡在匯入過程中因手機 OCR 殘缺而由 Agent 推斷還原、需對照實體書確認的頁面，皆會列於此處；核對完成後移除。

- *目前尚無待核對項目。*

---

## 1. 章節總覽 (`wiki/chapters/`)

| 章節 | 頁面連結 | 一句話摘要 | 狀態 | 來源數 |
| :--- | :--- | :--- | :---: | :---: |
| Ch.05 | [[ch05-risk-and-return\|Ch.05 風險與報酬]] | 建立單期與多期報酬衡量、總風險與風險溢酬、夏普比率及資本配置線 (CAL) 的基礎架構。 | `active` | 1 |
| Ch.06 | [[ch06-efficient-diversification\|Ch.06 效率多角化與投資組合理論]] | 拆解系統與非系統性風險，透過兩資產相關係數與 Markowitz 效率前緣找出最佳風險組合 $P^*$ 與分離定理。 | `active` | 1 |
| Ch.07 | [[ch07-capm-and-apt\|Ch.07 CAPM 與多因子定價理論]] | 串聯 CAPM (CML/SML/Beta/Alpha)、單因子指數模型、Fama-French 三因子模型與套利定價理論 (APT) 的完整演進。 | `active` | 1 |
| Ch.08 | [[ch08-efficient-market-hypothesis\|Ch.08 效率市場假說 (EMH)]] | 探討隨機漫步、三種效率形式、事件研究法 (AR/CAR)、四大市場異象與共同基金績效實證。 | `active` | 1 |
| Ch.09 | [[ch09-behavioral-finance\|Ch.09 行為財務學與技術分析]] | 從非理性資訊處理、行為偏誤（展望理論）、四大套利限制與技術分析連結系統挑戰 EMH。 | `active` | 1 |
| Ch.10 | [[ch10-bond-prices-and-yields\|Ch.10 債券價格與殖利率]] | 開啟固定收益篇章，涵蓋債券現值定價、價格—殖利率凸性、四大殖利率指標與違約風險／信用利差。 | `active` | 1 |

---

## 2. 財務模型與定價理論 (`wiki/models/`)

> 每個模型頁皆包含核心假設、標準 KaTeX 公式、模型缺陷／限制與前後模型演進連結。

| 模型頁面 | 英文名稱 | 關聯章節 | 一句話摘要 | 狀態 |
| :--- | :--- | :--- | :--- | :---: |
| [[capital-allocation-line\|資本配置線 (CAL)]] | Capital Allocation Line (CAL) | `ch05` | 描述無風險資產與單一既定風險組合 $P$ 構成之完整投資組合的線性風險報酬權衡，斜率為 $S_P$。 | `active` |
| [[markowitz-portfolio-theory\|馬可維茲投資組合理論 (Markowitz)]] | Markowitz Portfolio Selection Model | `ch06` | 透過效率前緣與切線 CAL 求解最佳風險組合 $P^*$ 並導出分離定理；缺陷為 $O(n^2)$ 參數估計量過大。 | `active` |
| [[single-index-model\|單因子指數模型]] | Single-Index Model | `ch07` | 以共同市場因子 $R_M$ 將 Markowitz 估計參數降至 $3n+2$，並將總風險拆解為 $\beta_i^2\sigma_M^2 + \sigma^2(e_i)$。 | `active` |
| [[capm\|資本資產定價模型 (CAPM)]] | Capital Asset Pricing Model (CAPM) | `ch07` | 市場均衡下 $P^*=M$，以 SML 依系統性風險 $\beta_i$ 為個別資產定價；受限於嚴苛假設與規模／價值異象。 | `active` |
| [[fama-french-three-factor\|Fama-French 三因子模型]] | Fama-French Three-Factor Model | `ch07` | 針對 CAPM 實證異象，在市場因子外加入規模因子 (SMB) 與價值因子 (HML) 解釋橫斷面報酬。 | `active` |
| [[apt\|套利定價理論 (APT)]] | Arbitrage Pricing Theory (APT) | `ch07` | 以無套利原則推導多因子均衡定價，放寬 CAPM 假設；但僅保證適用充分多角化組合且未指定具體因子。 | `active` |
| [[efficient-market-hypothesis\|效率市場假說 (EMH)]] | Efficient Market Hypothesis (EMH) | `ch08` | 主張股價即時充分反映資訊並呈隨機漫步（弱式／半強式／強式）；受限於完全理性與無套利限制假設。 | `active` |
| [[behavioral-finance-and-prospect-theory\|行為財務學與展望理論]] | Behavioral Finance and Prospect Theory | `ch09` | 以資訊處理誤差、行為偏誤及展望理論（參考點與損失規避）解釋市場異象與泡沫；缺乏單一定量定價式。 | `active` |
| [[bond-pricing-model\|債券現值定價模型]] | Bond Present Value Pricing Model | `ch10` | 以未來票息與面額折現為債券定價並刻畫凸性與溢／平／折價關係；受限於單一平坦折現率與忽略含權條款。 | `active` |

---

## 3. 核心概念、金融工具與指標 (`wiki/concepts/`)

| 概念頁面 | 英文名稱 | 關聯章節 | 一句話摘要 | 狀態 |
| :--- | :--- | :--- | :--- | :---: |
| [[return-measurement\|報酬率衡量：HPR、算術與幾何平均]] | Return Measurement: HPR, Arithmetic & Geometric Average | `ch05` | 定義單期持有期間報酬率 (HPR)，並比較算術平均（未來單期預測）與幾何平均（真實複利年化）的適用場景與波動差異。 | `active` |
| [[risk-and-risk-premium\|風險、風險溢酬與超額報酬]] | Risk, Risk Premium, and Excess Return | `ch05` | 以機率情境計算 $E(r)$、$\sigma^2$ 與 $\sigma$，並區分事前預期的風險溢酬 $E(r)-r_f$ 與事後實現的超額報酬 $R = r - r_f$。 | `active` |
| [[sharpe-ratio\|夏普比率 (Sharpe Ratio)]] | Sharpe Ratio (Reward-to-Volatility Ratio) | `ch05` | 衡量每承擔一單位總風險 ($\sigma_P$) 所獲得的風險溢酬，在幾何上即為 CAL（均衡下為 CML）的斜率。 | `active` |
| [[systematic-vs-unsystematic-risk\|系統性風險與非系統性風險]] | Systematic vs. Unsystematic Risk | `ch06`, `ch07` | 區分不可分散的市場風險與可多角化消除的公司特有風險，連結兩資產 $\rho < 1$ 降險公式與單因子變異數拆解。 | `active` |
| [[beta-and-alpha\|貝他係數與詹森阿法 (Beta & Alpha)]] | Beta and Jensen's Alpha | `ch07` | 定義系統性風險敏感度 $\beta_i$ 與 SML 錯誤定價指標 $\alpha_i$，並整理低估／高估判別準則與均衡條件 $\alpha_i=0$。 | `active` |
| [[event-study-and-anomalies\|事件研究法與市場異象]] | Event Study and Market Anomalies | `ch08` | 以 $AR_t$ 與 $\text{CAR}$ 檢驗半強式效率，並整理 P/E、規模、被忽視／流動性與 PEAD 盈餘公告後漂移四大異象。 | `active` |
| [[limits-to-arbitrage\|套利限制 (Limits to Arbitrage)]] | Limits to Arbitrage | `ch09` | 解析基本面、執行成本、模型與噪音交易者四大風險（含 Royal Dutch / Shell 案例），說明為何錯誤定價難以消除。 | `active` |
| [[bond-yield-measures\|債券殖利率衡量指標]] | Bond Yield Measures | `ch10` | 比較到期殖利率 (YTM)、當期殖利率、贖回殖利率 (YTC) 與已實現複利報酬率之公式、假設與適用時機。 | `active` |
| [[default-risk-and-credit-spread\|違約風險、信用評等與信用利差]] | Default Risk, Credit Ratings, and Credit Spread | `ch10` | 劃分投資級與投機級信用評等，釐清承諾 YTM 與期望 YTM 差異，並定義公司債信用利差。 | `active` |

---

## 4. 跨章節比較與查詢沉澱 (`wiki/comparisons/`)

| 頁面連結 | 涵蓋主題 | 一句話摘要 | 狀態 |
| :--- | :--- | :--- | :---: |
| [[capm-vs-apt\|CAPM 與 APT 比較]] | `ch07` 資產定價模型 | 從理論基礎、假設強度、因子個數、市場組合角色與適用範圍六大維度完整對照 CAPM 與 APT。 | `active` |
| [[cal-cml-sml-comparison\|CAL、CML 與 SML 比較]] | `ch05`–`ch07` 三條定價與配置線 | 釐清三條線之橫軸風險尺規（$\sigma$ vs. $\beta$）、斜率公式、適用標的與「個別股票落於 CML 下方但在 SML 線上」高頻考點。 | `active` |
| [[emh-vs-behavioral-finance\|效率市場假說與行為財務學比較]] | `ch08`–`ch09` 理性效率 vs. 行為財務論戰 | 從投資人理性、效用函數、套利有效性、市場異象詮釋與技術分析態度五大維度系統對照兩大學派。 | `active` |

---

## 5. 圖文講義型 HTML 簡報 (`slides/`)

| 簡報檔案 | 對應章節／主題 | 產生日期 |
| :--- | :--- | :---: |
| `slides/ch07-capm-and-apt.html` | Ch.07 CAPM 與多因子定價理論複習（含 Ch.05–06 前置公式與全符號精解，12 頁雙模式） | 2026-11-22 |
