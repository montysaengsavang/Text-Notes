```
ZSH_THEME="robbyrussell"

plugins=(git)

source $ZSH/oh-my-zsh.sh

# User configuration


# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.
#
# Example aliases
# alias zshconfig="mate ~/.zshrc"
# alias ohmyzsh="mate ~/.oh-my-zsh"

GHUB_TOKEN='token-here'
alias gtok="echo $GHUB_TOKEN"
alias tok="gtok | pbcopy"

alias where="pwd | pbcopy"

alias build="docker-compose up --build"

alias another="open -a iterm ."
alias info="open https://github.com/montysaengsavang/Text-Notes"
alias search="open https://github.com/montysaengsavang"

goto() {open $(git config remote.origin.url | sed "s/git@\(.*\):\(.*\).git/https:\/\/\1\/\2/")/tree/$(git symbolic-ref --quiet --short HEAD )/$(git rev-parse --show-prefix)}

glab() {open https://gitlab.com/$(basename $(git rev-parse --show-toplevel))/-/tree/$(git symbolic-ref --quiet --short HEAD )/$(git rev-parse --show-prefix)}

alias k='kubectl'
alias d='docker'

code () { VSCODE_CWD="$PWD" open -n -b "com.microsoft.VSCode" --args $* ;}
```
