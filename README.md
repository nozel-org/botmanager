# botmanager

Botmanager is a convenience tool for managing Nozel programs on your FreeBSD system.

## Features

* Show a overview of installed programs, their versions and available updates.
* Install, update (optionally automated/unattended) and remove software.

## How to use

```
Usage:
  botmanager [feature]...
  botmanager [option]...

Features:
  -o, --overview             Shows the bot status on this device
  -i, --install              Install one of the bots
  -r, --remove               Remove a installed bot
  -u, --update               Update all installed bots
      --unattended           Add to --update for unattended action
Options:
  --cron                     Set daily automatic update
  --disable-cron             Set daily automatic update
  --help                     Display this help and exit
  --version                  Display version information and exit
```

## How to install

Copy `botmanager` to `/usr/local/etc/botmanager` (owner=`root`,group=`wheel`,permissions=`555`). This will look something like:

```
# install botmanager
wget https://codeberg.org/nozel/botmanager/raw/branch/main/botmanager -O /usr/local/bin/botmanager
chown root:wheel /usr/local/bin/botmanager
chmod 555 /usr/local/bin/botmanager
```

## Support

If you have questions, suggestion or find bugs, please let us know via Issues.

## Changelog

### 2.0.0-RELEASE ([06-04-2025](https://codeberg.org/nozel/botmanager/commit/32df74e51e80d408e918120303fc153b327c5e90))

- Changed license to Apache 2.0 #7.
- Made botmanager independent from hard coded package names #3.
- Reworked option_version and added version date.
- Removed colors from features and options.
- Reworked program errors.
- Reworked program logs via logger.
- Replaced wget dependency with curl #8.
- Added rudimentary support for self updating #1.

### 1.0.0-RELEASE ([21-05-2023](https://codeberg.org/nozel/botmanager/commit/e0818e346abb115b99a7833ecd79d9a3cc84ac64))

- Added overview feature.
- Added install feature.
- Added update feature.
- Added unattended update feature.
- Added remove feature.
- Added automatic cronjob creation feature.
