---
name: in-stock-reco
description: Research and recommend Indian stocks using fundamental screening, five-year sales growth, promoter ownership, and a consolidated report. Trigger for "provide list of Indian stock", "recommend Indian Stock", and semantically similar requests to list, screen, shortlist, suggest, or recommend Indian stocks, India stocks, or Indian equities, regardless of capitalization or singular/plural wording. Also use for fundamental analysis of Indian stocks covering valuation, profitability, ownership, and fund holdings. For requests covering both Indian and US stocks, use alongside us-stock-reco and report each market separately.
---

# IN Stock Reco

Create a fresh, source-backed Indian stock research report. Apply the user's latest instructions first; otherwise use the defaults below. Carry forward preferences and methods only. Never reuse prior stock selections, company examples, financial figures, dates, or conclusions as current evidence.

## Default screening rules

Require every condition:

- Trailing return on equity (ROE) > 20%.
- Positive trailing price-to-earnings ratio (P/E) < 20.
- Five-year sales/revenue compound annual growth rate (CAGR) > 15%.
- Promoter and promoter-group holding > 50%.

Apply strict inequalities. Do not substitute institutional ownership for promoter holding. Require positive, meaningful equity when interpreting ROE; investigate distorted or anomalous ratios before declaring a pass.

Target up to 20 verified qualifying stocks. Never relax thresholds, silently change the universe, or include unverified candidates to fill the list. Default to Indian operating companies listed on NSE or BSE, deduplicate dual listings, and state exchange coverage and treatment of SME listings. Exclude funds from the stock shortlist.

## Research workflow

1. Browse current sources on every run. Record the research date, market-price date, financial periods, and shareholding reporting dates. Use a consistent price date where available; disclose mixed dates.
2. Discover candidates and examine financial statements with [Tickertape](https://www.tickertape.in/) and [Screener](https://www.screener.in/). Prefer consolidated financials where available; label standalone figures and never mix bases silently.
3. Use [Tijori Finance](https://www.tijorifinance.com/) for business models, products, revenue sources, and industry positioning; [Trendlyne](https://trendlyne.com/) for valuation, estimates, and ownership changes; [TradingView](https://www.tradingview.com/) for price trends; and [Moneycontrol](https://www.moneycontrol.com/) for announcements and news. Verify material inputs against issuer reports and official [NSE](https://www.nseindia.com/) or [BSE](https://www.bseindia.com/) filings. These are preferred sources, not mandatory subscriptions. Attribute opinions and estimates with dates; never invent inaccessible content.
4. Obtain six comparable annual sales/revenue observations covering five full fiscal-year intervals. Calculate CAGR = (latest annual revenue / revenue five fiscal years earlier)^(1/5) - 1. Include the annual revenue series and period labels in the report or appendix. Do not mix annual and trailing revenue, confuse five observations with five intervals, or substitute one-year growth. CAGR above the threshold does not mean each year's growth exceeds it.
5. Verify trailing ROE, reported diluted EPS, trailing P/E, and net profit margin with consistent periods and definitions. If calculating ROE, use trailing profit attributable to ordinary shareholders divided by average attributable equity and disclose the averaging convention. Use net profit divided by revenue for net margin, identifying the profit basis. Label vendor methodology differences. Reconcile restatements, acquisitions, fiscal-year changes, share splits, and units where material. Distinguish operating revenue from other income; explain sector-specific revenue definitions.
6. Verify promoter holding against the latest available quarterly shareholding filing and report its date. Examine promoter pledges or encumbrances, ownership changes, and governance risks. Report institutional ownership as supplementary context when available; it is not a replacement filter. Obtain separate ETF and mutual-fund holder counts where reliable data are accessible, with provider, coverage, and holdings date. For the mutual-fund column, count distinct mutual-fund schemes holding the stock at the latest available holdings date, deduplicating plan or option variants of the same scheme. State whether ETFs are included in the source count. If only a fund-house or AMC count is available, label it explicitly and report the scheme count as unavailable rather than substituting it silently. Do not add counts across reporting periods. Do not confuse scheme counts, fund-house counts, institutional holder counts, and ownership percentages. Report unavailable counts as unavailable, not zero.
7. Assess business model, industry position, growth durability, cash generation, leverage, earnings quality, competitive risks, and valuation relative to relevant peers. Explain when sector accounting makes a ratio less comparable. Price trends may provide entry context, but do not override failed fundamental filters.

## Consolidated report

Open with the applied rules, dates, universe, ranking method, and number of verified passes. Use a transparent ranking supported by evidence; do not present a screener order as a prediction of investment returns.

Provide one comparison table containing all requested parameters:

- Rank, company, exchange symbol, and industry/business description.
- Market capitalization in INR crore and stock segment, using a stated, current Indian classification method.
- Trailing ROE, trailing P/E, five-year revenue CAGR, and the CAGR period.
- Net profit margin, reported diluted trailing EPS in INR, and promoter holding.
- Institutional ownership where available and ETF holder count, with dates or links to a source appendix.
- Mutual fund holdings (scheme count): a dedicated column showing the number of distinct mutual-fund schemes holding the stock, separate from ownership percentages, with the source and holdings date.
- Verification status and sources supporting the row.

Add concise reasons for inclusion and material risks for each stock, plus the annual revenue appendix. State that the result is a research shortlist, with no guaranteed returns or implied suitability for the user's portfolio. Distinguish verified passes from near misses and unresolved candidates; keep the latter outside the qualifying list. Always include the mutual-fund count column; show N/A with the reason when no reliable count is available. Missing holder counts need not disqualify a stock, but missing mandatory filter evidence does. Describe coverage limits without claiming an exhaustive market-wide top 20 unless the research supports that claim. Follow the requested output format; use relevant artifact skills when creating files.
