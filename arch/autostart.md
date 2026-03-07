# Autostart

## NM-Applet

Stop `nm-applet` from automatically starting

check if it's in here

```sh
ls /etc/xdg/autostart
```

add `Hidden=true` to the `nm-applet.desktop` file

### Shell Command

```sh
sudo sh -c 'echo "Hidden=true" >> /etc/xdg/autostart/nm-applet.desktop'
```
