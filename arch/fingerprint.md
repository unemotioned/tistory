# Fingerprint (ThinkPad T14 / Synaptics 06cb:00f9)

---

## Install

```sh
sudo pacman -S fprintd libfprint
```

## Enable

```sh
sudo systemctl enable --now fprintd
```

## Enroll & Verify

Run **without sudo** — fingerprint must be enrolled as your user, not root.

```sh
fprintd-enroll -f right-index-finger
fprintd-verify -f right-index-finger
```

### Enroll stages

| Stage | Meaning |
|---|---|
| `enroll-stage-passed` | Good scan captured from a specific angle/pressure |
| `enroll-retry-scan` | Bad scan — finger lifted too early, wrong angle, or too dry |
| `enroll-completed` | Enough scans collected, fingerprint template built |

Requires ~8 good scans.

## PAM Integration

`/etc/pam.d/sddm`:
```
auth sufficient pam_fprintd.so
auth include system-login
```

`/etc/pam.d/hyprlock`:
```
auth sufficient pam_fprintd.so
auth include login
```

`sufficient` means either fingerprint **or** password unlocks — whichever succeeds first.

## hyprlock.conf

```
fingerprint {
    enabled = true
    ready_message = Scan fingerprint
    present_message = Scanning...
    error_message = Fingerprint error
}
```

## Troubleshooting

**`EnrollStart failed: PermissionDenied`**
polkit is blocking enroll for your user. Create `/etc/polkit-1/rules.d/50-fprintd.rules`:
```js
polkit.addRule(function(action, subject) {
    if (action.id == "net.reactivated.fprint.device.enroll" &&
        subject.isInGroup("wheel")) {
        return polkit.Result.YES;
    }
});
```
```sh
sudo systemctl restart polkit
```

**`enroll-duplicate`**
A fingerprint is already stored. Delete it first:
```sh
sudo fprintd-delete $USER
sudo fprintd-delete root
```

**`fprintd-list $USER` shows no fingers enrolled**
Fingerprint was enrolled as root. Delete root's print and re-enroll as your user:
```sh
sudo fprintd-delete root
fprintd-enroll -f right-index-finger
```

**`list_devices failed`**
fprintd is not running:
```sh
sudo systemctl start fprintd
```

**`python-validity` fails with "No matching devices found"**
`06cb:00f9` is supported by mainline `libfprint`, not `python-validity`:
```sh
sudo systemctl disable --now python3-validity open-fprintd
sudo pacman -S fprintd libfprint
sudo systemctl enable --now fprintd
```
