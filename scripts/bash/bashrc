#################################################
#   BASHRC  -  LUCFR.COM  -  UPDATED 07.13.2017
#################################################

export LS_OPTIONS='--color=auto --group-directories'
eval "`dircolors`"

####    PROMPT
PS1='[\u@\h \W]\$ '

####    SYSTEM ALIASES

alias ls='ls -FHXx $LS_OPTIONS'

####    USER ALIASES

alias goroot='cd /'
alias gohome='cd ~'


#################################################
#   END CUSTOM SHIT
#################################################

####    RUNNING INTERACTIVELY
[[ $- != *i* ]] && return

####    DISPLAY SHIZ
[[ $DISPLAY ]] && shopt -s checkwinsize

####    TERMINAL
case ${TERM} in
  xterm*|rxvt*|Eterm|aterm|kterm|gnome*)
    PROMPT_COMMAND=${PROMPT_COMMAND:+$PROMPT_COMMAND; }'printf "\033]0;%s@%s:%s\007" "${USER}" "${HOSTNAME%%.*}" "${PWD/#$HOME/\~}"'
    ;;
  screen*)
    PROMPT_COMMAND=${PROMPT_COMMAND:+$PROMPT_COMMAND; }'printf "\033_%s@%s:%s\033\\" "${USER}" "${HOSTNAME%%.*}" "${PWD/#$HOME/\~}"'
    ;;
esac

####    BASH COMPLETION SHIZ
[ -r /usr/share/bash-completion/bash_completion   ] && . /usr/share/bash-completion/bash_completion
