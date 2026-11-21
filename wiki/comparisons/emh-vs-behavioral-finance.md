---
title: 效率市場假說與行為財務學比較
en_title: EMH vs. Behavioral Finance Comparison
type: comparison
chapters:
  - ch08
  - ch09
tags:
  - emh
  - behavioral-finance
  - anomalies
  - comparison
status: active
sources:
  - raw/ch08/ch08-notes.md
  - raw/ch09/ch09-notes.md
updated: 2026-11-22
---

# 效率市場假說與行為財務學比較 (EMH vs. Behavioral Finance)

## 比較背景

[[ch08-efficient-market-hypothesis|Ch.08 效率市場假說 (EMH)]] 與 [[ch09-behavioral-finance|Ch.09 行為財務學]] 構成當代金融學最核心的學派論戰：一方主張市場價格已即時且正確地反映所有資訊，另一方則從人類心理偏誤與現實套利障礙出發，解釋為何市場會反覆出現泡沫、反應不足與過度反應。

---

## 核心維度對照表

| 比較維度 | 效率市場假說 ([[efficient-market-hypothesis\|EMH]]) | 行為財務學 ([[behavioral-finance-and-prospect-theory\|Behavioral Finance]]) |
| :--- | :--- | :--- |
| **投資人假設** | **完全理性**：正確執行貝氏更新，依據期望效用最大化決策 | **有限理性**：存在系統性資訊處理誤差（過度自信、保守主義、代表性偏誤）與行為偏誤 |
| **效用與風險偏好** | 依**最終財富水準 $W$** 評估，全程風險趨避（凹性效用） | **展望理論**：依相對參考點之**財富變動量 $\Delta W$** 評估；損失規避、獲利區風險趨避、損失區風險愛好 |
| **套利機制假設** | **套利無限制**：理性套利者會迅速抹平任何錯誤定價 | **存在 [[limits-to-arbitrage\|套利限制]]**：基本面、執行成本、模型與噪音交易者風險阻礙價格回歸 |
| **對市場異象之詮釋** | 傾向視為「尚未納入定價模型的系統性風險補償」（如 [[fama-french-three-factor\|Fama-French 因子]]）或資料探勘假象 | 視為系統性心理偏誤導致的錯誤定價（如保守主義解釋 [[event-study-and-anomalies\|PEAD]]、代表性偏誤解釋反轉） |
| **對技術分析之態度** | **弱式效率即否定技術分析**：歷史價量無預測力 | 承認處分效果與參考點錨定可解釋支撐／壓力位，但實務仍須警惕交易成本與資料探勘偏誤 |
| **投資實務核心啟示** | 主動選股難長期打敗大盤（基金實證），推崇低成本被動指數化投資 | 提醒投資人克服過度交易、心理帳戶與賣贏抱輸，但仍不代表市場存在輕鬆無風險暴利 |

---

## 考題判別與綜合視角

1. **「價格不完全等於基本面價值」是否等於「散戶能輕鬆賺取超額報酬」？**
   - **否！** 這是 Ch.08 與 Ch.09 交會處最重要的結論。即使行為財務學正確指出錯誤定價存在，但正因為存在 [[limits-to-arbitrage|套利限制]]（如噪音交易者風險導致 Royal Dutch / Shell 價差長期不收斂）與交易成本，主動型共同基金依然難以穩定創造扣除費用後的正 [[beta-and-alpha|$\alpha_i$]]。
2. **四大經典異象的跨章節對應速查**：
   - **PEAD 盈餘公告後漂移**（Ch.08） $\longleftrightarrow$ **保守主義偏誤**（Ch.09，對新資訊更新過慢）。
   - **股價過度反應與反轉** $\longleftrightarrow$ **樣本數忽略與代表性偏誤**（Ch.09，將短期漲跌誤當長期趨勢）。
   - **投資人未做好整體分散**（衝擊 Ch.06 [[markowitz-portfolio-theory|Markowitz]]） $\longleftrightarrow$ **心理帳戶**（Ch.09）。
   - **套牢不賣、小賺就跑** $\longleftrightarrow$ **處分效果**與**展望理論損失規避**（Ch.09）。

---

## 關聯連結
- [[efficient-market-hypothesis|效率市場假說 (EMH)]]
- [[behavioral-finance-and-prospect-theory|行為財務學與展望理論]]
- [[event-study-and-anomalies|事件研究法與市場異象]]
- [[limits-to-arbitrage|套利限制 (Limits to Arbitrage)]]
- [[fama-french-three-factor|Fama-French 三因子模型]]
