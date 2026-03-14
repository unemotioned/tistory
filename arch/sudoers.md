# Sudoers

In terminal when typing password for `sudo` show asterisk for feedback

```sh
sudo visudo
```

This will open `/etc/sudoers.tmp` file

some where in the `Defaults Specification`
add the following line:

```sudoers
Defaults pwfeedback
```

> Preferably between `Defaults` and `Runas alias` specifications.
