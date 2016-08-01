Zsh can create temporary files when using command substitution
insteaad of pipes. This makes a difference when programs need
to go over input multiple times, like `vimdiff` does.

    vimdiff =(ls /bin) =(ls /usr/bin) # temp files, zsh only
    vimdiff <(ls /bin) <(ls/usr/bin)  # pipes, works in bash,zsh

Source: https://news.ycombinator.com/item?id=5690387
