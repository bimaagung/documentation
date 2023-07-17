## How to limit battery on linux

1.Open terminal
```
sudo nano /etc/crontab
```

2. Add last line in this file
```
@reboot root echo 60 > /sys/class/power_supply/BAT0/charge_control_end_threshold
```