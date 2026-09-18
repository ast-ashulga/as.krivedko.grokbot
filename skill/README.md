# Skill refs via submodule

`SKILL.md` never inlines the orthography corpus. It instructs a **Read** of:

```
vendor/asrokrivedko.kgam/skills/krivedko/references/orfoart.md
vendor/asrokrivedko.kgam/skills/krivedko/references/slovar.md
vendor/asrokrivedko.kgam/skills/krivedko/references/sceny.md
```

Those paths exist only after the git submodule is initialized and checked out at the pinned SHA:

```bash
git submodule update --init --recursive
cd vendor/asrokrivedko.kgam
git checkout 2722a45780cb27f5af58f8989ed1993b016f412f
```

If the submodule is unavailable, see `../vendor/README.md` for the pin and manual clone instructions. Do not copy dictionary bodies into this tree.
