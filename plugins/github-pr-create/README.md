# github-pr-create

A Claude Code skill plugin that automatically creates GitHub or GitLab Pull Requests with smart, auto-formatted semantic titles derived from the branch name and PR content.

## What It Does

When you ask Claude Code to create a PR, this skill:

1. Detects a semantic prefix from your branch name (`feat/`, `fix/`, `chore/`, `docs/`, etc.)
2. Generates a concise, lowercase, past-tense title summarizing the change
3. Creates the PR via `gh` CLI, `glab` CLI, or the REST API

### Title Format

```
[prefix]: <past tense lowercase summary>
```

**Examples:**

| Branch | Generated Title |
|---|---|
| `feat/create-user` | `[feature]: created user` |
| `fix/login-null-pointer` | `[fix]: fixed null pointer crash on login` |
| `chore/update-deps` | `[chore]: updated deps` |
| `docs/api-auth-guide` | `[docs]: added authentication guide` |
| `refactor/payment-service` | `[refactor]: cleaned up payment logic` |

## Installation

Add this plugin to your Claude Code configuration:

```bash
claude skill add github-pr-create
```

## Usage

Just ask Claude Code to create a PR:

- "Create a PR for this branch"
- "Open a pull request"
- "Submit a PR to main"
- "Create a merge request on GitLab"

The skill will gather any missing details (repo, branch, base branch, reviewers, labels) and propose a title before creating the PR.

## Supported Platforms

- **GitHub** — via `gh` CLI or GitHub REST API
- **GitLab** — via `glab` CLI or GitLab REST API

## Prefix Rules

| Branch prefix | PR title prefix |
|---|---|
| `feat/`, `feature/` | `[feature]:` |
| `fix/`, `bugfix/`, `hotfix/` | `[fix]:` |
| `chore/` | `[chore]:` |
| `docs/`, `doc/` | `[docs]:` |
| `refactor/`, `refact/` | `[refactor]:` |
| `test/`, `tests/` | `[test]:` |
| `style/` | `[style]:` |
| `perf/` | `[perf]:` |
| `ci/` | `[ci]:` |
| *(no match)* | `[feature]:` |

## Author

Md Eftakhairul Islam (eftakhairul@gmail.com)

## License

See [LICENSE.txt](../../LICENSE.txt) for details.
