# Investment Portfolio Management

**User:** Tahsin Yusuf Bennur (RX3464) | **Broker:** Zerodha Kite
**Style:** Long-term value investor (12-24 months) | **Primary concern:** Avoid valuation traps

---

## Kite MCP Connection

**ALWAYS connect first:**
1. `mcp__Kite__login` → User clicks auth link
2. `mcp__Kite__get_profile` → Verify connection

---

## ⚠️ TRADING SAFETY RULES - CRITICAL

**NEVER place any GTT, market orders, or any trading orders using Kite MCP without EXPLICIT USER APPROVAL.**

### Order Placement Protocol:

1. **Analysis & Recommendation Phase:**
   - Perform full analysis
   - Provide clear recommendation with reasoning
   - Suggest specific GTT levels (trigger price, limit price, quantity)
   - **STOP HERE - DO NOT EXECUTE**

2. **User Approval Required:**
   - Wait for user to explicitly say: "place the order", "execute", "go ahead", or similar confirmation
   - User may modify parameters (price, quantity, timing)
   - User may decline and choose to place manually

3. **Execution Phase (ONLY after approval):**
   - Place GTT/orders using Kite MCP tools
   - Confirm execution with trigger IDs
   - Update investment journal with GTT IDs

**Why This Rule Exists:**
- Real money at stake - mistakes are costly
- User may want to review, sleep on it, or time the entry differently
- Market conditions change rapidly - recommendations may become stale
- User has final authority over their capital allocation

**Exceptions:** NONE. Always require explicit approval for any order placement.

---

## Key Files

- **`investment_journal.md`** - Decision log (Date | Stock | Decision | Rationale | GTT IDs | Follow-ups)
- **`portfolio_companies/[SYMBOL].md`** - Complete analysis history per stock (append new dated sections at top)
- **`PORTFOLIO_SNAPSHOT.md`** - Real-time portfolio data (LOCAL ONLY - in .gitignore, not pushed to GitHub)

---

## Decision Criteria

### ACCUMULATE
- Strong fundamentals (order book 3x+ for EPC, revenue CAGR >15%)
- Reasonable valuation (P/E within 30% of peers)
- Sector tailwinds (structural, not cyclical)

### HOLD
- Mixed signals or awaiting Q4/Q1 results for clarity
- Small profit/loss, need more data

### SELL
- **Valuation trap:** P/E >40x + margin compression 2+ quarters
- **Red flag:** Premium >30% vs peers without justification
- Stop-loss triggered

### PARTIAL SELL (Book Profits)
- **Price-Fundamentals disconnect:** Stock up 30%+ but revenue/margins declining
- **Large gains in short time:** >40% gain in <2 months warrants profit booking
- **Strategy:** Sell 50%, hold 50% with stop-loss (de-risk while keeping upside)

---

## Workflow (Every Analysis)

1. Read `investment_journal.md` for context
2. Get holdings → quotes → news → fundamentals
3. Provide recommendation with specific ₹ amount
4. **⚠️ STOP and get user approval before placing any orders** (see Trading Safety Rules above)
5. If user approves execution:
   - Place GTT orders (BUY: limit 0.4-0.5% above trigger | SELL: limit 0.5% below trigger)
   - Update `investment_journal.md` (Date | Stock | Decision | Rationale in 1 para | GTT IDs | Follow-ups)
   - APPEND new dated section to `portfolio_companies/[SYMBOL].md` (compare vs previous analysis)
   - Update `PORTFOLIO_SNAPSHOT.md` if requested (full portfolio refresh)

---

## New Company Analysis Workflow

**Trigger:** User types just a company name or ticker (e.g., "SUNPHARMA", "RELIANCE", "Tata Motors")

**Automatic Process:**
1. **Search Instrument:**
   - Use `mcp__Kite__search_instruments` to find exact trading symbol
   - Get current price using `mcp__Kite__get_quotes`
   - Get OHLC data using `mcp__Kite__get_ohlc`

2. **Gather Fundamental Data:**
   - Use `WebSearch` for:
     - "SYMBOL screener.in" → Financial metrics (ROCE, ROE, margins, debt/equity, FCF)
     - "SYMBOL annual report FY24" → Qualitative insights, management commentary
     - "SYMBOL moat competitive advantage" → Business analysis
     - "SYMBOL latest results Q3 FY26" → Recent performance
     - "SYMBOL peer comparison" → Relative valuation

