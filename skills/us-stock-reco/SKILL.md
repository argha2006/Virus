---
name: us-stock-reco
description: Research and recommend US stocks using fundamental screening, five-year revenue growth, institutional ownership, and a consolidated report. Trigger for "provide list of US stock", "recommend US Stock", and semantically similar requests to list, screen, shortlist, suggest, or recommend US, U.S., United States, or American stocks or equities, regardless of capitalization or singular/plural wording. Also use for fundamental analysis of US stocks covering valuation, profitability, ownership, and fund holdings. For requests covering both US and Indian stocks, use alongside in-stock-reco and report each market separately.
---

# US Stock Reco

Create a fresh, source-backed US stock research report. Apply the user's latest instructions first; otherwise use the defaults below. Carry forward preferences and methods only. Never reuse prior stock selections, company examples, financial figures, dates, or conclusions as current evidence.

## Default screening rules

Require every condition:

- Trailing return on equity (ROE) > 20%.
- Positive trailing price-to-earnings ratio (P/E) < 20.
- Five-year revenue compound annual growth rate (CAGR) > 15%.
- Institutional ownership > 50%.

Apply strict inequalities. Institutional ownership is a user-selected screening criterion, not an equivalent measure of promoter control. Do not substitute insider ownership for it. Require positive, meaningful equity when interpreting ROE; investigate distorted or anomalous ratios before declaring a pass.

Target up to 20 verified qualifying stocks. Never relax thresholds, silently change the universe, or include unverified candidates to fill the list. State the universe searched, exchange coverage, and treatment of foreign issuers and depositary receipts. Default to US-domiciled operating companies listed on major US exchanges. Exclude funds from the stock shortlist.

## Research workflow

1. Browse current sources on every run. Record the research date, market-price date, financial periods, and ownership reporting dates. Use a consistent price date where available; disclose mixed dates.
2. Discover candidates with [Finviz](https://finviz.com/). Examine financial statements and statistics with [Stock Analysis](https://stockanalysis.com/) or [Yahoo Finance](https://finance.yahoo.com/).
3. Verify material financial inputs against issuer annual reports and [SEC EDGAR](https://www.sec.gov/edgar/search/). Use [Morningstar](https://www.morningstar.com/) for business quality and valuation perspectives, [Seeking Alpha](https://seekingalpha.com/) for ratings and competing views, and [TradingView](https://www.tradingview.com/) for price trends when useful. These are preferred sources, not mandatory subscriptions. Attribute opinions and ratings with their dates; never invent inaccessible content.
4. Obtain six comparable annual revenue observations covering five full fiscal-year intervals. Calculate CAGR = (latest annual revenue / revenue five fiscal years earlier)^(1/5) - 1. Include the annual revenue series and period labels in the report or appendix. Do not mix annual and trailing revenue, confuse five observations with five intervals, or substitute one-year growth. CAGR above the threshold does not mean each year's growth exceeds it.
5. Verify trailing ROE, reported diluted EPS, trailing P/E, and net profit margin with consistent periods and definitions. If calculating ROE, use trailing net income attributable to common shareholders divided by average common equity and disclose the averaging convention. Use net income divided by revenue for net margin. Label vendor methodology differences. Reconcile restatements, acquisitions, fiscal-year changes, share splits, and currency units where material.
6. Check institutional ownership using dated, documented coverage. Reconcile materially conflicting or anomalous percentages. Also obtain the number of distinct institutional holders with a reported position in each stock for the latest available reporting period. Deduplicate institutional entities within the source coverage; do not add counts across reporting periods. Record the source, reporting date, and whether the count represents reporting managers or another defined institutional entity. Keep this count separate from institutional ownership percentage and from ETF or mutual-fund counts. Obtain separate counts of ETFs and mutual funds holding each stock where reliable data are accessible. Record the provider, coverage, and holdings date. Do not equate institutional holder counts with fund counts, sum overlapping categories, or report missing data as zero.
7. Assess business model, industry position, growth durability, cash generation, leverage, earnings quality, competitive risks, and valuation relative to relevant peers. Explain when sector accounting makes a ratio less comparable. Price trends may provide entry context, but do not override failed fundamental filters.

## Consolidated report

Open with the applied rules, dates, universe, ranking method, and number of verified passes. Use a transparent ranking supported by evidence; do not present a screener order as a prediction of investment returns.

Provide one comparison table containing all requested parameters:

- Rank, company, ticker, and industry/business description.
- Market capitalization in USD and stock segment, using a stated, market-appropriate classification method.
- Trailing ROE, trailing P/E, five-year revenue CAGR, and the CAGR period.
- Net profit margin, reported diluted trailing EPS in USD, and institutional ownership.
- Institutional holders (count): a dedicated column showing the number of institutional holders, separate from institutional ownership (%).
- ETF holder count and mutual-fund holder count, with dates or links to a source appendix.
- Verification status and sources supporting the row.

Add concise reasons for inclusion and material risks for each stock, plus the annual revenue appendix. State that the result is a research shortlist, with no guaranteed returns or implied suitability for the user's portfolio. Distinguish verified passes from near misses and unresolved candidates; keep the latter outside the qualifying list. Always include the institutional-holder count column; show N/A with the reason when no reliable count is available. Missing holder counts need not disqualify a stock, but missing mandatory filter evidence does. Describe coverage limits without claiming an exhaustive market-wide top 20 unless the research supports that claim. Follow the requested output format; use relevant artifact skills when creating files.
