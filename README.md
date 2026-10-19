# Daily Loss Guard (MetaTrader 5)

Keeps prop-firm and personal accounts from breaking a daily loss limit. It warns as the limit gets close, then closes every position, deletes pending orders, and closes any new trade within about a second until the trading day resets.

https://github.com/user-attachments/assets/0239cd7a-93cb-4e5b-a754-a590416f4d5d

## What it does

- Daily loss limit as a % of the start-of-day balance or equity, or of a fixed account size (prop-firm style)
- Optional overall loss limit from the account size
- Warning at a set share of the limit, with an alert and optional push to the MT5 phone app
- At the trigger: closes all trades and blocks new ones until the day resets
- Its state survives terminal restarts and re-attaching, so it can't be switched off in a weak moment
- On-chart panel: limit used, equity, today's result, the equity level where it acts, and time to reset
- Optional filters by symbol or magic number

## Good to know

- MT5 doesn't let an EA cancel a manual order before it executes, so a blocked trade is closed right after it opens and costs roughly the spread.
- Check your prop firm's exact daily-loss rule and set the reset hour to its server time.

## Get it

The source code isn't public. Message me on Fiverr for a copy, or for a version set up for your firm's rules:
