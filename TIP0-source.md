# TIP0 — Source of truth (face vs code)

**Status:** decided (interim) · **Date:** 2026-11-22  
**Repo face:** https://github.com/ihelpmaybe/Tip-wallet (public)

## What we found

| Artifact | Where | Verdict |
|----------|-------|---------|
| Public GitHub `Tip-wallet` | this repo | **Face only** — `read.me`, TODO/AGENTS/NOTES. No Android app tree, no Gradle, no APK |
| Program folder `pulse-trezor-org/` | Desktop | No Tip app clone until this face repo; no `android/` / `apps/mobile` |
| Org other repos | ihelpmaybe | No second Tip code host listed; EIP-681 helpers are `Internetmoney681-Android` / Chrome (pay-link only, not Tip) |

**Claim grade:** verified for GH face · **full Tip app source path on this PC: not located this session**

## Decision (preferred)

1. **Keep `Tip-wallet` public as the product face** (sideload notes, safety copy, program TODOs).  
2. **Do not rebuild Tip** (Rabby Mobile lineage) — BUILD-EFFICIENCY forbids a second soft Android wallet.  
3. **When full source path is known**, either:  
   - **A (preferred):** private sibling e.g. `Tip-wallet-app` with code; this repo stays face + release notes / checksums, **or**  
   - **B:** push app under this repo in `android/` (or root) if license/lineage allows public.  
4. Until then: **TIP1+ code work is blocked** on locating the tree; Desk continues (#9 A2).

## Sideload / build (stub)

- Product promise (from `read.me`): update-over-install; PulseChain 369; optional 943; PulseX 0% fee; no HWW/WC in Tip v1.  
- **Build steps:** unknown until source path + toolchain notes exist.  
- **APK channel:** publish checksums here when builds resume; Graphene sideload = pen requirement (platform TODO).

## Next

- Operator: name absolute path (or private remote) of Tip Android tree → reopen TIP0 to pick A vs B and unstick TIP1.  
- Agents: do **not** invent Tip from Rabby; consume SYNC4 pack only after code is reachable.

## Kill if

Source never appears and someone proposes greenfield Android wallet → **KILL**; soft mobile stays Tip or nothing.
