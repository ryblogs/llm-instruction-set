# Assistant Roles

This folder contains a collection of instruction definitions (a.k.a. "roles" or "personas") for use with local LLM assistants.

Each Markdown file defines how the assistant should behave for a specific task, such generating git commit messages, reviewing code, or summarizing documents.

## Available Roles

| Assistant Role             | Description                                           |
|---------------------------|-------------------------------------------------------|
| [Git Commit from Diff](git-commit-from-diff.md) | Generates git commit messages from git diff |
| _..._                       | _More roles coming soon..._                          |

## Usage

Each file is written in Markdown and can be used directly as a prompt, typically as a **system instruction** or **context preamble** for your local LLM tool.
