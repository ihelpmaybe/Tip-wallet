# TODO — Tip-wallet

PulseChain **Android soft wallet** (EIP-681, PulseX). Public face: this repo.

Program: [pulse-trezor ROADMAP § TIP](https://github.com/ihelpmaybe/pulse-trezor/blob/main/ROADMAP.md) · [END-TO-END Layer 4b](https://github.com/ihelpmaybe/pulse-trezor/blob/main/END-TO-END.md)

Hardware wallets are **Desk’s job** until TIP2.

## TIP0 — Source of truth
- [ ] Locate full Tip app source on disk / private remote
- [ ] Decide: keep this repo face-only **or** push app code here
- [ ] Document build / sideload release steps
- [ ] Versioned APK update channel

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

## Already true (don’t regress)
- [x] PulseChain-first (not multi-chain cloud)
- [x] EIP-681 scan / pay
- [x] PulseX swap (Tip fee 0%)
- [x] Self-custody seed on device
- [x] No HWW / WalletConnect in v1 on purpose
