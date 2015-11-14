# bashAlias
Back up for my aliases of in bashrc


alias ..='cd ..'
alias ...='cd ../..'
alias update='sudo apt-get update && sudo apt-get upgrade --yes'
alias install='sudo apt-get install'
alias c='clear'
alias ls='ls -al --color=auto'
alias grep='grep --color=auto'
alias egrep='egrep --color=auto'
alias fgrep='fgrep --color=auto'
alias h='history'
alias netRestart='sudo ifconfig wlan0 down && sudo ifconfig wlan0 up'
alias mv='mv -i'
alias cp='cp -i'
alias ln='ln -i'
alias root='sudo -i'
alias reboot='sudo /sbin/reboot'
alias poweroff='sudo /sbin/poweroff'
alias halt='sudo /sbin/halt'
alias shutdown='sudo /sbin/shutdown'
alias home='cd ~'
mcd() { mkdir -p "$1"; cd "$1";}
alias mkdir='mcd'
extract() { 
    if [ -f $1 ] ; then 
      case $1 in 
        *.tar.bz2)   tar xjf $1     ;; 
        *.tar.gz)    tar xzf $1     ;; 
        *.bz2)       bunzip2 $1     ;; 
        *.rar)       unrar e $1     ;; 
        *.gz)        gunzip $1      ;; 
        *.tar)       tar xf $1      ;; 
        *.tbz2)      tar xjf $1     ;; 
        *.tgz)       tar xzf $1     ;; 
        *.zip)       unzip $1       ;; 
        *.Z)         uncompress $1  ;; 
        *.7z)        7z x $1        ;; 
        *)     echo "'$1' cannot be extracted via extract()" ;; 
         esac 
     else 
         echo "'$1' is not a valid file" 
     fi 
} 
alias websiteget="wget --random-wait -r -p -e robots=off -U mozilla"
