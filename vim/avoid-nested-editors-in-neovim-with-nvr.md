# Avoid nested editors in NeoVim with nvr

With this script in your `~/.zshrc` file, you can avoid nested editor when you execute
NeoVim command inside the NeoVim terminal

```sh
# User nvr inside nvim to prevent nested nesting
# 
if [ -n "$NVIM_LISTEN_ADDRESS" ]; then
  if [ -x "$(command -v nvr)" ]; then
    alias nvim=nvr
    alias vim=nvr
    alias vi=nvr
    export VISUAL="nvr -cc split --remote-wait"
  else
    alias nvim='echo "No nesting!"'
  fi
fi
```

You require pip3 to install nvr, more information in: https://github.com/mhinz/neovim-remote 
