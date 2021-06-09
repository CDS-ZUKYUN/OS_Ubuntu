# 01-0 UBS Ipv6 disable(永久、非正規)

>**date_tag**: 210525


## 1.UBS Ipv6 disable (永久)
---

**linux kernel 啟動過程就disable ipv6**:

指令: 
```
1 sudo nano /etc/default/grub

# 內容修改 (並保存離開)
GRUB_CMDLINE_LINUX="ipv6.disable=1"


2 sudo update-grub
sudo reboot
```

<br />

## 2.UBS Ipv6 disable (非正規)
---

**指令**: 
```
1 sudo nano /etc/sysctl.conf

# 增加 (並保存離開)
net.ipv6.conf.all.disable_ipv6 = 1


2 sysctl -p
```


<br /><br />
###### tags: `OS_Ubuntu 01`


