# Investment Portfolio Management

**User:** Tahsin Yusuf Bennur (RX3464) | **Broker:** Zerodha Kite
**Style:** Long-term value investor (12-24 months) | **Primary concern:** Avoid valuation traps

---

## Kite MCP Connection

**ALWAYS connect first:**
1. `mcp__Kite__login` → User clicks auth link
2. `mcp__Kite__get_profile` → Verify connection

---

## Key Files

- **`investment_journal.md`** - Decision log (Date | Stock | Decision | Rationale | GTT IDs | Follow-ups)
- **`portfolio_companies/[SYMBOL].md`** - Complete analysis history per stock (append new dated sections at top)

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

---

## Workflow (Every Analysis)

1. Read `investment_journal.md` for context
2. Get holdings → quotes → news → fundamentals
3. Provide recommendation with specific ₹ amount
4. If executing:
   - Place GTT orders (BUY: limit 0.4-0.5% above trigger | SELL: limit 0.5% below trigger)
   - Update `investment_journal.md` (Date | Stock | Decision | Rationale in 1 para | GTT IDs | Follow-ups)
   - APPEND new dated section to `portfolio_companies/[SYMBOL].md` (compare vs previous analysis)

---

## GTT Orders - Active (2026-02-05)

| Stock | Type | Trigger | Qty | Limit | Trigger ID |
|-------|------|---------|-----|-------|------------|
| KPITTECH | SELL | ₹900 | 110 | ₹895 | 305672287 |
| MANKIND | SELL | ₹1,950 | 100 | ₹1,945 | 305578263 |
| INDIGO | SELL | ₹4,500 | 22 | ₹4,490 | 305631403 |
| WABAG | BUY | ₹1,150 | 20 | ₹1,155 | 305665451 |
| WABAG | SELL | ₹1,000 | 64 | ₹995 | 305665456 |

**⚠️ After WABAG buy executes:** Update stop-loss to 84 shares

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

## Communication Style

- Crisp, data-driven (no superlatives like "amazing", "incredible")
- Specific numbers, dates, percentages
- Tables for comparisons
- No emojis unless requested
- Sources: Always include URLs when using WebSearch

---

## Common Mistakes to Avoid

- Don't place GTT without checking holdings first
- Update stop-loss quantity after position changes
- Check earnings dates before setting follow-ups (Q4: April-May, Q1: July-Aug)
- Include Trigger IDs in journal
- Always verify day change % before buy recommendations

---

**Last Updated:** 2026-02-05
