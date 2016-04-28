raspberry-pi-static-address
====
How to set a static IP address on the Raspberry Pi.

This is valid from Raspbian Jessie (v. 8) on.

```
sudo nano /etc/dhcpcd.conf
```

Then add the following for wifi and/or wired interface
```
interface eth0
static ip_address=192.168.1.101/24
static routers=192.168.1.1
static domain_name_servers=192.168.1.1
interface wlan0
static ip_address=192.168.1.201/24
static routers=192.168.1.1
static domain_name_servers=192.168.1.1
```