3. **Follow Template:**
   - Use structure from `fundamental_analysis.md`
   - Complete ALL 10 sections systematically
   - Focus on FACTS (financials) vs INTERPRETATION (assessment) vs OPINION (judgment)

4. **Create Analysis File:**
   - Filename: `portfolio_companies/[SYMBOL]_Comprehensive_Analysis.md`
   - Structure:
     ```markdown
     # [COMPANY NAME] - Comprehensive Analysis

     **Analysis Date:** [Date]
     **Current Market Price (CMP):** ₹[X]
     **Exchange:** NSE/BSE
     **Sector:** [X]

     ---

     [Follow all 10 sections from fundamental_analysis.md]
     ```

5. **Key Requirements:**
   - Use tables for all data presentation
   - Include 10-year historical data where available (minimum 5-year)
   - Cite data vintage (FY24, Q3 FY26, TTM)
   - Calculate intrinsic value range with margin of safety
   - Provide specific price targets (Bear/Base/Bull)
   - Include technical levels (support/resistance, RSI, MACD)
   - End with clear RECOMMENDATION: BUY/HOLD/AVOID/SELL

6. **Quality Checks:**
   - ✅ All financial metrics filled (ROCE, ROE, margins, FCF)
   - ✅ Moat analysis completed (6 types rated)
   - ✅ Management quality assessed
   - ✅ Valuation vs historical median
   - ✅ Valuation vs peers (3+ comparisons)
   - ✅ Risk matrix completed
   - ✅ Quick reference card at end

**Example Usage:**
```
User: "RELIANCE"
→ Auto-triggers full analysis
→ Creates portfolio_companies/RELIANCE_Comprehensive_Analysis.md
→ Returns summary with recommendation
```

---

## Key Metrics (User's Benchmarks)

**Pharma:** EBITDA >24% | P/E <35x (Sun/Cipla/Dr.Reddy's benchmark)
**EPC/Infra:** Order book >3x revenue | EBITDA >13%
**IT Services:** EBITDA >20% | P/E <35x
**Airlines:** Watch forex exposure, load factor, operational efficiency

---

## Position Sizing

- Banks/Blue chips: ₹40-100k
- Mid-caps: ₹30-50k
- ETFs: ₹50-75k

---

## Portfolio Snapshot Generation

**When to generate:** User requests "portfolio snapshot" or "portfolio file"

**Process:**
1. `mcp__Kite__get_holdings` - Get all positions
2. `mcp__Kite__get_margins` - Get cash/margin data
3. Create `PORTFOLIO_SNAPSHOT.md` with:
   - Overall portfolio summary (value, P&L, returns)
   - Asset allocation by sector
   - Top gainers/losers
   - Detailed holdings table
   - Active GTT orders
   - Sector-wise performance

**Important:** File stays LOCAL only (in .gitignore)

---

## Communication Style

- Crisp, data-driven (no superlatives like "amazing", "incredible")
- Specific numbers, dates, percentages
- Tables for comparisons
- No emojis unless requested
- Sources: Always include URLs when using WebSearch

---

## Common Mistakes to Avoid

- **⚠️ CRITICAL: NEVER place orders without explicit user approval** - Always wait for user confirmation before executing any GTT/market orders
- Don't place GTT without checking holdings first
- Update stop-loss quantity after position changes
- Check earnings dates before setting follow-ups (Q4: April-May, Q1: July-Aug)
- Include Trigger IDs in journal
- Always verify day change % before buy recommendations
- **Check if revenue is growing or declining** - Don't assume growth, verify with actual data
- **Update existing analysis files** - Append new dated sections at top of portfolio_companies/[SYMBOL].md files
- **Consider partial profit booking** - When stock up 40%+ but fundamentals deteriorating

---

## Git & Privacy Management

**Repository:** https://github.com/marcusaurelius02/fundamental_analysis
**Account:** Personal (javed02@gmail.com) - NOT work account

### Files to NEVER push (in .gitignore):
- `PORTFOLIO_SNAPSHOT.md` - Real-time holdings with quantities/prices
- `.env` files - API keys/credentials
- `*.csv` - Raw data files

### Safe to push:
- Analysis methodology and templates
- Stock analysis files (portfolio_companies/*.md)
- Investment journal (decisions/rationale)
- CLAUDE.md configuration

### Privacy principle:
- **Share methodology, not real-time positions**
- Analysis files show thinking process (good for learning)
- Portfolio snapshot shows actual money (keep private)

---

**Last Updated:** 2026-02-09 (Added: Critical Trading Safety Rule - NEVER place orders without explicit user approval)
