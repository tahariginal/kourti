# Repository Guidelines

Agent name: **Sonic**.

## Project Structure & Module Organization

Kurty is a mobile app concept for Morocco’s grand taxi ecosystem, currently in brainstorming and product definition. `README.md` contains the product vocabulary, role requirements, proposed workflows, and open questions. No technology stack has been selected, and there are no source, test, or asset directories yet. Keep product documentation in the README until its size justifies separate documents.

## Development & Validation Commands

There are currently no build, installation, test, or local runtime commands. Use these repository checks when contributing:

- `git status --short`: inspect staged and unstaged changes.
- `git diff -- README.md sonic.md`: review unstaged documentation edits.
- `git diff --cached`: review staged content before committing.
- `git diff --check` and `git diff --cached --check`: check unstaged and staged whitespace errors.

Document setup and validation commands when implementation tooling is introduced.

## Writing Style & Naming Conventions

Use Markdown headings, short paragraphs, hyphenated bullet lists, and numbered lists for ordered workflows. Wrap filenames, commands, and state names in backticks. Match the README’s terminology: **kourti** manages operations, **nouba** describes turn order, and **Fayaje** is the provisional trip name. Explicitly label proposals and unresolved questions; do not present them as agreed requirements. No code formatter, linter, or language-specific indentation standard is configured.

## Testing Guidelines

No automated testing framework or coverage target exists. For documentation changes, preview Markdown, verify links, and check consistency across roles, trip states, and open questions. Preserve the distinction between allocated seats, passenger arrival, and departure. Add appropriate tests and their execution instructions when application code is introduced.

## Commit & Pull Request Guidelines

There is no commit history yet, so no established message convention exists. Use concise, imperative subjects such as `docs: clarify seat confirmation proposals`. Keep changes focused. Pull requests should explain the change, its rationale, and validation performed; link relevant issues when available. Include screenshots for future interface changes.

## Privacy & Product Decisions

Use fictional examples for driver IDs, phone numbers, taxi registrations, and locations. Treat location-sharing permissions and seat-confirmation behavior as unresolved until explicitly agreed and documented.
