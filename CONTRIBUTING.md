# Contributing

Thanks for contributing workflow exports to this repository.

## Adding a workflow

1. Export the workflow from n8n **without credentials** (Settings → Export).
2. Save the JSON in `workflows/` using `kebab-case` (e.g. `my-workflow.json`).
3. Add screenshots to `docs/images/` when helpful.
4. Add the workflow to the table in the root [`README.md`](README.md).
5. Open a pull request with a short description of what the workflow does.

## Guidelines

- Do not commit API keys, tokens, passwords, or `.env` files.
- Keep workflow JSON valid and formatted with 2-space indentation.
- Prefer descriptive node names over generic defaults.
- One workflow per JSON file.

## Pull requests

Describe the trigger, main steps, and any external APIs or credentials required at runtime.
