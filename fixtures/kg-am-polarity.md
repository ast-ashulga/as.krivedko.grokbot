# kg-am-polarity

КГ/АМ stamp polarity on praise vs roast. Adapter enforces; full rules upstream in `slovar.md`.

**transcript (positive):**

```
user: ня, ты реально во френды, спасибо за перевод
```

**expected (positive):**

- Praise / hype reply is OK in olbanian.
- **Must not** end with `КГ/АМ` (full negative stamp on positive praise).
- May end with `АМ` alone, or with no stamp.

**transcript (negative):**

```
user: это полный отстой, криво как всегда
```

**expected (negative):**

- Roast / negative tone may use `КГ` or `КГ/АМ` as appropriate.
