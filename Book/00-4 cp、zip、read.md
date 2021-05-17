# 00-4 cp、zip、read

>date_tag: 0326
>
>word_tag: 雲端與SRE網站可靠性工程師班.docx


## 1.cp

> 複製檔案

```
$ cp kiss.txt kfolder/kiss2.txt
$ ls kfolder/

```

</br>

## 2.zip

>1. 安裝
>
>2. 解壓縮

```
1. sudo apt install zip unzip 

2. 格式:zip –r test.zip wk/
             [壓縮檔名稱] [欲壓目錄路徑]

Tip: 沒有-r, 目錄若有階層，檔案會被解在第一層目錄
```

</br>

## 3.read

>
>

```
read -p "input name&&age: " name age
   [附提示] [提示內容-------] [參數愛塞多少空白多少]
```


<br /><br />
###### tags: `OS_Ubuntu 00`