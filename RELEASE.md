# Release — Share as Template

## Live

Public template: https://x.ai/bot/k4TVp_w5mKyJ7CCQQ_8Ty  
Published: 2026-09-19 (QA post-share GREEN)

## Checklist (all green)

- [x] `git submodule update --init --recursive` succeeds (or `vendor/README.md` pin is documented and refs resolve)
- [x] Upstream pin is `ca133efbf7f12fe8a6250b9920ad3b12a99d620b`
- [x] `skill/SKILL.md` instructs Read of vendor refs only — no pasted `slovar` / `orfoart` / `sceny` bodies
- [x] `profile.md` matches Marketplace `template.description` intent
- [x] `listing.md` blurb is short and accurate
- [x] Fixtures reviewed:

| Fixture | Gate |
|---------|------|
| `fixtures/room-spice-ok.md` | Rare spice allowed when slot open + on-beat |
| `fixtures/room-spice-storm.md` | Storm / spam → stay quiet |
| `fixtures/room-mention-burns-slot.md` | `@` burns the spice slot |
| `fixtures/room-skip-no-beat.md` | No beat → silence |
| `fixtures/mixed-code-preserve.md` | Code / ids / URLs untouched |
| `fixtures/critical-path-clean.md` | DROP / rm -rf / force-push / security → clean prose |

## QA gates (green)

1. **Code preserve** — PASS
2. **Critical-path clean** — PASS
3. **Rare spice** — PASS
4. **Anti-jobs** — PASS
5. **Post-share public listing** — PASS (https://x.ai/bot/k4TVp_w5mKyJ7CCQQ_8Ty)

Keep this repo as the versioned adapter source of truth.
