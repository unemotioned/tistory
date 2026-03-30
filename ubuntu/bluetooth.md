# Bluetooth

## Start Bluetooth

From `gnome-desktop` if the bluetooth does not toggle enable

```sh
systemctl start bluetooth  # start bt service
systemctl enable bluetooth # start on every log in
```

- bluetooth: systemd integration
- bluez: tool + daemon
- blueman: gui manager

```sh
sudo apt install bluetooth bluez blueman
```
