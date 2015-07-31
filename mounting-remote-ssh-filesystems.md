### Prerequisites

```
sudo apt-get install sshfs
```

### Instructions

Uncomment the following line in `/etc/fuse.conf`
```
#user_allow_other
```

Create the folder
```
mkdir /mnt/server1
```

Edit your `/etc/fstab`
```
username@server1.domain.com:/project/www/ /mnt/server1  fuse.sshfs allow_other,reconnect,_netdev,users,idmap=user,ServerAliveInterval=30,IdentityFile=/home/user/.ssh/id_rsa 1000 1000
```

Reboot.
