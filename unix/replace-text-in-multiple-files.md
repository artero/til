# Replace text in multiple files

to search and replace text in Unix we can use the next command

```shell
grep -rIl 'search' * | xargs sed -i '' 's/search/remplace/g'
```

The command grep with this arguments search: 
- `r` recursive
- `Ì` ignoring binaries
- `l` listing all the attached files.

With `xargs` we do the command `sed` for each line in the `grep` results with the 
option `i` replacing in the files.
