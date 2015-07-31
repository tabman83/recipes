### Prerequisites

```
sudo apt-get install sshfs
```

### Instructions

Create the folder
```
mkdir /mnt/server1
```

Edit your `/etc/fstab`
```
username@server1.domain.com:/project/www/ /mnt/server1  fuse.sshfs allow_other,reconnect,_netdev,users,idmap=user,IdentityFile=/home/user/.ssh/id_rsa 0 0
```

Reboot.
