My dotfiles.


# Install

```bash
git clone https://github.com/mauron85/dotfiles ~/.dotfiles
```

Add following to .bash_profile:

```bash
for dotfile in "$HOME/.dotfiles"/.{functions,function,function_*,path,env,alias,grep,prompt,nvm,completion,custom};
do
  [ -f "$dotfile" ] && \. "$dotfile"
done
# Clean up
unset dotfile
```
