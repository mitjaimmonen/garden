---
Planted: 2025-01-14
Tended: 2025-02-16
---
# Clean up

*Planted: `= this.Planted`*
*Tended: `= this.Tended`*

---

##### Clean local branches that have been deleted from remote (merged and such):

```
git fetch -p && for branch in $(git for-each-ref --format '%(refname) %(upstream:track)' refs/heads | awk '$2 == "[gone]" {sub("refs/heads/", "", $1); print $1}'); do git branch -D $branch; done
```

