# common commands and aliases

| scenario | alias  | command |
|:---------|:-------|:--------|
| show last commit | `git last` | `git log -1 HEAD` |
| unstage a file | `git unstage` | `git reset HEAD --` |
| short log | `git l` | `git log --pretty=format:"%C(yellow)%h\\ %ad%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --date=short` |
| more verbose log showing the names of changed files | `git ll` |  `git log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat`
| short log with graph | `git lg` | `git log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all` |
| more verbose log with graph | `git log2` | `git log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all` |
| list branches by last modified | `git b` | `git for-each-ref --sort='-authordate' --format='%(authordate) %(objectname:short) %(authorname) %(refname)' refs/heads \| sed -e 's-refs/heads/--'` |
| undo last commit | `git undo-commit` | `git reset --soft HEAD~1` |

# Diffs
> use `git log -p` to see diffs in the log <br>

![](https://i.stack.imgur.com/tVHYO.png)
