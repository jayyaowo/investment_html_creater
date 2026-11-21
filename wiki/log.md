# 《投資學》知識庫操作日誌 (Wiki Log)

> 本檔案採 **Append-Only（僅向尾端追加）** 紀錄格式，每一筆操作統一以 `## [YYYY-MM-DD] <action> | <title>` 開頭（`<action>` 限填：`init` / `ingest` / `query` / `lint` / `slides` / `fix`），方便未來使用 `grep "^## \[" wiki/log.md` 快速檢索時間軸。

---

## [2026-11-21] init | 初始化《投資學》LLM Wiki 知識庫架構
- **動作**：建立專案最高工作憲法 `agents.md`、完整資料夾階層（`raw/`、`wiki/chapters/`、`wiki/models/`、`wiki/concepts/`、`wiki/comparisons/`、`slides/`、`assets/`）、`.gitignore`、初始總目錄 `wiki/index.md` 與本操作日誌 `wiki/log.md`。
- **核心約定**：
  - 領域分類型目錄架構 + 英文 `kebab-case` 全域唯一檔名 + Obsidian `[[slug|顯示名稱]]` 雙向連結。
  - 彈性精簡模板（強制 YAML Frontmatter、KaTeX 相容 LaTeX 公式與符號表、模型演進與限制雙向連結）。
  - `raw/` 絕對唯讀；OCR 公式自動還原並對不確定處標記 `⚠️ 待核對`。
  - 嚴格執行「先提案、後動工」兩階段 Ingest 流程。
  - 繁體中文（台灣術語）+ 首見中英並列 + BKM (*Essentials of Investments*) 原書標準符號。

## [2026-11-21] ingest | Ch.05 風險與報酬 (Risk and Return: Past and Prologue)
- **來源**：`raw/ch05/ch05-notes.md`
- **新增**：
  - `[[ch05-risk-and-return|Ch.05 風險與報酬]]`
  - `[[capital-allocation-line|資本配置線 (CAL)]]`
  - `[[return-measurement|報酬率衡量：HPR、算術與幾何平均]]`
  - `[[risk-and-risk-premium|風險、風險溢酬與超額報酬]]`
  - `[[sharpe-ratio|夏普比率 (Sharpe Ratio)]]`
- **更新**：`wiki/index.md`
- **公式修復 / 待核對**：所有 8 組核心公式（HPR、算術平均、幾何平均、期望報酬、變異數/標準差、風險溢酬與超額報酬、夏普比率、完整投資組合與 CAL 直線方程式）皆已還原為標準 BKM 符號與 KaTeX 語法；無 `⚠️ 待核對` 項目。

## [2026-11-21] ingest | Ch.06 效率多角化 ＆ Ch.07 CAPM 與多因子定價理論
- **來源**：`raw/ch06/ch06-notes.md`、`raw/ch07/ch07-notes.md`
- **新增（11 頁）**：
  - Chapters：`[[ch06-efficient-diversification|Ch.06 效率多角化與投資組合理論]]`、`[[ch07-capm-and-apt|Ch.07 CAPM 與多因子定價理論]]`
  - Models：`[[markowitz-portfolio-theory|馬可維茲投資組合理論]]`、`[[single-index-model|單因子指數模型]]`、`[[capm|資本資產定價模型 (CAPM)]]`、`[[fama-french-three-factor|Fama-French 三因子模型]]`、`[[apt|套利定價理論 (APT)]]`
  - Concepts：`[[systematic-vs-unsystematic-risk|系統性風險與非系統性風險]]`、`[[beta-and-alpha|貝他係數與詹森阿法 (Beta & Alpha)]]`
  - Comparisons：`[[capm-vs-apt|CAPM 與 APT 比較]]`、`[[cal-cml-sml-comparison|CAL、CML 與 SML 比較]]`
- **更新（雙向演進回填 + 索引）**：
  - `[[capital-allocation-line|資本配置線 (CAL)]]`、`[[ch05-risk-and-return|Ch.05 風險與報酬]]`、`[[sharpe-ratio|夏普比率 (Sharpe Ratio)]]`、`[[risk-and-risk-premium|風險、風險溢酬與超額報酬]]`、`wiki/index.md`
- **公式修復 / 待核對**：所有 11 組核心公式（兩資產組合、Markowitz 參數量、Beta、SML、Jensen's Alpha、單因子指數模型與風險拆解、Fama-French 三因子、APT 多因子定價式）皆已還原為 BKM 標準符號與 KaTeX 語法；無 `⚠️ 待核對` 項目。

