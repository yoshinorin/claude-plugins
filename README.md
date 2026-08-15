# claude-plugins

A collection of custom agents and skills for [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

## Plugins

| Type | Name | Description |
|------|------|-------------|
| Skill | `commit-message` | Analyzes `git diff` and generates a commit message in English following the [Conventional Commits](https://www.conventionalcommits.org/) format. |
| Agent | `secret-scanner` | Scans code and configuration files for sensitive information such as API keys, passwords, and personal data that must not be exposed in a public repository. |
| Agent | `npm-publish-checker` | Checks an npm package for readiness before publishing, verifying `package.json` metadata, the actual set of files `npm publish` will include, and common publish mistakes. Delegates secret scanning to `secret-scanner`. |
| Agent | `crate-publish-checker` | Checks a Rust crate for readiness before publishing, verifying `Cargo.toml` metadata, the actual set of files `cargo publish` will include, and common publish mistakes. Delegates secret scanning to `secret-scanner`. |

## Installation

Add this marketplace to Claude Code:

```
# Add marketplace
/plugin marketplace add https://github.com/yoshinorin/claude-plugins

or

/plugin marketplace add yoshinorin/claude-plugins
```

```
# Install plugins
/plugin install commit-plugin@yoshinorin-plugins
/plugin install secret-scanner@yoshinorin-plugins
/plugin install publish-checker@yoshinorin-plugins
```
