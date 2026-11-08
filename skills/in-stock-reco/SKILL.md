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

## Advanced valuation and investment decision framework

Run this stage for every qualifying stock and include its results in the report output. Valuation is a second-stage assessment, not an extra fundamental screening gate: do not silently remove an otherwise qualifying company merely because a method is unsuitable or data are unavailable. Clearly distinguish calculated values, sourced vendor values, estimates, and unavailable items. Never fabricate inputs or present illustrative assumptions as company facts.

### Method selection and applicability

Select valuation methods based on the business model, sector, cash-flow characteristics, and data quality. Mark each parameter in the output as **Calculated**, **Conditional**, or **N/A**, with a brief reason where conditional or unavailable.

1. **Intrinsic value per share — required.** Estimate intrinsic value using at least one defensible, sector-appropriate method. Where possible, triangulate with a second independent method. Show the method, valuation date, key assumptions, equity/share-count bridge, and value per share. If no reliable estimate can be made, state that explicitly rather than inventing a value.
2. **DCF — conditional by suitability.** Use FCFF discounted at WACC for non-financial operating businesses when cash flows can be reasonably forecast. FCFE or dividend discount models may be more suitable in selected cases. Do not force a conventional FCFF/WACC model onto banks, insurers, or other financial institutions; use sector-appropriate approaches such as excess-return/residual-income, dividend discount, or justified P/B–ROE frameworks. For cyclical businesses, normalize margins, earnings, and cash flows across the cycle. Explain why DCF is unsuitable when omitted.
3. **Bull, base, and bear scenarios — required.** Provide three valuation cases with explicit operating and valuation assumptions, estimated value per share, and upside/downside versus the current market price. Avoid false precision; explain major scenario drivers.
4. **PEG — conditional.** Calculate P/E divided by the expected annual EPS growth rate expressed as a percentage (for example, 20 / 15 = 1.33). State the growth horizon and source. Use only when earnings and growth are positive, meaningful, and reasonably sustainable. Mark N/A for losses, volatile/rebounding earnings, or unreliable growth estimates. Treat PEG thresholds as heuristics, not buy/sell rules.
5. **Free cash flow yield — conditional.** For non-financial companies, calculate a clearly defined FCF yield, preferably unlevered FCFF / enterprise value or levered FCFE / market capitalization; state which definition is used and keep numerator/denominator consistent. Explain treatment of leases, exceptional capex, and working-capital swings where material. Do not apply conventional FCF yield mechanically to banks/insurers; use relevant sector measures instead.
6. **Margin of safety — required when a credible intrinsic value is available.** Calculate (intrinsic value per share − current share price) / intrinsic value per share × 100. Show negative values when price exceeds estimated value. Identify which intrinsic-value estimate is used and disclose uncertainty. Do not imply that a positive margin guarantees safety.
7. **Historical valuation comparison — required where meaningful.** Compare current P/E (or the sector-appropriate multiple) with the company's own historical range, preferably across a representative cycle and using consistent earnings definitions. Include the lookback period and source. Explain structural changes and exclude distorted periods where justified. For cyclical companies, use normalized earnings rather than relying on peak/trough P/E.
8. **Peer valuation comparison — required where meaningful.** Compare with a relevant peer set using consistent dates, financial periods, accounting bases, and multiples. Include at least P/E where meaningful and sector-specific multiples such as P/B, EV/EBITDA, EV/sales, or price-to-book as appropriate. Explain peer selection and material differences in growth, leverage, profitability, and business mix. Do not call a stock cheap solely because its multiple is below peers.
9. **Sensitivity analysis — conditional on model use.** For DCF or other assumption-driven intrinsic valuation, show how value changes under reasonable changes to the key drivers. For DCF, at minimum provide a WACC/terminal-growth sensitivity table when those inputs are used. For non-DCF methods, test the assumptions that materially drive value. If unavailable, explain why.
10. **WACC — conditional on valuation method.** Calculate and disclose WACC only when using an FCFF DCF or another method that requires it. Show cost of equity, cost of debt, tax rate, capital weights, risk-free rate, equity risk premium, and beta/source where data permit. Use India-appropriate, dated market inputs (including an appropriate Indian government-security yield) and disclose assumptions. Do not use WACC as the discount rate for FCFE, banks, or insurers by default; use the discount rate appropriate to the selected method.