## [2026-11-21] fix | 升級 agents.md：確立通用 HTML 簡報生成 Graph 工作流 (SOP 4)
- **更新**：`agents.md`（SOP 4）
- **核心規格**：建立 8 節點狀態機（N1 檢索 → N2 大綱 → N3 大綱自審[上限2次] → N4 人類審核暫停關卡 → N5 講義稿 → N6 單一自包含現代學術簡約風 HTML → N7 公式與數據零誤差審查[上限2次] → N8 交付與同步）；支援簡報鍵盤翻頁與一鍵切換連續講義／列印 PDF 模式；審查報告於對話輸出並於 `wiki/log.md` 留存精簡紀錄。

## [2026-11-22] slides | Ch.07 CAPM 與多因子定價理論複習簡報（含 Ch.05–06 前置公式與符號精解）
- **輸出**：`slides/ch07-capm-and-apt.html`
- **來源頁**：`[[ch07-capm-and-apt]]`、`[[capm]]`、`[[single-index-model]]`、`[[fama-french-three-factor]]`、`[[apt]]`、`[[beta-and-alpha]]`、`[[capm-vs-apt]]`、`[[cal-cml-sml-comparison]]`、`[[risk-and-risk-premium]]`、`[[sharpe-ratio]]`、`[[capital-allocation-line]]`、`[[systematic-vs-unsystematic-risk]]`、`[[markowitz-portfolio-theory]]`
- **審查摘要**：N3 自審通過（重試 1 次，由 10 頁優化為 12 頁）；N7 零誤差審查核對 26 組公式區塊與 12 頁符號數據通過（重試 1 次，修復 P04 殘留 wikilink、P03 參數精確值與 P10 APT 展開項一致度）

## [2026-11-22] fix | 強化 agents.md 簡報 Graph 規範（護眼暖紙色系＋KaTeX 橫向大括號防變形檢查）
- **更新**：`agents.md`（SOP 4.2 N7 審查基準、SOP 4.3 渲染與視覺規格）、`slides/ch07-capm-and-apt.html`
- **新增永久防呆規則**：
  1. 全面採用護眼暖紙色系（`#E9E4D8` / `#F4F0E6`），N7 檢查禁止於螢幕樣式出現純白 `#FFFFFF`。
  2. 凡 `\underbrace` / `\overbrace` 內含單字元或窄項目，強制加上 `\hspace{0.75em}`～`\hspace{0.85em}` 維持扁平括號造型，雙欄長公式須用 `\begin{aligned}` 換行，並列入 N7 必檢項目。
  3. 明訂數學式使用 `\lt` / `\gt` 防 HTML 誤判、Mermaid 先展開渲染再切投影模式防塌陷。

## [2026-11-22] ingest | Ch.08 效率市場假說 ＆ Ch.09 行為財務學 ＆ Ch.10 債券價格與殖利率
- **來源**：`raw/ch08/ch08-notes.md`、`raw/ch09/ch09-notes.md`、`raw/ch10/ch10-notes.md`
- **新增（11 頁）**：
  - Chapters：`[[ch08-efficient-market-hypothesis|Ch.08 效率市場假說 (EMH)]]`、`[[ch09-behavioral-finance|Ch.09 行為財務學與技術分析]]`、`[[ch10-bond-prices-and-yields|Ch.10 債券價格與殖利率]]`
  - Models：`[[efficient-market-hypothesis|效率市場假說 (EMH)]]`、`[[behavioral-finance-and-prospect-theory|行為財務學與展望理論]]`、`[[bond-pricing-model|債券現值定價模型]]`
  - Concepts：`[[event-study-and-anomalies|事件研究法與市場異象]]`、`[[limits-to-arbitrage|套利限制]]`、`[[bond-yield-measures|債券殖利率衡量指標]]`、`[[default-risk-and-credit-spread|違約風險、信用評等與信用利差]]`
  - Comparisons：`[[emh-vs-behavioral-finance|效率市場假說與行為財務學比較]]`
- **更新（跨章節雙向回填 + 索引）**：
  - `[[ch07-capm-and-apt]]`、`[[capm]]`、`[[fama-french-three-factor]]`、`[[markowitz-portfolio-theory]]`、`[[apt]]`、`[[beta-and-alpha]]`、`wiki/index.md`
- **公式修復 / 待核對**：所有 6 組核心公式（$AR_t$、$\text{CAR}$、債券現值級數式與年金因子式、當期殖利率、信用利差）及展望理論價值函數凹凸性特徵皆已還原為標準 BKM 符號與 KaTeX 語法；面額金額規範書寫為 `USD 1,000`；無 `⚠️ 待核對` 項目。
