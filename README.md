# QuantPit — GEX Levels (Free: SPY & QQQ)

TradingView (Pine Script v6) indicator that draws **Call Wall, Put Wall, Gamma Flip & HVL**
on your chart. No TradingView Premium required.

**Free tier:** SPY & QQQ.
**Pro:** ES, MES, NQ, MNQ, SPX & NDX with intraday auto-refresh — see
[quantpit-gex-levels-ninjascript](LINK) (requires QuantPit Pro).

## How it works
This indicator is a **display template** — it does no calculation. It draws the daily
levels you paste in from your QuantPit subscription. Levels are published each session
(pre-open + a midday refresh).

## Setup
1. In TradingView: **Pine Editor → paste `QuantPit_GEX_Levels.pine` → Add to chart.**
2. Put a **SPY** or **QQQ** chart up.
3. Open the indicator settings → **Levels string** → paste today's string from the
   QuantPit feed, e.g.:
   ```
   QPGEX|2026-06-21|SPY,755,750,614,750|QQQ,742.06,705.57,739.12,739.63
   ```
4. The script auto-selects SPY or QQQ from the chart symbol and draws the four levels.
   On any non-SPY/QQQ symbol it shows a **Pro** prompt instead.

## Levels
| Level | Meaning |
|---|---|
| **Call Wall** | Largest call-gamma strike above spot — resistance / pin |
| **Put Wall** | Largest put-gamma strike below spot — support / pin |
| **Gamma Flip** | Dealer long/short-gamma boundary (regime change) |
| **HVL** | Highest-gamma level near spot — the dominant pin |

*Not financial advice.*
