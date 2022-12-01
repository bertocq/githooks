# Add this git hook manager to a project

We use git subtree for that purpose.

Go into the project's folder and add this repo as a subtree on the `.githooks` folder:

```bash
git subtree add --prefix=.githooks git@github.com:bertocq/githooks.git master --squash
```

Then push the branch, you'll a pair of commits with the entire history of this repo.

## Keep references up to date

```bash
git subtree pull --prefix=.githooks git@github.com:bertocq/githooks.git master --squash
```
