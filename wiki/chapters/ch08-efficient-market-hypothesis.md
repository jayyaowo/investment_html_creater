---
title: Ch.08 效率市場假說 (EMH)
en_title: "Chapter 8: The Efficient Market Hypothesis"
type: chapter
chapters:
  - ch08
tags:
  - emh
  - market-efficiency
  - anomalies
  - event-study
status: active
sources:
  - raw/ch08/ch08-notes.md
updated: 2026-11-22
---

# Ch.08 效率市場假說 (The Efficient Market Hypothesis, EMH)

## 本章核心問題與學習地圖

延續 [[ch07-capm-and-apt|Ch.07 CAPM 與多因子定價理論]] 中「均衡市場下 $\alpha_i = 0$」的推論，本章從資訊反映速度的角度追問：**市場價格是否已經充分且即時地反映所有資訊？主動選股、技術分析或基本面分析真的能持續擊敗大盤嗎？**

```mermaid
flowchart LR
    RW["隨機漫步 (Random Walk)<br/>股價僅對未預期新資訊反應"] --> V["EMH 三種形式<br/>(弱式 / 半強式 / 強式)"]
    V --> ES["實證檢驗<br/>(事件研究法 AR/CAR ＋ 共同基金績效)"]
    ES --> AN["市場異象挑戰<br/>(P/E / Size / 流動性 / PEAD)"]
    AN -.-> BF["理性與無套利限制破口<br/>(銜接 Ch.09 行為財務學)"]
```

---

## 本章核心知識拆解

### 1. 隨機漫步與效率市場三種形式
- 詳見 [[efficient-market-hypothesis|效率市場假說 (EMH)]]
- 重點摘要：
  - 任何可預測的資訊皆會立即被理性交易者反映於當下股價，故未來價格變動僅取決於不可預測的新資訊，呈現**隨機漫步 (Random Walk)**。
  - 依資訊集合涵蓋範圍由窄到廣分為**弱式效率**（否定技術分析）、**半強式效率**（否定基本面分析持續超額報酬）與**強式效率**（實證不成立，內線交易法規即明證）。

### 2. 事件研究法、市場異象與基金實證
- 詳見 [[event-study-and-anomalies|事件研究法與市場異象]]
- 重點摘要：
  - 透過**事件研究法 (Event Study)** 計算異常報酬 $AR_t$ 與累積異常報酬 $\text{CAR}$ 檢驗半強式效率（若有效率，CAR 應於宣告日瞬間跳躍後維持水平）。
  - 四大市場異象：本益比效應 (P/E Effect)、規模效應 (Size Effect)、被忽視公司與流動性效應，以及直接挑戰半強式效率的**盈餘公告後漂移 (PEAD)**。
  - 主動型共同基金扣除管理費後長期多無法穩定打敗大盤指數（如 S&P 500、Wilshire 5000），顯示市場仍具備高度競爭效率。

---

## 核心公式速查

$$
AR_t = r_t - E(r_t), \qquad \text{CAR} = \sum_{t=t_1}^{t_2} AR_t
$$

---

## 跨章節脈絡銜接

- **承接 [[ch07-capm-and-apt|Ch.07 CAPM 與多因子定價理論]]**：事件研究法需仰賴 [[capm|CAPM]] 或 [[single-index-model|單因子指數模型]] 估算正常預期報酬 $E(r_t)$；規模效應等異象直接呼應 [[fama-french-three-factor|Fama-French 三因子模型]]；共同基金實證則是對 [[beta-and-alpha|$\alpha_i = 0$]] 的直接檢驗。
- **銜接 [[ch09-behavioral-finance|Ch.09 行為財務學與技術分析]]**：EMH 仰賴「完全理性」與「無套利限制」兩大前提，無法解釋資產泡沫與 PEAD 漂移，直接開啟 Ch.09 [[behavioral-finance-and-prospect-theory|行為財務學與展望理論]] 及 [[limits-to-arbitrage|套利限制]] 之反動（完整論戰對照見 [[emh-vs-behavioral-finance|效率市場假說與行為財務學比較]]）。
