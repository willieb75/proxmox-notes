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
