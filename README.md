# Git & GitHub Collaboration Workflow

A software engineering course exercise in team version control. The code is intentionally tiny (`hello.py`) so the focus stays on the workflow: branching, pull requests, code review and resolving a real merge conflict with a partner.

**Stack:** Python · Git · GitHub · VS Code · Linux terminal

## Run it

```bash
python3 hello.py
```

```text
Hello, World!
Hello from both MAIN and FEATURE-2
```

The second line is the result of the merge conflict described below: both branches changed the same line, and the resolution kept a line that credits both.

## Workflow

```text
main ──●──────────●─────────●──  (merge)
        \        /         /
feature-1 ●─────●         /
          \              /
     feature-2 ●────────●       (conflict resolved here)
```

1. **Repository setup:** initialized a local repo, connected it to GitHub, and committed from the terminal.
2. **Feature branches:** `feature-1` and `feature-2` isolated each change from `main`.
3. **Pull requests:** every change reached `main` through a PR reviewed by my partner.
4. **Merge conflict:** both feature branches edited the same line of `hello.py`. I resolved it by hand, removed the `<<<<<<<` / `=======` / `>>>>>>>` markers, re-ran the script, and merged after approval.

## Issues tracked

| # | Issue | Resolution |
|---|-------|------------|
| 1 | Create the base script | Added `hello.py` on `main` with the initial commit |
| 2 | Syntax error during development | Found and fixed it, tested locally before committing |
| 3 | Add a feature on a second branch (conflicting edit) | Resolved the conflict manually; reviewed and merged via PR |

## What I practiced

- Git from the command line: `init`, `add`, `commit`, `branch`, `checkout`, `merge`, `push`, `pull`
- Isolating work on feature branches and keeping `main` releasable
- Opening, reviewing and merging pull requests
- Reading and resolving merge conflicts without losing either side's intent

## Author

Noel Mekogue, with a course partner for review and the conflict exercise.
