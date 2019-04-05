# Git commands I tend to forget

## For all branches matching pattern print who did the last commit and when, oldest branch first

```bash
git branch --list '*pattern*' -r | xargs -n 1 git log -n 1 --pretty="%ct %ar - %cn %D" | sort
```
