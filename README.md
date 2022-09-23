![This is an image](mikrotik.png)

# :man_beard: This is my configuration script router MikroTik RB7... RB9... :+1:

RouterMode:
- WAN port is protected by firewall and enabled DHCP client
- Wireless and Ethernet interfaces (except WAN port ether) are part of LAN bridge

## Private Address Space
10.0.0.0 - 10.255.255.255 (10/8 prefix)

172.16.0.0 - 172.31.255.255  (172.16/12 prefix)

192.168.0.0 - 192.168.255.255 (192.168/16 prefix)

...[subnet calculator tool](https://subnet.im)


### Configuration

#### Do it manually.
0. connect a laptop to ether1 port
1. reset configuration
```
/system reset-configuration no-defaults=yes skip-backup=yes
```
2. change user
```
/user add name="admin-2" password="PASSWORD" group=full
```
```
/user set [find name="admin"] disable="yes"
```
3. Check For Updates (System→Packages)
4. Upgrade Firmware (System→Routerboard)
5. clearin System-Script-Environment
