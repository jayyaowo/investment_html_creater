---
title: 效率市場假說 (EMH)
en_title: Efficient Market Hypothesis (EMH)
type: model
chapters:
  - ch08
tags:
  - emh
  - random-walk
  - market-efficiency
status: active
sources:
  - raw/ch08/ch08-notes.md
updated: 2026-11-22
---

# 效率市場假說 (Efficient Market Hypothesis, EMH)

## 核心直覺

效率市場假說 (Efficient Market Hypothesis, EMH) 認為在競爭激烈的資本市場中，證券價格已迅速且充分地反映所有相關資訊。只要任何資訊具備可預測性，理性投資人便會立即進場交易並瞬間將其納入當前價格；因此，**未來股價變動只能源自「未預期的新資訊 (News)」**，呈現不可預測的**隨機漫步 (Random Walk)**。

---

## 核心假設 (Key Assumptions)

1. **投資人完全理性**：市場參與者能正確處理所有可得資訊並迅速評估證券內含價值。
2. **無套利限制與高度競爭**：即使存在部分非理性投資人，理性套利者也能在無成本、無風險限制下迅速修正任何錯誤定價。
3. **資訊流通充分且即時**：新資訊隨機出現，並能迅速傳導至市場交易價格中。

---

## 效率市場三種形式與投資意涵

| 效率形式 | 股價已充分反映之資訊集合 | 對投資策略的推論 | 實證狀態 |
| :--- | :--- | :--- | :--- |
| **弱式效率 (Weak-Form EMH)** | 所有**歷史市場交易資訊**（過去股價、成交量、報酬率序列） | **技術分析 (Technical Analysis) 無效**，無法藉歷史價量規律賺取超額報酬 | 大致獲實證支持（扣除交易成本後） |
| **半強式效率 (Semistrong-Form EMH)** | 所有**公開可得資訊**（歷史交易資料＋財報、盈餘預測、總經數據、公司治理資訊） | **基本面分析 (Fundamental Analysis) 無法持續**賺取經風險調整後的超額報酬 | 多數情況成立，但面臨 [[event-study-and-anomalies\|PEAD 等異象]] 挑戰 |
| **強式效率 (Strong-Form EMH)** | **所有資訊**，包含公司內部尚未公開的內線消息 (Inside Information) | 連公司內部人也無法藉未公開消息獲利 | **實證不成立**（各國嚴格禁止內線交易之法規即為明證） |

> **包含關係**：強式效率 $\implies$ 半強式效率 $\implies$ 弱式效率（資訊集合層層向外擴張）。

---

## 標準實證檢定指標（事件研究法）

檢驗半強式效率的核心工具為 [[event-study-and-anomalies|事件研究法 (Event Study)]]，透過計算事件日 $t$ 的**異常報酬 (Abnormal Return, $AR_t$)** 與**累積異常報酬 (Cumulative Abnormal Return, $\text{CAR}$)** 觀察資訊反映速度：

$$
AR_t = r_t - E(r_t), \qquad \text{CAR} = \sum_{t=t_1}^{t_2} AR_t
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $r_t$ | 證券於事件期第 $t$ 期之實際實現報酬率 |
| $E(r_t)$ | 依 [[capm\|CAPM]] 或 [[single-index-model\|單因子指數模型]] 估算之正常預期報酬率 |
| $AR_t$ | 第 $t$ 期異常報酬（實際報酬減正常預期報酬） |
| $\text{CAR}$ | 視窗 $[t_1, t_2]$ 內之累積異常報酬；半強式效率下應於宣告日瞬間跳躍並於之後維持水平 |

### 共同基金績效實證
統計實證顯示，絕大多數主動型股票基金在扣除管理費用後，長期無法穩定擊敗大盤基準指數（如 S&P 500 或 Wilshire 5000），顯示要持續創造顯著正 [[beta-and-alpha|$\alpha_i$]] 極為困難，為市場高度有效率提供了有力佐證。

---

## 模型缺陷與限制 (Limitations & Critiques)

1. **完全理性與無套利限制假設過強**：現實投資人常出現認知與行為偏誤，且理性套利者面臨 [[limits-to-arbitrage|套利限制]]（如噪音交易者風險與放空成本），無法即時將價格拉回基本面。
2. **無法解釋系統性市場異象與泡沫**：難以單以理性定價解釋網路泡沫、價格過度反應，以及 [[event-study-and-anomalies|盈餘公告後漂移 (PEAD)]]、本益比效應與規模效應等現象。
3. **聯合假說問題 (Joint Hypothesis Problem)**：檢驗 EMH 時必須同時設定一個正常報酬定價模型（如 CAPM），因此發現異常報酬時，難以區分究竟是「市場無效率」還是「定價模型本身有誤」。

---

## 模型演進鏈 (Model Evolution)

```mermaid
flowchart LR
    CAPM["CAPM 與單因子指數模型<br/>(Ch.07：提供正常報酬基準與 α = 0)"] -->|"作為事件研究檢定基準"| EMH["效率市場假說 (EMH)<br/>(Ch.08：三種效率形式)"]
    EMH -->|"面臨 PEAD / 規模 / 泡沫等異象挑戰"| BF["行為財務學與展望理論<br/>(Ch.09：非理性心理與套利限制)"]
```

- **理論前身 / 依賴基準**：
  - [[capm|資本資產定價模型 (CAPM)]]、[[single-index-model|單因子指數模型]]（提供事件研究之 $E(r_t)$ 基準）
  - [[beta-and-alpha|貝他係數與詹森阿法 (Beta & Alpha)]]（EMH 對應均衡下無法持續獲取正 $\alpha_i$）
- **核心檢驗與挑戰**：
  - [[event-study-and-anomalies|事件研究法與市場異象]]
  - [[behavioral-finance-and-prospect-theory|行為財務學與展望理論]]（從非理性資訊處理與行為偏誤直接挑戰 EMH）
  - [[limits-to-arbitrage|套利限制 (Limits to Arbitrage)]]（說明為何理性資金無法消除錯誤定價）
  - [[emh-vs-behavioral-finance|效率市場假說與行為財務學比較]]
- **所屬章節**：[[ch08-efficient-market-hypothesis|Ch.08 效率市場假說 (EMH)]]
