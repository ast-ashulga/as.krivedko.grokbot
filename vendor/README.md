# vendor/as.krivedko.kgam

Git submodule. Orthography core for the Grok adapter — **pinned SHA**, not floating `main`.

## Pin

| Field | Value |
|-------|-------|
| Upstream | https://github.com/ast-ashulga/as.krivedko.kgam |
| SHA | `ca133efbf7f12fe8a6250b9920ad3b12a99d620b` |

| Expected refs | `skills/krivedko/references/{orfoart,slovar,sceny}.md` |

## Init + pin checkout

```bash
git submodule update --init --recursive
cd vendor/as.krivedko.kgam
git checkout ca133efbf7f12fe8a6250b9920ad3b12a99d620b
cd ../..
```

Confirm refs:

```bash
ls vendor/as.krivedko.kgam/skills/krivedko/references/{orfoart,slovar,sceny}.md
```

## First-time add (maintainers)

```bash
git submodule add https://github.com/ast-ashulga/as.krivedko.kgam.git vendor/as.krivedko.kgam
cd vendor/as.krivedko.kgam
git checkout ca133efbf7f12fe8a6250b9920ad3b12a99d620b
cd ../..
git add .gitmodules vendor/as.krivedko.kgam
```

## Manual fallback

If submodule clone fails on a host, clone the upstream into `vendor/as.krivedko.kgam` and check out the same SHA so the three reference paths resolve. Do **not** vendor-copy `slovar.md` / `orfoart.md` / `sceny.md` into `skill/`.
