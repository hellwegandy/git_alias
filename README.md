# git_alias
Some of my most used git aliases

```gitconfig
[alias]
    d = diff --word-diff
    s = status
    c = commit
    cam = !git add -A && git commit -am
    ca = !git add -A && git commit -a
    go = checkout
    lastc = log -1 HEAD
    lastd = diff HEAD^..HEAD --word-diff
    lasts = diff HEAD^..HEAD --name-only
    uncommit = reset HEAD^1
    uc = reset HEAD^1
    patch = commit -a --amend --no-edit

    # prints the file path relative to repository root
    show-hidden = !git ls-files -v | grep '^[[:lower:]]' | cut -f2 -d' '
    hidden = !git show-hidden

    # hides a file from commits or adds
    hide = update-index --assume-unchanged

    # stops a file from being hidden by commits or adds
    unhide = update-index --no-assume-unchanged
    
    # get the current branch name, used mostly in other aliases
    current = rev-parse --abbrev-ref HEAD

    # update with remote master and update local master with remote changes
    uwm = !CURRENT=$(git current) && git checkout master && ( git pull || git checkout $CURRENT && echo "Failed updating with master." && exit 1) && git checkout $CURRENT && git merge master
```
