# Investment Portfolio - Fundamental Analysis

**Owner:** Tahsin Yusuf Bennur (RX3464)
**Broker:** Zerodha Kite
**Strategy:** Long-term value investing with fundamental analysis
**Focus:** Avoid valuation traps, protect capital with stop-losses

---

## 📁 Folder Structure

```
fundamental_analysis/
├── README.md                    ← You are here
├── CLAUDE.md                    ← Auto-loaded instructions for Claude
├── investment_journal.md        ← Decision log with GTT orders
│
└── portfolio_companies/         ← Detailed analysis per stock
    ├── KPITTECH.md              ← IT Services - Automotive Software
    ├── MANKIND.md               ← Pharmaceuticals
    ├── INDIGO.md                ← Airlines
    └── WABAG.md                 ← Water Infrastructure / EPC
```

---

## 🎯 What This Folder Does

This is your **investment command center** for:
1. **Tracking decisions** - All buy/sell/hold calls logged with rationale
2. **Analyzing companies** - Deep fundamental analysis per stock
3. **Managing risk** - GTT stop-losses documented
4. **Following up** - Calendar reminders for earnings reviews

---

## 📊 Current Portfolio (as of 2026-02-05)

| Stock | Decision | Position | P&L | GTT Order |
|-------|----------|----------|-----|-----------|
| **WABAG** | ACCUMULATE ⭐⭐⭐⭐ | 64→84 shares | -4.38% | Buy @ ₹1,150, Stop @ ₹1,000 |
| **INDIGO** | HOLD ⭐⭐⭐ | 22 shares | +3.14% | Stop @ ₹4,500 |
| **MANKIND** | HOLD ⭐⭐⭐ | 100 shares | -8.96% | Stop @ ₹1,950 |
| **KPITTECH** | HOLD ⭐⭐⭐ | 110 shares | -15.96% | Stop @ ₹900 |

---

## 🚀 Quick Start

### For Claude Code:
1. **Auto-loads** `CLAUDE.md` at session start
2. **Connect** to Kite MCP (login required each session)
3. **Check** `investment_journal.md` for current positions
4. **Follow** documented workflow automatically

### For User:
1. Open Claude Code in this folder
2. Say: "Check my portfolio" or "Analyze [STOCK]"
3. Claude follows the documented process
4. Get analysis → Make decision → GTT orders placed → Journal updated

---

## 📝 Key Files Explained

### `investment_journal.md`
**Purpose:** Quick decision log
**Contains:** Date | Stock | Decision | Position | Rationale (1 para) | GTT IDs | Follow-up dates

**Example Entry:**
```
2026-02-05 | KPITTECH | HOLD
Position: 110 shares @ ₹1,151, Current: ₹967 (-15.96%)
Rationale: Margin compression concerns but undervalued...
GTT: Stop-loss at ₹900 (ID: 305672287)
Next Review: Q4 FY26 results (April-May)
```

### `portfolio_companies/[STOCK].md`
**Purpose:** Complete analysis history per stock
**Contains:** Multiple dated analyses showing evolution over time

**Benefits:**
- Track how thesis evolved
- Compare predictions vs actual results
- Learn from past decisions
- Build investment case over time

### `CLAUDE.md`
**Purpose:** Auto-loaded project instructions (official Claude Code convention)
**Contains:** User profile, Kite MCP workflow, decision criteria, active GTT orders
**Why:** Claude Code automatically reads this at session start - no manual loading needed

---

## 🔄 Standard Workflow

```
Request Analysis → Get Holdings → Market Data → Research News →
Fundamental Analysis → Recommendation → Execute GTT →
Update Journal → Append to Stock File → Set Follow-ups
```

---

## 📅 Upcoming Reviews

**February 2026:**
- WABAG Q3 results (Feb 5-10) - Watch margins & order book

**April-May 2026:**
- MANKIND Q4 results - CRITICAL: Margin recovery needed
- INDIGO Q4 results - Check forex losses & operations
- KPITTECH Q4 results - CRITICAL: Margin expansion needed
- WABAG Q4 results - Full year performance

**July 2026:**
- Q1 FY27 results for all tracked positions

---

## 🎯 Investment Framework

### ACCUMULATE when:
- Strong fundamentals (order book, revenue CAGR >15%)
- Reasonable valuation (P/E within 30% of peers)
- Sector tailwinds (structural, not cyclical)
- Multiple analyst BUY ratings
- Temporary weakness = opportunity

### HOLD when:
- Mixed signals or awaiting clarity
- Small profit/loss, unclear direction
- Need next quarter results
- Stop-loss in place for protection

### SELL when:
- Valuation trap (high P/E + declining margins for 2+ quarters)
- Fundamentals deteriorating
- Stop-loss triggered
- Better opportunities elsewhere

---

## 🛡️ Risk Management

**Stop-Loss Strategy:**
- Set at -10% to -15% from average price
- Always place after buying/accumulating
- Update quantity after position changes
- Document Trigger IDs in journal

**Position Sizing:**
- Banks/Blue chips: ₹40-100k per position
- Mid-caps: ₹30-50k per position
- ETFs: ₹50-75k per position

---

## 🔗 Integrations

**Kite MCP (Model Context Protocol):**
- Real-time holdings, positions, orders
- Market data (LTP, OHLC, quotes)
- GTT order management
- Historical data

**WebSearch:**
- Latest news and earnings
- Analyst ratings and reports
- Sector outlook

---

## 📂 Archive

**old_work/** folder contains:
- Previous Python scripts
- Old analysis reports
- Development files
- Sentiment analysis system
- Swing trading system

Not actively used, kept for reference.

---

## 💡 Pro Tips

1. **Monthly habit:** Ask Claude to review all positions and check follow-up dates
2. **After earnings:** Tell Claude when results announced, it will update analysis
3. **Quarterly review:** Request review of all holdings every 3 months
4. **Before buying:** Always analyze the stock first, never buy without analysis

---

## 📊 Key Metrics by Sector

- **Banking:** P/E 15-25x | NIM, Asset Quality, Loan Growth
- **IT Services:** P/E 20-30x | Margins >20%, Revenue Growth >10%
- **Pharma:** P/E 25-35x | EBITDA >24%, R&D Pipeline
- **EPC/Infra:** P/E 15-25x | Order Book 3x+ revenue, Margins >13%
- **Airlines:** P/E varies | Load Factor, Yield, Forex Exposure

---

## 🚨 Red Flags

- P/E >40x with margin compression
- Premium >30% vs peers without justification
- Declining margins for 2+ consecutive quarters
- High debt with negative cash flow
- Promoter pledging/selling shares

---

## ✅ Quality Checklist

Before any recommendation, verify:
- [ ] Read journal for context
- [ ] Get current holdings and P&L
- [ ] Research latest news (within 30 days)
- [ ] Check recent earnings
- [ ] Compare valuation with peers
- [ ] Assess sector outlook
- [ ] Provide specific position sizing
- [ ] Set appropriate stop-loss
- [ ] Update journal with GTT Trigger IDs
- [ ] Set follow-up dates

---

**Last Updated:** 2026-02-05
**Version:** 2.0 - Clean, focused portfolio management

---

**Questions?** Check `CLAUDE.md` for project instructions.
