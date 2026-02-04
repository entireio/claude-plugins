---
description: Explains the intent behind source code by finding original session transcripts. Use /explain with a function, file, or line of code to understand why it exists.
---

# Explain Intent

Explain the intent behind source code by tracing it back to the original conversation where it was created. Works with:

- **Functions** — Why does this function exist? What problem was it solving?
- **Files** — What's the purpose of this file? What requirements drove its creation?
- **Line changes** — Why was this specific line added or modified?

## Process

1. Use `git blame` or `git log` to identify the commit that introduced the code.
2. Use `entire explain --commit COMMIT_SHA` to read the session transcripts.
