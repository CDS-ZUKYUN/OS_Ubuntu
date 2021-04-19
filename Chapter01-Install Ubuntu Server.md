# US_Chapter 01. Install Ubuntu Server


* * *

<h2 id="iso">step1.下載Ubuntu_ISO映像檔</h2>


* Ubuntu 官網 : https://ubuntu.com。

![Ubs_ISO_file](https://i.imgur.com/zTvcK1u.png)

---
<br />
<br />
<h2 id="VMconfig">step2.VM配置</h2>

注意創建(Create)時，選的版本。
ubuntu-20.04.2-live-server-amd64.iso <br />

![VMw_config_p1](https://i.imgur.com/RJzwZYv.png)
<br />
<br />

注意命名需有意義，不倚靠感覺，例如做webserver用，那就最好如下例做命名；並且，請注意將OS放在跑最快的C槽，設定的路徑要簡單好找。<br />
![VMw_config_p2](https://i.imgur.com/1FyrkAH.png)<br />
<br />


* start

1.OS 環境語系設定

![os_envir_language](https://i.imgur.com/L8gXC8h.png)

<br />

2.Keyboard 美式配置(備用鍵盤配置)

![keyboard_layout](https://i.imgur.com/GJwny1l.png)

<br />

3.網卡選擇
> 能手動配置ip 用manual
> Bond 增添網卡的機制(整合來同時作業)，以前整合網卡用的

![netcard](https://i.imgur.com/A5DTIAJ.png)

<br />

4.透過代理伺服器(身分)聯網

![set_proxy](https://i.imgur.com/7dqfdRE.png)

<br />

5.US Mirror address (安裝時更新系統的網頁source)

![mirror_url](https://i.imgur.com/NjLvccY.png)

<br />

6.將硬碟以LVM 能通過需要再擴充硬碟


![LVM](https://i.imgur.com/y4lsvNA.png)

<br />

7.US整體配置check

![US_install_config](https://i.imgur.com/cNiAf3J.png)

![continue](https://i.imgur.com/4H42ftx.png)

<br />

8.創建帳號
> Your name是創一個具有sudo(root)權限的帳號
> 
> server name 伺服器主機名稱
> 
> username 欲創建帳戶名，若是與your name相同，會整合成有sudo(root)權限的帳號
> 
> 設定密碼


![account](https://i.imgur.com/LOxiBWh.png)

<br />

9.安裝OpenSSH 遠端連線管理(空白鍵選起來是X，TAB跳選項)

![op_ssh](https://i.imgur.com/ePZZkqs.png)

<br />

10.選擇套件安裝(這裡都不必選)

![apk_list](https://i.imgur.com/3vuo4vs.png)

<br />

11.等待安裝reboot

![reboot](https://i.imgur.com/eT7cnhh.png)

<br />



12 安裝好會有等待畫面

>Enter 虛擬光碟會退掉ISO，應用該裝好的os。
>
>下一步再登錄
>
>要記得從VMware退ISO

<br />



13.Fin

![fin](https://i.imgur.com/yleMpWR.png)
