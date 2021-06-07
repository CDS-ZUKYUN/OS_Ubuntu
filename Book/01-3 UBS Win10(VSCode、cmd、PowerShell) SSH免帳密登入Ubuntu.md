# 01-3 UBS Win10(VSCode、cmd、PowerShell) SSH免帳密登入Ubuntu 

date_tag: 0531


## 1. SSH免帳密登入ubuntu

**備註**:
>使用cmd/powershell在C:\Users\zukyun> 家目錄下操作

**指令**:

```
[產生公私鑰，吃預設enter到底]
[cmd執行完下面指令，由於不吃$USER_AT_HOST變數設定，切換powershell來用]
C:\Users\zukyun>ssh-keygen -t rsa -b 4096

[powershell]
PS C:\Users\zukyun> $USER_AT_HOST="bigred@192.168.0.191"
PS C:\Users\zukyun> $PUBKEYPATH="$HOME\.ssh\id_rsa.pub"


PS C:\Users\zukyun> $pubKey=(Get-Content "$PUBKEYPATH" | Out-String); ssh "$USER_AT_HOST" "mkdir -p ~/.ssh && chmod 700 ~/.ssh && echo '${pubKey}' >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys"

~Fin~
```

</br>

**VSCode SSH設定補充**:

```
ssh config:

# Read more about SSH config files: https://linux.die.net/man/5/ssh_config
Host 192-168-0-191-m1
    HostName 192.168.0.191
    User bigred
    IdentityFile C:\\Users\\zukyun\\.ssh\\id_rsa
    [視情況加Identityfile這行，基本上不用+也行]
```

<br /><br />
###### tags: `OS_Ubuntu 01`
