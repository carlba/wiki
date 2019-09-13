# Usage

## Print all command line arguments sent to a script from within it

```bash
echo $@
```

## File checks

| Switch            | Meaning                                                                      |
|:------------------|:-----------------------------------------------------------------------------|
| -b filename       | Block special file                                                           |
| -c filename       | Special character file                                                       |
| -d directory name | Check for directory existence                                                |
| -e filename       | Check for file existence, regardless of type (node, directory, socket, etc.) |
| -f filename       | Check for regular file existence not a directory                             |
| -G filename       | Check if file exists and is owned by effective group ID.                     |
| -g filename       | true if file exists and is set-group-id.                                     |
| -k filename       | Sticky bit                                                                   |
| -L filename       | Symbolic link                                                                |
| -O filename       | True if file exists and is owned by the effective user id.                   |
| -r filename       | Check if file is a readable                                                  |
| -S filename       | Check if file is socket                                                      |
| -s filename       | Check if file is nonzero size                                                |
| -u filename       | Check if file set-user-id bit is set                                         |
| -w filename       | Check if file is writable                                                    |
| -x filename       | Check if file is executable                                                  |

## Samples

```bash
[[ ! -f $FILE ]]
```

## Color codes

https://wiki.archlinux.org/index.php/Color_Bash_Prompt

```bash
txtblk='\e[0;30m' # Black - Regular
txtred='\e[0;31m' # Red
txtgrn='\e[0;32m' # Green
txtylw='\e[0;33m' # Yellow
txtblu='\e[0;34m' # Blue
txtpur='\e[0;35m' # Purple
txtcyn='\e[0;36m' # Cyan
txtwht='\e[0;37m' # White
bldblk='\e[1;30m' # Black - Bold
bldred='\e[1;31m' # Red
bldgrn='\e[1;32m' # Green
bldylw='\e[1;33m' # Yellow
bldblu='\e[1;34m' # Blue
bldpur='\e[1;35m' # Purple
bldcyn='\e[1;36m' # Cyan
bldwht='\e[1;37m' # White
unkblk='\e[4;30m' # Black - Underline
undred='\e[4;31m' # Red
undgrn='\e[4;32m' # Green
undylw='\e[4;33m' # Yellow
undblu='\e[4;34m' # Blue
undpur='\e[4;35m' # Purple
undcyn='\e[4;36m' # Cyan
undwht='\e[4;37m' # White
bakblk='\e[40m'   # Black - Background
bakred='\e[41m'   # Red
bakgrn='\e[42m'   # Green
bakylw='\e[43m'   # Yellow
bakblu='\e[44m'   # Blue
bakpur='\e[45m'   # Purple
bakcyn='\e[46m'   # Cyan
bakwht='\e[47m'   # White
txtrst='\e[0m'    # Text Reset
```
