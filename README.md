![This is an image](mikrotik.png)

# :man_beard: This is my configuration script router MikroTik RB7... RB9... :rocket:

RouterMode:
- WAN port is protected by firewall and enabled DHCP client
- Wireless and Ethernet interfaces (except WAN port ether) are part of LAN bridge

### Private Address Space :link:[subnet calculator tool](https://subnet.im)
10.0.0.0 - 10.255.255.255 (10/8 prefix)

172.16.0.0 - 172.31.255.255  (172.16/12 prefix)

192.168.0.0 - 192.168.255.255 (192.168/16 prefix)


###     Configuration

#### In start
0. :small_orange_diamond: connect a laptop to ether1 port
1. :small_orange_diamond: reset configuration
```
/system reset-configuration no-defaults=yes skip-backup=yes
```
2. :small_orange_diamond: change user
```
/user add name="NewAdmin" password="PASSWORD" group=full
```
```
/user set [find name="admin"] disable="yes"
```
3. :small_orange_diamond: Check For Updates (System→Packages)
4. :small_orange_diamond: Upgrade Firmware (System→Routerboard)
5. :small_orange_diamond: clearin System-Script-Environment
