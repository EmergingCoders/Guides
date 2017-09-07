## Make your terminal look better

These are my personal settings for my terminal, you may copy this and edit as you please. 

You want to replace the .bash_profile file in your root directory with this. 

You can do this using the command:
```vi ~/.bashrc```

If you are not familiar with vi/vim use you will first need to:
press ```escape``` + ```:set paste```

Then press ```i``` to go into insert mode. 

At the bottom of the file, paste the following:


```sh
export PS1="\[\033[36m\]\u\[\033[m\]@\[\033[32m\]\h:\[\033[33;1m\]\w\[\033[m\]\$ "
export CLICOLOR=1
export LSCOLORS=ExFxBxDxCxegedabagacad

toilet -f mono12 -F gay "Simeon  Kakpovi"
alias docs='cd /Users/simeonkakpovi/Documents'
alias down='cd /Users/simeonkakpovi/Downloads'
alias desk='cd /Users/simeonkakpovi/Desktop'
alias husb='cd /Users/simeonkakpovi/Documents/hu_webmaster/bschoolbeta'
alias grepc="grep --color=always"
alias histogram="sort | uniq -c | sort -rn"
alias ttop="top -R -F -s 10 -o rsize"
alias tree="find . -print | sed -e 's;[^/]*/;|____;g;s;____|; |;g'"

alias la='ls -a'
alias lf='ls -alt'
alias ll='ls -lhS'

alias settings='vim ~/.bash_profile'
alias reload='source ~/.bash_profile'
```
