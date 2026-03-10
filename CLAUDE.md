# CLAUDE.md

## Session Protocol

1. Read this file + any `.claude/features/<FEATURE_NAME>/progress.md` at session start.
2. One feature at a time.
3. Update `progress.md` and `index.md` before session ends.

## Statuses

All status fields: `Draft` → `In Progress` → `In Review` → `Done`

## Roles

Tell Claude: "Act as [Role] for feature [FEATURE_NAME]."

- **Analyst** → `.claude/profiles/analyst.md`
- **Architect** → `.claude/profiles/architect.md`
- **Developer** → `.claude/profiles/developer.md`
- **Reviewer** → `.claude/profiles/reviewer.md`

## Feature Workflow

Each feature lives in `.claude/features/<FEATURE_NAME>/`.
Templates are in `.claude/templates/`.

```
Analyst   → index.md, progress.md, requirements.md, context.md
Architect → spec.md, tasks.md, updates index.md + progress.md
Developer → implements, checks off tasks, updates index.md + progress.md
Reviewer  → comments.md, updates index.md + progress.md
Developer → addresses comments, updates progress.md
Reviewer  → resolves comments → updates index.md status to Done
```

## Git Workflow

- Create a feature branch per feature: `feature/<FEATURE_NAME>`
- Merge to `main` via pull request when Done

## Project Specifics

See `ARCHITECTURE.md` for technology decisions and constraints.
See `CONVENTIONS.md` for code style rules.
