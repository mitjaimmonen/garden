# Clean up
##### Clean local branches that have been deleted from remote (merged and such):

```
git fetch -p && for branch in $(git for-each-ref --format '%(refname) %(upstream:track)' refs/heads | awk '$2 == "[gone]" {sub("refs/heads/", "", $1); print $1}'); do git branch -D $branch; done
```

### Set git hooks path to include hooks in source control

Place new hooks in folder ".git-hooks" and run the following:
`git config core.hooksPath .git-hooks

