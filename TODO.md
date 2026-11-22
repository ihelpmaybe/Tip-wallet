# TODO — Tip-wallet

PulseChain **Android soft wallet** (EIP-681, PulseX). Public face: this repo.

Program: [pulse-trezor ROADMAP § TIP](https://github.com/ihelpmaybe/pulse-trezor/blob/main/ROADMAP.md) · [END-TO-END Layer 4b](https://github.com/ihelpmaybe/pulse-trezor/blob/main/END-TO-END.md)

Hardware wallets are **Desk’s job** until TIP2.

Program tests: [TESTING.md](https://github.com/ihelpmaybe/pulse-trezor/blob/main/TESTING.md)

## TEST — Tip (smoke / fuzz / pen / full)

### Smoke
- [ ] Fresh install + update-over-install (no wipe)
- [ ] Create / restore wallet
- [ ] Receive + send once (testnet preferred)
- [ ] PulseX quote → swap once
- [ ] EIP-681 opens with correct chain/amount

### Fuzz
- [ ] Malformed EIP-681 / QR / deep links
- [ ] Bad amounts, tokens, RPC errors
- [ ] Registry import fuzz (SYNC); reject seed-like fields
- [ ] CI time-boxed fuzz job

### Pen
- [ ] Seed never in logs/analytics/AI prompts
- [ ] Backup verify flow; clipboard hygiene
- [ ] Sideload APK checksum published
- [ ] Clear-sign PulseChain (not ETH mislabel)
- [ ] Pen report before Play/sideload “stable” tag

### Full bar
- [ ] Android × Graphene × release channel matrix
- [ ] Gate T green before ACCEPTANCE Gate 2

## TIP0 — Source of truth
- [x] Locate full Tip app source on disk / private remote — **not on GH; not under pulse-trezor-org** (see [TIP0-source.md](./TIP0-source.md))
- [x] Decide: keep this repo face-only **for now**; pick A (private app repo) or B (push here) when path known
- [ ] Document build / sideload release steps — blocked on source
- [ ] Versioned APK update channel — blocked on source

## TIP1 — Align with Desk
- [ ] Same Pulse RPC defaults (369)
- [ ] Shared token list starter (HEX, PLSX, INC, …)
- [ ] Shared safety copy (seed, verify address/amount/chain)
- [ ] Optional Testnet V4 (943) notes stay in Settings
- [ ] **Backup verify** (seed check quiz) — soft-wallet E2E
- [ ] **Address book** (align with Desk)
- [ ] Fee / stuck-tx UX parity notes with Desk

## TIP2 — Hardware (later)
- [ ] Spike Trezor Connect on Android (after Desk A1 proven)
- [ ] Safe 7 / Suite-mobile Connect flow notes
- [ ] Keep soft-seed path as default; HWW opt-in

## TIP3 — Cross-product / mobile↔desktop
- [ ] Link bunker register (hexican-rescue) when live
- [ ] Link guides (pulse-trezor-guides)
- [ ] Same receive-address story as Desk (BIP44 account 0)
- [ ] Import/export watch-only registry (SYNC1)
- [ ] QR / deep-link pair with Desk (SYNC2) — no seed transfer
- [ ] Shared token/RPC pack from `pulse-trezor-platform`

## TIP4 — Distribution / OS
- [ ] Sideload channel hygiene (update-over-install warning stays)
- [ ] **GrapheneOS** install + hardened notes (high ROI)
- [ ] F-Droid / direct APK channel notes
- [ ] Play Store path (when ready)
- [ ] **iOS (Apple)** port — after Android+SYNC solid
- [ ] English-only → more locales later

## TIP5 — AI / MPC (optional surfaces)
- [ ] Explain EIP-681 / QR before pay (AI3)
- [ ] MPC recovery opt-in when platform MPC2 lands — never default silent

## TIP6 — Adoption
- [ ] Shareable “Pay me on Pulse” / EIP-681 profile link
- [ ] Creator tip-kit entry (see ADOPTION.md)
- [ ] Graphene / Obtainium install one-pager link in-app
- [ ] Keep Pulse-first identity (don’t dilute into multi-chain cloud)

## BONUS — after Android+SYNC solid

- [ ] Locales after English
- [ ] Play Store listing polish (screenshots / Pulse-first copy)
- [ ] MPC recovery **marketing** only after MPC2 works (no vapor)
- [ ] WalletConnect on Tip (optional; Desk WC is enough longer)
- [ ] iOS already TIP4 — keep as bonus until Gate 2
- [ ] **No** multi-chain Tip cloud (explicit non-goal)

## Already true (don’t regress)
- [x] PulseChain-first (not multi-chain cloud)
- [x] EIP-681 scan / pay
- [x] PulseX swap (Tip fee 0%) — keep first-class (core app)
- [ ] ProveX deep link / USDC awareness (core fiat ramp)
- [x] Self-custody seed on device
- [x] No HWW / WalletConnect in v1 on purpose
