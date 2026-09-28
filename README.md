# dynasty-core

Shared provider/domain primitives for **Ddreportcards** and **scoutcap**.

## Modules

- `dynasty_core.sleeper`: Sleeper league, roster, player-catalog, and trending primitives
- `dynasty_core.espn`: ESPN active-NFL stats, team map, and injury notes
- `dynasty_core.fantasycalc`: FantasyCalc dynasty values, indexes, and grades
- `dynasty_core.settings`: package-owned FantasyCalc query-profile defaults

Requires Python >= 3.12. The only runtime dependency is `httpx`.

## Consuming this package

Consumers **must** pin an exact 40-character commit SHA:

```
dynasty-core @ git+https://github.com/mcroney531-ctrl/dynasty-core.git@<40-char commit SHA>
```

Tags and version names (e.g. `v0.1.0`) are human labels only. The commit SHA
is the deployment identity; never pin a branch or a tag.

## Release process

1. Run the package test suite: `python -m unittest discover -s tests -v`.
2. Commit, and never rewrite a commit once a consumer has tested or pinned it.
3. Verify an exact-SHA install from GitHub in a clean Python 3.12 environment.
4. Update each consumer's `requirements.txt` to the new SHA.
