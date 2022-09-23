![This is an image](mikrotik.png)

## :man_beard: This is my configuration script router MikroTik RB7... RB9... :rocket:

RouterMode:
- WAN port is protected by firewall and enabled DHCP client
- Wireless and Ethernet interfaces (except WAN port ether) are part of LAN bridge

### Private Address Space   [subnet calculator tool](https://subnet.im)
> 10.0.0.0 - 10.255.255.255 (10/8 prefix)
> 172.16.0.0 - 172.31.255.255  (172.16/12 prefix)
> 192.168.0.0 - 192.168.255.255 (192.168/16 prefix)
---

### Configuration

#### In start
...before...
1.  connect a laptop to ether1 port
2.  run to winbox and connect to router (login: admin, password:(none))
3.  run to terminal
4.  reset configuration
```
/system reset-configuration no-defaults=yes skip-backup=yes
```
5.  change user
```
/user add name="NewAdmin" password="PASSWORD" group=full
```
```
/user set [find name="admin"] disable="yes"
```
6.  file, change the [:global] settings to your own
7.  all copy from file MikroTik-RB-my-script.ini and
paste in to terminal, wait for end
...after...
8.  Check For Updates (System→Packages)
9.  Upgrade Firmware (System→Routerboard)  
