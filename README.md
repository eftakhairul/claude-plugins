# claude-skills

A collection of custom Claude Code plugins for automating common development workflows.

## Installation

Add this plugin marketplace to your Claude Code:

```bash
/plugin marketplace add eftakhairul/claude-plugins
```

## Available Plugins

### github-pr-create

Automatically creates GitHub or GitLab Pull Requests with smart, auto-formatted semantic titles derived from the branch name and PR content. It supports both GitHub (`gh` CLI) and GitLab (`glab` CLI).

| Branch | Generated Title |
|---|---|
| `feat/create-user` | `[feature]: created user` |
| `fix/login-null-pointer` | `[fix]: fixed null pointer crash on login` |
| `chore/update-deps` | `[chore]: updated deps` |
| `docs/api-auth-guide` | `[docs]: added authentication guide` |


**NB**: `gh` CLI or `glab` CLI should be installed.

## Author

Md Eftakhairul Islam (eftakhairul@gmail.com)

## License

Apache License 2.0 — see [LICENSE.txt](LICENSE.txt) for details.
