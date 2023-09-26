# Systemd Battery Log

A simple systemd service to regularly record the current battery percent and capacity. This can be useful to monitor battery health and usage over time. I use this to visualize my battery's capacity degradation over years of use.

This is designed for ArchLinux, which uses systemd timers in place of cron. The steps should be applicable to other linux distributions as well, but see your distribution's documentation first.

### Setup

1. Move `battery.service` and `battery.timer` to the systemd folder:

`sudo mv battery.service /etc/systemd/system/`

`sudo mv battery.timer /etc/systemd/system/`

2. Reload the systemd files with:

`systemctl daemon-reload`

Enjoy!
