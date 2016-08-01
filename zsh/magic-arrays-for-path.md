Try the following in a zsh.

    print -l $path

What happened:

zsh creates lowercase variables for traditionally `:` separated
stuff and exposes them as arrays. Much nicer to work with IMO.

Source: https://news.ycombinator.com/item?id=5690633
