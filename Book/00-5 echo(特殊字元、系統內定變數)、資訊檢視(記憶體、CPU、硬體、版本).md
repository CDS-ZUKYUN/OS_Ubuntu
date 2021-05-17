# 00-5 echo(特殊字元、系統內定變數)、資訊檢視(記憶體、CPU、硬體、版本)

>**date_tag**: 0326
>
>**word_tag**: 雲端與SRE網站可靠性工程師班.docx

>**Tip**.  Ubconsole 使用ctrl + k能刪除(剪)游標後整行指令,ctrl + u能貼回

## 1.echo (特殊字元)

> 1. 顯示...痾,**特殊字元**
> 
> 2. bash設定變數
> 
> 3. 系統內定變數

```
1 echo -e "Name:${name}\nAge:${age}\t${name} ${age}"
 [命令][-e 特殊字元處理參數\n \t ---------------------]

2 nano grep.sh
#!/bin/bash
value=$(df –h | grep /dev/sda2)
     [等效`-命令--------------`]   
[變數塞進][命令結果-------------]
echo $value | cut –d ‘ ‘ –f2
   [變數內容][串接 cut命令]

3 
$ nano myarg.sh
#!/bin/bash 
echo $0 
echo $1 
echo $#  
    [參數個數]
echo $@  
    [含所有參數]

檢驗:
$ chmod +x myarg.sh 
      [執行權]
$ ./myarg.sh lee ton lin 
             [參數1 2 3 ]

```

</br>

## 2.資訊檢視(記憶體、CPU、硬體、版本)

>1. **記憶體**大小: **free** 
>
>2. 取出**CPU**型號: **/proc/cpuinfo**
>
>3. **硬體**使用量: **df**
>
>4. **Ubuntu版本**: **/etc/os-release**、**uname -a**
```
1 free -mh | grep Mem | fmt -u | cut -d ' ' -f2 
[mb/人看得懂][抓關鍵字''][把空格濃縮] [根據' '切欄,取第二欄 ]

2 cat /proc/cpuinfo | grep 'model name'

只取第一行, 並且刪除 "model name :
cat /proc/cpuinfo | grep 'model name' | fmt -u | cut -d ':' -f3
                                               [-d設定間格符號]
                                               
3.  df -h
      [人能看]
只取出上面結果的 "1.9T"

4 cat /etc/os-release
或 uname -av
```

<br /><br />
###### tags: `OS_Ubuntu 00`