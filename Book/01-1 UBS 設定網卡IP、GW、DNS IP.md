# 01-1 UBS 設定網卡IP、GW、DNS IP

>**date_tag**: 210525


## 1.UBS 設定網卡IP、GW、DNS IP
---

**目標yaml檔**:

指令: 
```
1 sudo nano /etc/netplan/00-installer-config.yaml


# 內容修改 (並保存離開)
network:
  ethernets:
    ens32:
      dhcp4: no
      addresses: [ 120.96.143.191/24 ]
      gateway4: 120.96.143.254
      nameservers:
        addresses: [168.95.1.1,8.8.8.8]
  version: 2



2 檢測/吃設定 or 直接重啟設定
sudo netplan try
sudo netplan apply

#or
sudo reboot
```

<br /><br />
###### tags: `OS_Ubuntu 01`
