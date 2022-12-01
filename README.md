# Configurable git hooks

## Default setup

Config local git repo to use `.githooks` folder as hooks path, and lint diff with master on pre-push:

```bash
git config --local core.hooksPath ./.githooks
```

## Advanced configuration

Configure git hooks to your liking with [this guide](/docs/advanced_configuration.md)

## Skip hook execution

If you need to avoid executing a git hook, pass the `--no-verify` option to the git command like `git push --no-verify`

## Uninstall

Unset the custom hooks path with `git config --local --unset core.hooksPath`, to use default `.git/hooks` folder.

## Add to another project

To add this git manager to another project check [this guide](/docs/add_to_project.md)
