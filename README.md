# sysadmin-util-tiny
scripts that might be usefull for different ranges of work on most linux distributions.
## requirements
- python3
- sh
### optional
- net-tools (for `gateway`)
- systemd (for `userctl`)

## docs
### gateway _\[options\]_
Get current gateway(s)

`$ gateway`

```
wlo1 192.168.2.254
eno1 10.0.10.254
```
- `-h` `--help` Show help and exit
- `-i<interface>` `--interface <interface>` Show details for a single network interface

### passgen _\<length\> \[options\]_
Generate a password

`$ passgen 16`
```
OZF#x`ObS%nx<Rf,
```
- `-h` `--help` Show help and exit
- `-s` `--no-special` Excludes special characters from the generated password
- `-n` `--no-numeric` Excludes numeric characters from the generated password
- `-a` `--no-alphabetical` Excludes alphabetical characters from the generated password

### userctl
Because writing `systemctl --user` is simply too much work.

Works the same as `systemctl` except it will run on user level.

`$ userctl status ssh-agent`

`$ systemctl --user status ssh-agent`
