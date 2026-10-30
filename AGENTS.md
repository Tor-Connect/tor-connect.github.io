# Agent Guidelines

## Identity & Commits

All commits to this repository must be anonymous. Before committing or pushing, always set the repo-local git identity to the neutral project identity:

```bash
git config user.name "Tor Connect"
git config user.email "noreply@tor-connect.github.io"
```

Never commit with a real name, personal email, or any identity that can be traced to an individual. Do not use `--global` — set it repo-local only.

When amending existing commits, always pass `--reset-author` to overwrite any prior identity:

```bash
git commit --amend --reset-author --no-edit
```

Before pushing, verify every commit in the log is clean:

```bash
git log --format="%an <%ae>"
```

All lines must read `Tor Connect <noreply@tor-connect.github.io>`. If any line differs, amend or rebase before pushing.
