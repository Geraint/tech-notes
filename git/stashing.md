# Stashing

- [detailed documentation](https://www.git-scm.com/docs/git-stash)

## Saving current state

```
git stash
```

This is equivalent to `git stash save`, but `save` is implied if there are no arguments.

To include untracked files:

```
git stash save -u
```

## See what's been saved

```
git stash list
```

## Pull back a saved state

```
git stash pop
```
