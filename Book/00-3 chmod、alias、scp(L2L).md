# 00-3 chmod、alias、scp(L2L)

>date_tag: none
>
>pptx_tag: none



## chmod


>1. 檔案權限設定
>
>2. 查看檔案權限
>
>3. 執行程式
```
1.
格式1: chmod +x filename
Example1: chmod +x kisscode.sh

格式2: chmod 777 filename (User、Group、及Other的許可權；r=4，w=2，x=1)
Example1: chmod 777 kisscode.sh


2. ls -al (filename)
註: () 表可略

3.格式1: ./filename
  格式2: source filename  (無須x執行權便可run code)
```


## alias

>改命令裝

```
Example1: alias myip=’./myip.sh’
```


## scp (L2L)

>檔案複製到遠端

```
Example1: 
scp /home/bigred/filename rbean@192.168.157.134:/home/rbean/refilename
```


<br /><br />
###### tags: `OS_Ubuntu 00`