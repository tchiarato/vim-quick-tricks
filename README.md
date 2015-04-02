# vim-quick-tricks
A bunch of vim quick tricks

#### Find Duplicated lines

```vim
:sort " To sort all lines in a file
:g/^\(.*\)$\n\1$/p
```
