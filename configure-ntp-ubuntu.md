# Quick guide on how to configure ntp time synchronization on a ubuntu system.

1. Set your timezone:

```
sudo timedatectl set-timezone "America/Los_Angeles"
```

2. Add an NTP entry in configuration:

```
sudo nano /etc/systemd/timesyncd.conf

Add an entry similar to:

NTP=1.2.3.4   # This will point to the ip/fqdn of your ntp server

(ctrl-x) to write changes, (y) to save modifications, then hit (enter) to select the file where changes are saved.
```

3. Toggle service off and then on:

```
sudo timedatectl set-ntp off
sudo timedatectl set-ntp on
```