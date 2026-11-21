---
title: 債券殖利率衡量指標
en_title: Bond Yield Measures (YTM, Current Yield, YTC, Realized Return)
type: concept
chapters:
  - ch10
tags:
  - fixed-income
  - ytm
  - current-yield
  - ytc
  - reinvestment-risk
status: active
sources:
  - raw/ch10/ch10-notes.md
updated: 2026-11-22
---

# 債券殖利率衡量指標 (Bond Yield Measures)

## 核心定義

在固定收益投資中，單看票面利率無法反映債券的真實報酬率。依據債券是否含提前贖回條款、是否持有至到期，以及票息再投資利率是否變動，投資學定義了四種核心殖利率指標：**到期殖利率 (YTM)**、**當期殖利率 (Current Yield)**、**贖回殖利率 (YTC)** 與**已實現複利報酬率 (Realized Compound Return)**。

---

## 標準 LaTeX 公式與符號定義

### 1. 到期殖利率 (Yield to Maturity, YTM)
使債券未來所有票息與到期面額現值恰好等於當前市價 $P_B$ 的內部報酬率 (IRR)，即求解下列方程式中之 $y$：

$$
P_B = \sum_{t=1}^{T} \frac{C}{(1 + y)^t} + \frac{F}{(1 + y)^T}
$$

### 2. 當期殖利率 (Current Yield)
衡量債券當年度票息收入相對於當前市價的現金收益率（**未計入**到期時買價與面額之間的資本利得或資本損失）：

$$
\text{Current Yield} = \frac{\text{Annual Coupon}}{P_B}
$$

### 3. 贖回殖利率 (Yield to Call, YTC)
針對**可贖回債券 (Callable Bond)**，以第一個可贖回期間 $T_{\text{call}}$ 與贖回價格 (Call Price, $P_{\text{call}}$) 取代到期期間 $T$ 與面額 $F$，求解內部報酬率 $y_c$：

$$
P_B = \sum_{t=1}^{T_{\text{call}}} \frac{C}{(1 + y_c)^t} + \frac{P_{\text{call}}}{(1 + y_c)^{T_{\text{call}}}}
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $P_B$ | 債券當前市場價格 |
| $C,\, \text{Annual Coupon}$ | 每期票息金額、全年度票息總額 |
| $F,\, T$ | 債券面額 (Par Value) 與剩餘到期期數 |
| $y$ | **到期殖利率 (YTM)**：持有至到期且所有票息以 $y$ 再投資時之內部報酬率 |
| $P_{\text{call}},\, T_{\text{call}},\, y_c$ | 可贖回債券之贖回價格、至首個可贖回日之期數與**贖回殖利率 (YTC)** |

---

## 四大殖利率指標比較與適用情境

| 指標 | 核心衡量的報酬 | 隱含假設／限制 | 最佳適用情境 |
| :--- | :--- | :--- | :--- |
| **到期殖利率 (YTM)** | 票息收入 ＋ 到期資本利得／損失（年化複利） | **強假設**：持有至到期，且每期收到的票息皆能以**相同的 YTM** 進行再投資 | 評估一般不含權、持有至到期的標準債券 |
| **當期殖利率 (Current Yield)** | 僅衡量當期現金票息收益率 | 忽略到期時的資本利得（折價債）或資本損失（溢價債） | 快速估算短期現金配息率（溢價債時 $\text{Current Yield} > \text{YTM}$；折價債反之） |
| **贖回殖利率 (YTC)** | 持有至第一個可贖回日並領取贖回價之報酬率 | 假設發行人會於首個可贖回日提前贖回 | **當市場利率大幅下跌、債券市價高於贖回價時**，發行人極可能提前贖回再融資，此時 YTC 比 YTM 更具參考價值 |
| **已實現複利報酬率 (Realized Compound Return)** | 納入**實際再投資利率變動**後的真實多期持有複利報酬率 | 須已知或設定各期票息實際再投資利率 | **解決 YTM 再投資率固定的假設缺陷**，衡量投資人跨期真正到手的複利績效 |

---

## 關聯連結
- **所屬章節**：[[ch10-bond-prices-and-yields|Ch.10 債券價格與殖利率]]
- **基礎定價模型**：[[bond-pricing-model|債券現值定價模型]]
- **相關概念**：
  - [[default-risk-and-credit-spread|違約風險、信用評等與信用利差]]（進一步區分承諾 YTM 與期望 YTM）
  - [[return-measurement|報酬率衡量：HPR、算術與幾何平均]]（已實現複利報酬率即跨期幾何年化概念在債券上的應用）
