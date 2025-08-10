# proxmox-notes

## Linux Initial Setup
```bash
sudo apt install -y qemu-guest-agent
```
```bash
sudo apt install -y qemu-guest-agent openssh-server
```


#### Remove Data after initial install and add space to root
```bash
lvremove /dev/pve/data
lvresize -l +100%FREE /dev/pve/root
resize2fs /dev/mapper/pve-root
```

#### Upgrade Proxmox
https://pve.proxmox.com/wiki/Downloads#Update_a_running_Proxmox_Virtual_Environment_8.x_to_latest_8.4

