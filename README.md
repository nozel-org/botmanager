# botmanager
Botmanager is a convenience tool for managing our programs on your FreeBSD system.

## Features
* Show a overview of installed programs, their versions and available updates.
* Install, update (optionally automated/unattended) and remove software

## How to use
Run `botmanager --overview`, `botmanager --install`, `botmanager --update` or `botmanager --remove` for their respective functions. You can enable automatic unattended updates at 1:00 each day with `botmanager --cron` and disable this with `botmanager --disable-cron`.

## How to install
Copy `botmanager` to `/usr/local/etc/botmanager` (owner=`root`,group=`wheel`,permissions=`555`). This will look something like:
```
# install botmanager
wget https://raw.githubusercontent.com/nozel-org/botmanager/main/botmanager -O /usr/local/bin/botmanager
chown root:wheel /usr/local/bin/botmanager
chmod 555 /usr/local/bin/botmanager
```

## Support
If you have questions, suggestion or find bugs, please let us know via Issues.

## Changelog
### 1.0.0-RELEASE (21-05-2023)
- Added overview feature.
- Added install feature.
- Added update feature.
- Added unattended update feature.
- Added remove feature.
- Added automatic cronjob creation feature.