# Replace text in multiple files

To search and replace text in Unix we can use the command

```shell
grep -rIl 'search' * | xargs sed -i '' 's/search/remplace/g'
```

The command grep uses these search arguments: 
- `r` recursive
- `I` ignoring binaries
- `l` listing all the attached files.

Then with the command `xargs` we do the command `sed` to search and replace in each file found, the option `i` means replacing the files. The command `sed` can create other files with the changes but isn't the result that we want in this case.
