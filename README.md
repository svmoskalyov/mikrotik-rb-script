![This is an image](mikrotik.png)

## :man_beard: This is my configuration script router MikroTik RB7... RB9... :rocket:

RouterMode:

- WAN port is protected by firewall and enabled DHCP client
- Wireless and Ethernet interfaces (except WAN port ether) are part of LAN bridge

### Private Address Space [subnet calculator tool](https://subnet.im)

> 10.0.0.0 - 10.255.255.255 (10/8 prefix)

> 172.16.0.0 - 172.31.255.255 (172.16/12 prefix)

> 192.168.0.0 - 192.168.255.255 (192.168/16 prefix)

---

### Configuration

...before...

- connect a laptop to ether1 port
- run to winbox and connect to router (login: admin, password:(none))
- run to terminal
- reset configuration

```
/system reset-configuration no-defaults=yes skip-backup=yes
```

- change user

```
/user add name="NewAdmin" password="PASSWORD" group=full
```

```
/user set [find name="admin"] disable="yes"
```

- file, change the [:global] settings to your own
- all copy from file MikroTik-RB-my-script.ini and
  paste in to terminal, wait for end

...after...

- Check For Updates (System→Packages)
- Upgrade Firmware (System→Routerboard)
