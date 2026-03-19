# fprintd

Use fprintd to unlock hyprlock with finger prints

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

### Available fingers

- left-little-finger
- left-ring-finger
- left-middle-finger
- left-index-finger
- left-thumb

- right-thumb
- right-index-finger
- right-middle-finger
- right-ring-finger
- right-little-finger

```sh
sudo fprintd-enroll -f right-index-finger
```

### Enroll stages

Requires about 8 good scans

| Stage                 | Meaning                    |
| --------------------- | -------------------------- |
| `enroll-stage-passed` | Good scan                  |
| `enroll-retry-scan`   | Bad scan                   |
| `enroll-completed`    | Fingerprint template built |

```sh
sudo fprintd-verify -f right-index-finger
```

## Troubleshooting

### enroll-duplicate

A fingerprint is already stored. Delete it first:

```sh
sudo fprintd-delete $USER
# or
sudo fprintd-delete root
```
