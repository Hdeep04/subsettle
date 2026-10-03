# SubSettle
![SubSettle logo](assets/logo.png)

Turning analog bank-transfer subscriptions into auto-reconciled stablecoin billing.

## Overview

SubSettle is a payments tool for subscription businesses that still rely on manual bank transfers instead of card or direct-debit billing. It creates a recurring stablecoin payment schedule per subscriber, automatically reconciles incoming payments against billing cycles, and consolidates merchant payouts through a multisig treasury.

## Problem

Subscription businesses without card or direct-debit infrastructure must manually confirm each bank transfer against subscriber due dates. This manual reconciliation delays service activation, creates operational overhead, and contributes to customer churn.

## Solution

SubSettle assigns each subscriber a recurring stablecoin payment identifier. Incoming payments are automatically matched to the correct billing cycle, missed or late payments are flagged with grace-period logic, and reconciled funds are consolidated into a multisig-controlled treasury for secure merchant payout.

## Features (MVP)

- Subscriber onboarding with a recurring stablecoin payment identifier
- Automated matching of payments to billing cycle due dates
- Late/missed payment alerting and grace period logic
- Multisig-controlled merchant payout consolidation
- Simple merchant dashboard for subscription status overview

## Tech Stack

- Anchor (Solana smart contracts)
- Clockwork / cron jobs for billing cycle scheduling
- Squads multisig for merchant payout control
- SPL stablecoins for payment settlement
- Postgres for off-chain subscription and billing state
- React dashboard for merchant-facing status overview

## How It Works

```
Subscriber --(stablecoin payment)--> Payment Identifier (on-chain)
                                         |
                                         v
                        Clockwork cron: match to billing cycle
                                         |
                          +--------------+--------------+
                          |                             |
                     On time                      Late / missed
                          |                             |
                          v                             v
                 Reconcile cycle              Alert + grace period
                          |
                          v
              Squads multisig treasury
                          |
                          v
                 Merchant payout
```

## Roadmap

- Add dunning/retry logic and customer notifications
- Integrate with existing subscription management platforms
- Support fiat off-ramp for merchants needing local currency payout

## Pitch

- [Pitch deck (PDF)](docs/pitch.pdf)
- [Pitch script](docs/pitch-script.md)

## Team

- Name / role — placeholder
- Name / role — placeholder
- Name / role — placeholder

Built for the Colosseum hackathon (Solana and other chains).

---

🎬 Pitch video: [docs/pitch-video.mp4](docs/pitch-video.mp4)
