# Private state contract

Store a course manifest outside the public procedure. It should include: course key, provider/page identity (never a signed media URL), authorized local output root, last inspection time, lesson records grouped by module, and evidence for each status. Use relative media paths when possible. Do not put credentials, cookies, private chat, purchased content or source media in Git.

Suggested statuses:

| Status | Meaning |
|---|---|
| `pending` | Listed or discovered, not yet validated. |
| `capturing` | Live operation only; reconcile after any interruption. |
| `validated` | Final media passed all checks; cite output and raw evidence. |
| `duplicate` | Same content proven against another validated lesson by direct evidence. |
| `blocked` | No usable player/audio or a repeatable platform error; preserve observed reason and revisit. |
| `partial` | Source take is incomplete; preserve it and do not count it as a completed lesson. |

Use a stable lesson slug/ID plus module identity as the key. List positions can shift when a provider inserts a lesson. Never renumber or overwrite existing files to make the list look contiguous. Update `checked_at` and evidence after each real inspection; a weekly no-change result should not fabricate a validation timestamp.

See the synthetic example in the repository's `examples/` directory. It illustrates schema shape, not live data. A private manifest can cite a raw recording and final media by relative path while keeping the recording itself out of Git.
