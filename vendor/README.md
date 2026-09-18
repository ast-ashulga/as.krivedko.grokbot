# vendor/asrokrivedko.kgam

Git submodule. Orthography core for the Grok adapter — **pinned SHA**, not floating `main`.

## Pin

| Field | Value |
|-------|-------|
| Upstream | https://github.com/ast-ashulga/asrokrivedko.kgam |
| SHA | `2722a45780cb27f5af58f8989ed1993b016f412f` |
| Expected refs | `skills/krivedko/references/{orfoart,slovar,sceny}.md` |

## Init + pin checkout

```bash
git submodule update --init --recursive
cd vendor/asrokrivedko.kgam
git checkout 2722a45780cb27f5af58f8989ed1993b016f412f
cd ../..
```

Confirm refs:

```bash
ls vendor/asrokrivedko.kgam/skills/krivedko/references/{orfoart,slovar,sceny}.md
```

## First-time add (maintainers)

```bash
git submodule add https://github.com/ast-ashulga/asrokrivedko.kgam.git vendor/asrokrivedko.kgam
cd vendor/asrokrivedko.kgam
git checkout 2722a45780cb27f5af58f8989ed1993b016f412f
cd ../..
git add .gitmodules vendor/asrokrivedko.kgam
```

## Manual fallback

If submodule clone fails on a host, clone the upstream into `vendor/asrokrivedko.kgam` and check out the same SHA so the three reference paths resolve. Do **not** vendor-copy `slovar.md` / `orfoart.md` / `sceny.md` into `skill/`.
