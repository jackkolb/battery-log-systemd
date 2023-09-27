# Systemd Battery Log

A simple systemd service to regularly record the current battery percent and capacity. This can be useful to monitor battery health and usage over time. I use this to visualize my battery's capacity degradation over years of use.

This is designed for ArchLinux, which uses systemd timers instead of cron. The steps should be applicable to other linux distributions as well, but see your distribution's documentation first.

### Setup

1. Make sure the `~/.config/systemd/user` folder exists:

`mkdir ~/.config/systemd`

`mkdir ~/.config/systemd/user`

2. Move `battery.service` and `battery.timer` to the systemd folder:

`mv battery.service ~/.config/systemd/user/`

`mv battery.timer ~/.config/systemd/user/`

3. Reload the systemd files with:

`systemctl daemon-reload`

4. Enable and start the service:

`systemctl enable --user battery.timer`

`systemctl start --user battery.timer`

Enjoy!
