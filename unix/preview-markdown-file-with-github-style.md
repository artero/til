# Preview markdown file with GitHub style

You can use the command `grip` to open a file in HTML with the same styles that
GitHub

```sh
$ grip -b my_file.md
```

This command runs a little server where you can see the file in the route
http://localhost:6419, the `-b` option a tab in the browser after the server start.
By default, the page will refresh when you change the file.

In VIM you can open the current file with

```
:!grip -b %
```

In NeoVim you can use a temporal terminal to the server and that auto-reload the
changes and doesn't stop the editor with:

```
:te grip -b %
```

