# Internet

Use wired connection when connected via thunderbolt.

network backend: `iwd`

---

## Check interfaces

```sh
ip link show
```

output:

`2: enp0s31f6`: dedicated ethernet port

`4: wlan0`: wifi

`5: enp85s0`: interface of thunderbolt

---

## Configure

Prioritize thunderbolt interface to Wi-Fi

```sh
sudo -E nvim /etc/systemd/network/20-wired.network
```

```ini
[Match]
Name=enp85s0

[Network]
DHCP=yes

[DHCPv4]
RouteMetric=10
```

```sh
sudo -E nvim /etc/systemd/network/30-wireless.network
```

```ini
[Match]
Name=wlan0

[Network]
DHCP=yes

[DHCPv4]
RouteMetric=20
```

---

## Apply

```sh
sudo systemctl restart systemd-networkd
```
