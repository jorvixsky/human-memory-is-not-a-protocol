# Human Memory Is Not a Protocol  
### Ownership-first ENS renewal reminders

ENS domains are digital identity. They secure wallets, websites, emails, and reputations.  
Yet today, ENS offers no reliable way to remind owners to renew them.

**Human Memory Is Not a Protocol** is a public-good project that solves a simple but costly problem: ENS owners forgetting to renew their domains and silently losing them to bots.

_This is a summary of the [project long description](https://hackmd.io/@jorvixsky/Hk-pXaqm-g). Soon I'll begin coding!_

## What this is

An ownership-first ENS reminder service that sends **real reminders** (email, for now) to **actual domain owners** before expiration and throughout the grace period.

- No calendar exports  
- No guessing  
- No reminders for domains you don’t own  

If the chain says you own it, it counts.

## How it works

1. **Wallet-based login**  
   Users authenticate with the wallet that owns the ENS domain.

2. **On-chain ownership verification**  
   ENS domain ownership and expiration data are fetched directly from on-chain data via The Graph (ENS subgraph).

3. **Explicit configuration**  
   Users select which domains to monitor and explicitly opt in to reminders.

4. **Reliable reminders**  
   Email notifications are sent at sensible defaults before expiration and during the grace period.

## Why this approach

- Prevents abuse by bots and squatters (no ownership = no reminders)  
- Avoids storing personal data on-chain  
- Prioritizes correctness and reliability over premature decentralization  
- Designed as a sustainable public good  

This project starts with boring, reliable infrastructure and moves toward decentralization only where it meaningfully improves safety and trust.

## Privacy stance

Reminder delivery is handled off-chain by design.  
Storing personal data on-chain would be irresponsible and, in many jurisdictions, illegal.

Privacy-first alternatives are an open problem and are explored as a dedicated research milestone rather than rushed into production.

## Project status

- MVP work is **starting very soon**  
- Initial focus: shipping a reliable, ownership-verified reminder system  
- Architecture, assumptions, and trade-offs will be documented transparently  

## Scope

This tool is **not**:
- A domain sniping tracker  
- A speculative analytics product  
- A reminder system for non-owners  

It exists for one reason only: **to help ENS owners not lose their domains by accident**.
