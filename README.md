# vim-quick-tricks
A bunch of vim quick tricks

## Regex
### Find Duplicated lines

```vim
:sort " To sort all lines in a file
:g/^\(.*\)$\n\1$/p
```

### Deleting lines that do not contain a given pattern
Let's say that you have the following log file and you want to delete all lines except the one that has the request path info.
```
2015-04-02T23:43:25.191908+00:00 app[web.1]: Started GET "/cars/16/models.json?format=json" for 189.71.47.35 at 2015-04-02 20:43:25 -0300
2015-04-02T23:43:25.188916+00:00 app[web.1]: source=rack-timeout id=e6a8641f-7dea-46c8-8b8f-f426122684c2 age=4ms timeout=20000ms duration=21ms state=completed at=info
2015-04-02T23:43:25.167262+00:00 app[web.1]: source=rack-timeout id=e6a8641f-7dea-46c8-8b8f-f426122684c2 age=4ms timeout=20000ms state=ready at=info
...
```

```vim
:g!/GET/d "
```
