# Chapter 10: Bond Prices and Yields (債券價格與殖利率)

## 1. 債券特性與基本定價 (Bond Characteristics and Pricing)
- **核心要素**：面額 (Par Value / Face Value, F，通常為 $1,000)、票面利率 (Coupon Rate)、到期期間 (Maturity, T)。
- **債券現值定價公式**：債券價格等於未來各期票息 (C) 與到期面額 (F) 按市場折現率 r 折現的總和：
  P_B = sum_{t=1}^{T} [ C / (1 + r)^t ] + [ F / (1 + r)^T ]
  或利用年金現值因子表示：P_B = C * [ (1 - (1 + r)^(-T)) / r ] + F / (1 + r)^T
- **價格與殖利率的反向關係**：當市場要求報酬率 r 上升時，債券價格 P_B 下降，且呈現「凸性 (Convexity)」——利率下跌帶來的價格漲幅大於等幅利率上升造成的價格跌幅。
  - 溢價債券 (Premium Bond)：票面利率 > 殖利率，P_B > F
  - 平價債券 (Par Bond)：票面利率 = 殖利率，P_B = F
  - 折價債券 (Discount Bond)：票面利率 < 殖利率，P_B < F

## 2. 債券殖利率衡量指標 (Bond Yields)
- **到期殖利率 (Yield to Maturity, YTM)**：使債券未來所有現金流量現值等於當前市價 P_B 的內部報酬率 (IRR)。隱含假設：所有收到的票息皆能以相同的 YTM 進行再投資。
- **當期殖利率 (Current Yield)**：年票息除以當前債券市價，公式：Current Yield = Annual Coupon / P_B（未計入到期時的資本利得或損失）。
- **贖回殖利率 (Yield to Call, YTC)**：針對可贖回債券 (Callable Bond)，計算持有至第一個可贖回日並領取贖回價格 (Call Price) 的報酬率。當利率大幅下跌、債券價格高於贖回價時，YTC 比 YTM 更具參考價值。
- **已實現複利報酬率 (Realized Compound Return)**：考量實際再投資利率變動後的真實多期持有報酬率（解決 YTM 再投資率固定的假設缺陷）。

## 3. 違約風險與債券定價 (Default Risk and Bond Pricing)
- **信用評等 (Credit Ratings)**：由 Moody's、S&P、Fitch 評估違約機率，分為投資級債券 (Investment-Grade，BBB/Baa 以上) 與投機級／高收益債券 (Speculative-Grade / Junk Bonds)。
- **承諾殖利率 vs. 期望殖利率 (Stated YTM vs. Expected YTM)**：
  - 承諾 YTM 是假設債券「絕不違約」所算出的最大可能殖利率。
  - 期望 YTM 則是將違約機率與違約回收率 (Recovery Rate) 納入加權平均後的真實期望報酬率。
- **信用利差 (Default Premium / Credit Spread)**：公司債承諾 YTM 與同到期日無風險公債 YTM 之間的差額，用以補償投資人承擔的信用風險。
