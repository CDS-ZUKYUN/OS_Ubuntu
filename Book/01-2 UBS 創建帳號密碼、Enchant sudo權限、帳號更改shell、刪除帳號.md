# 01-2 UBS 創建帳號密碼、Enchant sudo權限、帳號更改shell、刪除帳號
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
</br>

## 3. 帳號更改shell

```
方法一
~$ sudo usermod -s /bin/bash rbean
                             [$USERNAME]
                
方法二
~$ sudo nano /etc/passwd
[修改內容]
...
rbean ... /bin/bash
```
</br>

## 4. 刪除帳號

```
~$ sudo deluser --remove-home gbean
```


<br /><br />
###### tags: `OS_Ubuntu 01`
