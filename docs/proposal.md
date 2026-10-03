# SubSettle

_Turning analog bank-transfer subscriptions into auto-reconciled stablecoin billing_

## Summary

SubSettle targets subscription businesses that currently rely on manual bank transfers instead of card billing. It creates a recurring stablecoin payment schedule per customer, auto-matches incoming payments to subscription cycles, and uses multisig wallets to manage merchant payouts securely.

## Target users

Subscription businesses (BtoB SaaS, BtoC memberships) still billing via manual bank transfer

## Problem

Subscription businesses without card/direct-debit infrastructure must manually confirm each bank transfer against subscription due dates, delaying service activation and causing churn.

## Solution

SubSettle assigns each subscriber a recurring stablecoin payment identifier, automatically reconciles payments against billing cycles, and flags missed/late payments while consolidating funds via a multisig treasury.

## MVP features

- Subscriber onboarding with recurring stablecoin payment identifier
- Automated matching of payments to billing cycle due dates
- Late/missed payment alerting and grace period logic
- Multisig-controlled merchant payout consolidation
- Simple merchant dashboard for subscription status overview

## Chains

Solana

## Tech

Anchor, Clockwork/cron jobs for billing cycles, Squads multisig, SPL stablecoins, Postgres, React dashboard

## Category

Payments

## Why now

Many SMBs outside card networks still run subscriptions manually via bank transfer; stablecoins plus Solana's speed make automated recurring billing finally feasible for this underserved segment.

## Roadmap

- Add dunning/retry logic and customer notifications
- Integrate with existing subscription management platforms
- Support fiat off-ramp for merchants needing local currency payout
