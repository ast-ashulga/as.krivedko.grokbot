# asrokrivedko.grokbot

Thin **Grok Bot** adapter for «Йа Криведко» (padonki / olbanian / КГ/АМ).

The orthography core stays in upstream [`asrokrivedko.kgam`](https://github.com/ast-ashulga/asrokrivedko.kgam) at a **pinned SHA** (git submodule). This repo versions the adapter, fixtures, and Marketplace listing — not the dictionary bodies.

**License:** MIT (this adapter). Upstream `asrokrivedko.kgam` is also MIT — see `LICENSE` dual-MIT note.

## Upstream pin

| | |
|---|---|
| Repo | https://github.com/ast-ashulga/asrokrivedko.kgam |
| SHA | `2722a45780cb27f5af58f8989ed1993b016f412f` |
| Path | `vendor/asrokrivedko.kgam` (git submodule) |

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
    └── asrokrivedko.kgam/   # submodule (pinned)
```

## Submodule init

```bash
git clone https://github.com/ast-ashulga/asrokrivedko.grokbot.git
cd asrokrivedko.grokbot
git submodule update --init --recursive
cd vendor/asrokrivedko.kgam && git checkout 2722a45780cb27f5af58f8989ed1993b016f412f
cd ../..
ls vendor/asrokrivedko.kgam/skills/krivedko/references/{orfoart,slovar,sceny}.md
```

Details: `vendor/README.md`.

## What ships where

- **v1 Marketplace bot** is built in the Grok Bot UI from the bundled skill (`skill/SKILL.md` + `profile.md`).
- **This repo** versions adapter / fixtures / listing — persona and rare-spice rules are reviewable without publishing a bot from git alone.
- **Do not** paste `orfoart` / `slovar` / `sceny` bodies here; the skill `Read`s them from the vendor pin.

## Group presence (rare spice)

In group / room chats: silent most turns; peanut-gallery spice only on a clear beat.

- At most **1** unsolicited spice reply per **≥ 8** room turns; never two in a row.
- An `@` mention or «криведко|олбанский» cue **burns** the spice slot (immediate short reply).
- Quiet when there is nothing funny / on-beat to say.
