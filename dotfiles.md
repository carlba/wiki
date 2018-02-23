
``` bash
function EXT_COLOR () { echo -ne "\e[38;5;$1m"; }
function CLOSE_COLOR () { echo -ne '\e[m'; }
export PS1="\[`EXT_COLOR 187`\]\u@\h\[`CLOSE_COLOR`\]\[`EXT_COLOR 174`\] \w \$ \[`CLOSE_COLOR`\]"
export LS_COLORS='di=38;5;108:fi=00:*svn-commit.tmp=31:ln=38;5;116:ex=38;5;186
```