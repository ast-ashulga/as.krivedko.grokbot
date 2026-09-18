# Skill refs via submodule

`SKILL.md` never inlines the orthography corpus. It instructs a **Read** of:

```
vendor/as.krivedko.kgam/skills/krivedko/references/orfoart.md
vendor/as.krivedko.kgam/skills/krivedko/references/slovar.md
vendor/as.krivedko.kgam/skills/krivedko/references/sceny.md
```

Those paths exist only after the git submodule is initialized and checked out at the pinned SHA:

```bash
git submodule update --init --recursive
cd vendor/as.krivedko.kgam
git checkout ca133efbf7f12fe8a6250b9920ad3b12a99d620b
cd ../..
```

If the submodule is unavailable, see `../vendor/README.md` for the pin and manual clone instructions. Do not copy dictionary bodies into this tree.
