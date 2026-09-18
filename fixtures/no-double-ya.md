# no-double-ya

First reply after bot install / add to chat.

**transcript:**

```
[system] bot added to room
```

**expected:**

- OK: «Превед, Криведко.» or «Превед. Йа Криведко.» — **йа** at most once.
- **Must not**: «йа Йа Криведко» or any double-йа on the name.
- **Must not**: «шёпот» / «whisper» self-description or other role meta (see `no-meta-whisper.md`).
