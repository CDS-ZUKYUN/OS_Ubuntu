# 00-2 sudo指令後不打帳號密碼、導引符號、nano操作

>date_tag: none
>
>pptx_tag: none



## sudo指令後不打帳號密碼



> Tip 小心改壞毀一生
>

```
$ sudo nano /etc/sudoers

before
# Allow members of group sudo to execute any command
%sudo   ALL=(ALL:ALL) ALL

after
%sudo   ALL=(ALL:ALL) NOPASSWD:ALL

```

## 導引符號

>1. 導輸出成文字檔
>
>Tip. linux的副檔名有點那麼不重要，但又很重要。

```
1. cowsay -f kiss “kiss” > kiss.txt
cat kiss.tx 
```


## nano

>1. 開文檔 (宣告指定shell來coding)

```
1. nano kisscode.sh

內容:
#!/bin/bash

基本重要操作:
I. ctrl +o;按enter存檔 
II. ctrl + x 離開編輯器
III. shift + alt + 3 顯示行數

```

<br /><br />
###### tags: `OS_Ubuntu 00`