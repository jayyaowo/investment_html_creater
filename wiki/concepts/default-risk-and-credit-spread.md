---
title: 違約風險、信用評等與信用利差
en_title: Default Risk, Credit Ratings, and Credit Spread
type: concept
chapters:
  - ch10
tags:
  - fixed-income
  - default-risk
  - credit-ratings
  - credit-spread
status: active
sources:
  - raw/ch10/ch10-notes.md
updated: 2026-11-22
---

# 違約風險、信用評等與信用利差 (Default Risk & Credit Spread)

## 核心定義

不同於無違約風險的政府公債，公司債面臨發行人無法如期支付票息或償還本金的**違約風險 (Default Risk / Credit Risk)**。市場透過專業機構之**信用評等 (Credit Ratings)** 衡量違約機率，並在債券定價上要求高於同到期日公債殖利率的**信用利差 (Credit Spread / Default Premium)** 作為風險補償。

---

## 標準 LaTeX 公式與符號定義

### 1. 信用利差 (Credit Spread / Default Premium)

$$
\text{Credit Spread} = \text{Stated YTM}_{\text{corp}} - \text{YTM}_{\text{Treasury}}
$$

### 2. 承諾殖利率與期望殖利率之關係（定性與情境加權）
設違約機率為 $p_D$、違約時之債權回收率為 $RR$，則債券的**期望殖利率 (Expected YTM)** 必然嚴格低於假設絕不違約之**承諾殖利率 (Stated YTM)**（只要 $p_D > 0$ 且 $RR < 1$）：

$$
E(\text{YTM}) < \text{Stated YTM}_{\text{corp}}
$$

| 符號 | 經濟意義 |
| :--- | :--- |
| $\text{Stated YTM}_{\text{corp}}$ | **承諾到期殖利率 (Stated / Promised YTM)**：假設公司債「絕不違約」所算出的最大可能殖利率 |
| $\text{YTM}_{\text{Treasury}}$ | 相同到期期間之無風險政府公債到期殖利率 |
| $\text{Credit Spread}$ | **信用利差 (Default Premium)**：公司債承諾 YTM 超過同天期公債 YTM 之差額，用以補償違約風險 |
| $E(\text{YTM})$ | **期望到期殖利率 (Expected YTM)**：將違約機率與違約回收率 (Recovery Rate) 納入加權平均後的真實期望報酬率 |

---

## 信用評等分類與關鍵辨析

### 1. 信用評等兩大等級（Moody's / S&P / Fitch）

| 等級分類 | S&P / Fitch 評級 | Moody's 評級 | 風險與市場特性 |
| :--- | :---: | :---: | :--- |
| **投資級債券 (Investment-Grade)** | $\text{AAA}$ 至 $\text{BBB}$ | $\text{Aaa}$ 至 $\text{Baa}$ | 違約機率較低，多數機構投資人（退休基金、保險公司）主要配置標的 |
| **投機級／高收益債券 (Speculative-Grade / Junk Bonds)** | $\text{BB}$ 以下 | $\text{Ba}$ 以下 | 違約風險顯著偏高，須提供高票息與寬信用利差吸引投資人 |

### 2. 承諾 YTM vs. 期望 YTM（核心考點）
- **承諾 YTM (Stated YTM)**：只是契約上「萬一完全不違約」時投資人能拿到的**上限報酬**；當公司財務惡化、債券價格暴跌時，承諾 YTM 會大幅飆升，切勿誤以為真實預期報酬也同等暴增。
- **期望 YTM (Expected YTM)**：將「準時履約（機率 $1-p_D$）」與「違約後僅收回部分殘值（機率 $p_D$，依回收率 Recovery Rate 計算）」加權平均，才是投資人真正應納入投資組合決策的期望報酬。

---

## 關聯連結
- **所屬章節**：[[ch10-bond-prices-and-yields|Ch.10 債券價格與殖利率]]
- **同章關聯**：
  - [[bond-pricing-model|債券現值定價模型]]
  - [[bond-yield-measures|債券殖利率衡量指標]]
- **跨章節連結**：[[risk-and-risk-premium|風險、風險溢酬與超額報酬]]（公債殖利率為無風險利率 $r_f$ 基準，信用利差即違約風險溢酬）
