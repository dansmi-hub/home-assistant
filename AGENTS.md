# Instructions for AI agents

This repo stores Home Assistant YAML for version history. It is not a deployment target, a public site, or a shared resource.

## Rules

- Do not create anything in this repo that is meant to be used or seen from outside it. That includes dashboards, web pages, published artifacts, shared links, or anything another system is expected to read directly from here.
- Only store Home Assistant config: blueprints, automations, and notes about them.
- Keep the layout from [README.md](README.md):
  - `blueprints/automation/<author>/` for blueprints
  - `automations/<area>/` for automation configs
- Use lowercase, underscore-separated file names named after the device or job.
- Never commit tokens, passwords, `secrets.yaml`, or `.env` files. Check the `.gitignore` before adding new files.
- Before committing YAML, check that it parses.
- Commit messages should say what changed and why, and end with the Co-Authored-By line used in this repo's history.

## Context

- The live Home Assistant config may differ from this repo. Changes here do not automatically apply to the Home Assistant box.
- The repo may become a Git pull source for Home Assistant later, so keep the folder layout matching Home Assistant's expected paths.
