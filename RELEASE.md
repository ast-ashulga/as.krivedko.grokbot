# Release — Share as Template

Do **not** publish / Share as Template until every gate below is green.

## Checklist

- [ ] `git submodule update --init --recursive` succeeds (or `vendor/README.md` pin is documented and refs resolve)
- [ ] Upstream pin is `2722a45780cb27f5af58f8989ed1993b016f412f`
- [ ] `skill/SKILL.md` instructs Read of vendor refs only — no pasted `slovar` / `orfoart` / `sceny` bodies
- [ ] `profile.md` matches Marketplace `template.description` intent
- [ ] `listing.md` blurb is short and accurate
- [ ] Fixtures reviewed:

| Fixture | Gate |
|---------|------|
| `fixtures/room-spice-ok.md` | Rare spice allowed when slot open + on-beat |
| `fixtures/room-spice-storm.md` | Storm / spam → stay quiet |
| `fixtures/room-mention-burns-slot.md` | `@` burns the spice slot |
| `fixtures/room-skip-no-beat.md` | No beat → silence |
| `fixtures/mixed-code-preserve.md` | Code / ids / URLs untouched |
| `fixtures/critical-path-clean.md` | DROP / rm -rf / force-push / security → clean prose |

## QA gates (must be green)

1. **Code preserve** — mixed prose+code fixtures pass.
2. **Critical-path clean** — irreversible / security turns are plain text.
3. **Rare spice** — ≤1 per ≥8; mention burns slot; skip when no beat.
4. **Anti-jobs** — coding / shipping / auth / repo asks are refused.
5. **No CreateAgent / no live bot publish from this checklist alone** — build v1 in Grok Bot UI from bundled skill when ready.

## After green

Share as Template from Grok Bot UI (Team or Public as chosen). Keep this repo as the versioned adapter source of truth.
