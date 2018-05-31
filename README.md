# git_alias
Some of my most used git aliases

```gitconfig
[alias]
    # show-hidden and hidden are the same, currently prints the file path relative to repository root
    show-hidden = !git ls-files -v | grep '^[[:lower:]]' | cut -f2 -d' '
    hidden = !git ls-files -v | grep '^[[:lower:]]' | cut -f2 -d' '

    # hides a file from commits or adds
    hide = update-index --assume-unchanged

    # stops a file from being hidden by commits or adds
    unhide = update-index --no-assume-unchanged

    d = diff
    s = status
    c = commit
    cam = !git add -A && git commit -am
    ca = !git add -A && git commit -a
    go = checkout
```
