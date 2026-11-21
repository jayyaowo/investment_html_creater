---
title: 事件研究法與市場異象
en_title: Event Study and Market Anomalies
type: concept
chapters:
  - ch08
tags:
  - event-study
  - anomalies
  - pead
  - emh
status: active
sources:
  - raw/ch08/ch08-notes.md
updated: 2026-11-22
---

# 事件研究法與市場異象 (Event Study & Market Anomalies)

## 核心定義

檢驗 [[efficient-market-hypothesis|效率市場假說 (EMH)]]（特別是半強式效率）是否成立，實務與學術界最常採用**事件研究法 (Event Study)** 觀測特定重大資訊公開前後股價的異常反應，同時追蹤各種難以被傳統風險定價模型解釋的長期**市場異象 (Market Anomalies)**。

---

## 標準 LaTeX 公式與符號定義

### 1. 異常報酬 (Abnormal Return, AR)

$$
AR_t = r_t - E(r_t)
$$

### 2. 累積異常報酬 (Cumulative Abnormal Return, CAR)

$$
\text{CAR} = \sum_{t=t_1}^{t_2} AR_t
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $t$ | 相對於事件宣告日 ($t = 0$) 的交易日索引 |
| $r_t$ | 個股於第 $t$ 期之實際實現報酬率 |
| $E(r_t)$ | 第 $t$ 期之正常預期報酬率，通常以 Ch.07 [[capm\|CAPM]] 或 [[single-index-model\|單因子指數模型]] 估算 |
| $AR_t$ | 第 $t$ 期異常報酬（實際報酬扣除基準模型預期報酬之差額） |
| $\text{CAR}$ | 事件視窗 $[t_1, t_2]$ 內異常報酬之累計加總，用於檢驗資訊是否瞬間完全反映 |

### 半強式效率之 CAR 圖形判別
- **完全半強式效率**：$\text{CAR}$ 應在事件宣告日 ($t = 0$) 當天**瞬間跳躍到位**，且在宣告日後 ($t > 0$) 維持**水平不再漂移**。
- **消息提前洩漏**：宣告日前 ($t < 0$) $\text{CAR}$ 便已提前上升或下降。
- **反應不足（漂移）**：宣告日後 ($t > 0$) $\text{CAR}$ 持續朝同方向緩慢攀升或下跌，代表半強式效率受挑戰。

---

## 四大常見市場異象 (Market Anomalies)

| 市場異象 | 實證現象 | 跨章節理論連結 |
| :--- | :--- | :--- |
| **本益比效應 (P/E Effect)** | 低本益比 (P/E) 股票組合之風險調整後報酬顯著高於高本益比組合 | 與價值投資風格高度相關（呼應 [[fama-french-three-factor\|HML 價值因子]]） |
| **規模效應 (Small-Firm / Size Effect)** | 小型股長期平均報酬顯著高於 [[capm\|CAPM]] 預測 | 直接呼應 Ch.07 [[fama-french-three-factor\|Fama-French 三因子模型]] 之 $\text{SMB}$ 因子 |
| **被忽視公司與流動性效應** | 缺乏分析師追蹤（Neglected-Firm）或流動性較差的股票，長期提供較高風險溢酬 | 反映資訊不對稱風險與交易流動性補償 |
| **盈餘公告後漂移 (PEAD)** | 盈餘驚喜公佈後股價未瞬間完全反映，反而在隨後數週持續朝同方向緩慢漂移 | **直接挑戰半強式效率**；Ch.09 [[behavioral-finance-and-prospect-theory\|保守主義偏誤]] 為其核心心理解釋 |

---

## 關聯連結
- **所屬章節**：[[ch08-efficient-market-hypothesis|Ch.08 效率市場假說 (EMH)]]
- **定價基準模型**：[[capm|資本資產定價模型 (CAPM)]]、[[single-index-model|單因子指數模型]]、[[beta-and-alpha|貝他係數與詹森阿法 (Beta & Alpha)]]
- **多因子與行為詮釋**：
  - [[efficient-market-hypothesis|效率市場假說 (EMH)]]
  - [[fama-french-three-factor|Fama-French 三因子模型]]
  - [[behavioral-finance-and-prospect-theory|行為財務學與展望理論]]（保守主義解釋 PEAD）
  - [[emh-vs-behavioral-finance|效率市場假說與行為財務學比較]]
