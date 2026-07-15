# Git hooks (identity enforcement)

This repo requires commits as:

```text
Daniel Febrero <febrero.daniel@gmail.com>
```

After clone:

```bash
git config --local user.name "Daniel Febrero"
git config --local user.email "febrero.daniel@gmail.com"
git config --local core.hooksPath .githooks
```

The `pre-commit` hook rejects commits if the effective `user.name` / `user.email` (or `GIT_AUTHOR_EMAIL` / `GIT_COMMITTER_EMAIL`) do not match.
