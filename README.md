My dotfiles.


# Install

```bash
git clone https://github.com/mauron85/dotfiles ~/.dotfiles
```

Add following to .bash_profile:

```bash
DOT_FILES_DIR=$HOME/.dotfiles
PIPETO_ME_KEY=

for dotfile in "$DOT_FILES_DIR"/.{functions,function,function_*,path,env,alias,grep,prompt,nvm,completion,custom};
do
  [ -f "$dotfile" ] && \. "$dotfile"
done
# Clean up
unset dotfile
```
