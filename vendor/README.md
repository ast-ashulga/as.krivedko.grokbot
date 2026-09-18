# vendor/asrokrivedko.kgam

## Pin

| Field | Value |
|-------|-------|
| Upstream | https://github.com/ast-ashulga/asrokrivedko.kgam |
| SHA | `2722a45780cb27f5af58f8989ed1993b016f412f` |
| Expected refs | `skills/krivedko/references/{orfoart,slovar,sceny}.md` |

## Preferred: git submodule

```bash
git submodule add https://github.com/ast-ashulga/asrokrivedko.kgam.git vendor/asrokrivedko.kgam
cd vendor/asrokrivedko.kgam
git checkout 2722a45780cb27f5af58f8989ed1993b016f412f
cd ../..
git add .gitmodules vendor/asrokrivedko.kgam
git commit -m "chore: pin asrokrivedko.kgam submodule"
```

Clone consumers:

```bash
git submodule update --init --recursive
```

## If submodule add / clone fails

Documented fallback (scaffold continues without blocking):

```bash
mkdir -p vendor
git clone https://github.com/ast-ashulga/asrokrivedko.kgam.git vendor/asrokrivedko.kgam
cd vendor/asrokrivedko.kgam
git checkout 2722a45780cb27f5af58f8989ed1993b016f412f
```

Or fetch the zipball / tarball for that SHA from the GitHub API and unpack into `vendor/asrokrivedko.kgam` so the three reference paths resolve.

Do **not** vendor-copy `slovar.md` / `orfoart.md` / `sceny.md` into `skill/` — the adapter must Read them from this pin.
SUBMODULE_ADD_FAILED

Scaffold note (2026-09-18T22:59:32+03:00): `git submodule add` failed on this host:

```
Cloning into '/workspace/tmp/asrokrivedko.grokbot-scaffold/vendor/asrokrivedko.kgam'...
fatal: could not read Username for 'https://github.com': No such device or address
fatal: clone of 'https://github.com/ast-ashulga/asrokrivedko.kgam.git' into submodule path '/workspace/tmp/asrokrivedko.grokbot-scaffold/vendor/asrokrivedko.kgam' failed
```

Pin remains `2722a45780cb27f5af58f8989ed1993b016f412f`. Init when git protocol / clone works again.