### Sector-specific valuation guidance

- **Banks and lenders:** Prefer P/B with sustainable ROE, residual-income/excess-return, or dividend approaches; assess asset quality, capital adequacy, and credit costs. Avoid conventional FCFF and generic FCF yield.
- **NBFCs:** Use P/B, sustainable ROE/ROA, residual-income, and asset-quality/credit-cost analysis as appropriate. Explain differences between lending models.
- **Insurance:** Consider embedded value, value of new business (VNB), relevant multiples, and dividend/residual-income methods where data support them; do not force industrial-company DCF metrics.
- **Manufacturing, IT, FMCG, pharma, and other operating companies:** Use FCFF DCF/WACC when cash flows are forecastable, supported by peer and historical multiples, FCF yield, PEG when meaningful, and scenario/sensitivity analysis.
- **Cyclical sectors (for example metals, commodities, autos, and cement):** Normalize earnings, margins, capex, and working capital over a cycle; use mid-cycle multiples and scenario analysis. Avoid interpreting peak or trough P/E in isolation.
- **Holding companies, REITs/InvITs, and other special structures:** Use NAV, sum-of-the-parts, AFFO/distribution or other structure-appropriate methods; explain any discount/premium and avoid unsuitable generic ratios.

### Required valuation output for every qualifying stock

Add a dedicated **Advanced Valuation** section and include, in the main comparison table or a linked per-company valuation table, at least:

- Current share price and price date; valuation date and currency (INR).
- Selected valuation method(s), intrinsic value per share, and method applicability/status.
- Bear/base/bull value per share and implied upside/downside for each case.
- Margin of safety (or negative margin where applicable).
- PEG and its EPS-growth horizon/source, or N/A with reason.
- FCF yield, its exact definition, or N/A with reason.
- Current versus historical valuation multiple and lookback period.
- Peer-group valuation comparison and peer set.
- WACC and key assumptions when applicable.
- Sensitivity analysis results when applicable.
- Key assumptions, data gaps, valuation confidence (High/Medium/Low with rationale), and principal risks.

Use dated, India-relevant inputs and cite primary filings/company reports and reliable market-data sources. State whether figures are consolidated or standalone and keep periods/bases consistent. Do not use fixed valuation weights universally; if combining methods, justify the weights by sector and disclose the calculation. The output must always show every listed parameter, even when marked conditional or N/A, so users can see what was assessed and why. Conclude with a valuation assessment (attractive / fairly valued / expensive / insufficient evidence), separate from the fundamental-screen pass, and do not present it as personalized financial advice or a guaranteed return.

### Preserve the original report parameters

The Advanced Valuation section supplements the original screening and company-analysis output; it never replaces it. Every triggered report must retain all original columns and supporting analysis: rank; company name; NSE/BSE symbol; industry/business description; market capitalization in INR crore; stock segment; trailing ROE; trailing P/E; five-year revenue CAGR and its period; net profit margin; diluted trailing EPS in INR; promoter and promoter-group holding; promoter pledge/encumbrance and ownership-change notes; institutional ownership where available; ETF holder count; mutual-fund scheme count; verification status; sources; reasons for inclusion; material risks; and the six annual revenue observations covering five fiscal-year intervals. Keep the original fundamental screening rules and ownership checks visible. Add the Advanced Valuation outputs as additional columns or a clearly linked per-company section. Do not omit an original parameter merely because the new valuation section is present or because a value is unavailable; show N/A and explain the limitation. The final report must therefore contain both the complete original fundamental/ownership output and all ten valuation parameters for every qualifying stock.
