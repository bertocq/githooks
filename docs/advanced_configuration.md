# Custom git hooks configuration

If you want to execute a script for any given git hook, symlink that file to the folder with the hook name inside of `.githooks` directory.

For example to execute `bin/lint/rubocop` file as part of the hooks triggered by `git push` you would:

```bash
ln -s ./bin/lint/rubocop .githooks/pre-push.hooks/rubocop
```

That way, when you `git push`, git will call the `.githooks/pre-push` file (which is a symlink to `.githooks/group-scripts-into-git-hook`) that in turn will execute all scripts inside of `.githooks/pre-push.hooks` folder.
