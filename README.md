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

See the [project wiki](https://github.com/StephanieF/DrupalAI/wiki) for the
full guide, and `.ai/kenkeep/README.md` for kenkeep's own reference.
