# Usage

## Multiline single-quoted string

  - name: Add cronjob that Commits changes to wiki repo
    cron:
      name: "Commit changes to wiki repo"
      job: 'cd ~/development/wiki; git pull > /dev/null; git add . > /dev/null;
            git commit -m$(date +\%Y\%m\%dT\%H:\%M:\%SZ) > /dev/null;
            git push &>/dev/null'
