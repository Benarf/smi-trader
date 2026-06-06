# SMI Trading Bot

A complete standalone HTML trading bot for Deriv API with real-time technical analysis.

## Features

- **SMI (Stochastic Momentum Index)**: Periods (10, 3, 3, 3)
- **LSMA (Least Squares Moving Average)**: Period 25
- **Automated Trading**: CALL/PUT strategy based on indicator crossovers

## Strategy Logic

| Condition | Action |
|-----------|--------|
| LSMA UP + SMI crosses above Signal below -50 | CALL (Rise) |
| LSMA DOWN + SMI crosses below Signal above +50 | PUT (Fall) |

## Dynamic Expiry

- **Hyper Reversal** (|SMI| >= 75): 6 ticks
- **Standard** (50 <= |SMI| < 75): 9 ticks

## Installation

1. Download trading-bot (4).html
2. Serve via HTTP server (WebSocket required)
3. Configure API credentials and start trading

## Quick Start

```bash
python -m http.server 8080
# Open: http://localhost:8080/
```

## License

MIT
