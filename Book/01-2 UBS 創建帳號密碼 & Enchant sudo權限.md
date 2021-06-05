# 01-2 UBS 創建帳號密碼 & Enchant sudo權限
date_tag: 0605

## 1. 創建帳號密碼

**備註**:
>使用sudo bigred帳號操作

**指令**:

```
~$ sudo useradd -s /bin/bash -m rbean
               [指定shell]  [創/home/rbean]
~$ sudo passwd rbean
```

</br>

## 2. Enchant sudo權限

```
方法一
~$ sudo usermod -aG sudo rbean
                [wheel]

方法二
[user enchant sudoright]
~$ sudo nano /etc/sudoers

# User privilege specification
root ALL=(ALL:ALL) ALL
rbean ALL=(ALL:ALL) ALL
```
<br /><br />
###### tags: `OS_Ubuntu 01`
