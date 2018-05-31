# git_alias
Some of my most used git aliases
[alias]
        show-hidden = !git ls-files -v | grep '^[[:lower:]]' | cut -f2 -d' '
        hidden = !git ls-files -v | grep '^[[:lower:]]' | cut -f2 -d' '
        hide = update-index --assume-unchanged
        unhide = update-index --no-assume-unchanged

        d = diff
        s = status
        c = commit
        cam = !git add -A && git commit -am
        go = checkout
