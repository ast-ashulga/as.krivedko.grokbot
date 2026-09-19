# as.krivedko.grokbot

Thin **Grok Bot** adapter for «Йа Криведко» (padonki / olbanian / КГ/АМ).

## Install

Add the bot on x.ai: **https://x.ai/bot/k4TVp_w5mKyJ7CCQQ_8Ty**

Then invite **Йа Криведко** into a group chat. The bot stays quiet most of the time; mention `@Йа Криведко` or say «олбанский» for an immediate reply.

The orthography core stays in upstream [`as.krivedko.kgam`](https://github.com/ast-ashulga/as.krivedko.kgam) at a **pinned SHA** (git submodule). This repo versions the adapter, fixtures, and Marketplace listing, not the dictionary bodies.

**License:** MIT (this adapter). Upstream `as.krivedko.kgam` is also MIT; see `LICENSE` dual-MIT note.

## Upstream pin

| | |
|---|---|
| Repo | https://github.com/ast-ashulga/as.krivedko.kgam |
| SHA | `ca133efbf7f12fe8a6250b9920ad3b12a99d620b` |
| Path | `vendor/as.krivedko.kgam` (git submodule) |

## Layout

```
.
├── LICENSE
├── README.md
├── profile.md          # persona / template.description
├── listing.md          # Marketplace blurb
├── RELEASE.md          # Share-as-Template checklist + QA gates
├── skill/
│   ├── SKILL.md        # Grok-adapted skill (reads vendor refs)
│   └── README.md       # how refs resolve via submodule
├── fixtures/           # short transcripts + expected:
└── vendor/
    ├── README.md       # pin + submodule init
    └── as.krivedko.kgam/   # submodule (pinned)
```

## Submodule init

```bash
git clone https://github.com/ast-ashulga/as.krivedko.grokbot.git
cd as.krivedko.grokbot
git submodule update --init --recursive
cd vendor/as.krivedko.kgam && git checkout ca133efbf7f12fe8a6250b9920ad3b12a99d620b
cd ../..
ls vendor/as.krivedko.kgam/skills/krivedko/references/{orfoart,slovar,sceny}.md
```

Details: `vendor/README.md`.

## What ships where

- **v1 Marketplace bot** is built in the Grok Bot UI from the bundled skill (`skill/SKILL.md` + `profile.md`).
- **This repo** versions adapter / fixtures / listing; persona and rare-spice rules are reviewable without publishing a bot from git alone.
- **Do not** paste `orfoart` / `slovar` / `sceny` bodies here; the skill `Read`s them from the vendor pin.

## Group presence (rare spice)

In group / room chats: silent most turns; peanut-gallery spice only on a clear beat.

- At most **1** unsolicited spice reply per **≥ 8** room turns; never two in a row.
- An `@` mention or «криведко|олбанский» cue **burns** the spice slot (immediate short reply).
- Quiet when there is nothing funny / on-beat to say.
