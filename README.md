# DrupalAI

Drupal 11 site (DDEV, Composer-managed). The web root is `web/`.

## AI knowledge base (kenkeep)

This repo uses [kenkeep](https://kenkeep.canpicasoft.com/) to keep a shared,
git-reviewed knowledge base for AI coding assistants (currently Claude Code).
Notes live in `.ai/kenkeep/nodes/`, and every new AI session loads
`.ai/kenkeep/ENTRY.md`.

Quick reference (needs Node.js 22+ on the host):

```bash
npx kenkeep doctor   # verify the setup after cloning
npx kenkeep status   # see pending session captures
```

Inside a Claude Code session:

- `/kk-curate`: turn captured sessions into notes
- `/kk-session-extract`: capture knowledge from the current session now
- `/kk-add`: record one fact by hand
- `/kk-bootstrap`: seed notes from existing docs (respects `.kkignore`)

New or changed notes show up in `git status`. Review them with `git diff`,
commit to accept, and `git restore` to reject.

See the [kenkeep wiki page](https://github.com/StephanieF/DrupalAI/wiki/Kenkeep:-AI-knowledge-base) for the
full guide, and `.ai/kenkeep/README.md` for kenkeep's own reference.

## Plan-first AI tasks (Strikethroo)

Larger AI-assisted changes go through
[Strikethroo](https://strikethroo.canpicasoft.com): plan → tasks → execute,
with a review point between each step. Plans live in `.ai/strikethroo/plans/`.

Inside a Claude Code session:

- `/st-create-plan <describe the work>`: write a plan (note its ID)
- `/st-refine-plan <id> <notes>`: adjust the plan
- `/st-generate-tasks <id>`: break it into tasks and an execution blueprint
- `/st-execute-blueprint <id>`: implement it, one commit per phase (start
  from a clean working tree)

Check the workspace with `npx strikethroo validate`, and browse plans with
`npx strikethroo serve`. See the
[Strikethroo wiki page](https://github.com/StephanieF/DrupalAI/wiki/Strikethroo)
for the full guide.
