# Mella
ownCloud upload via WebDAV using curl
Copyright (c)2015 by [Florian Beer](https://github.com/florianbeer)
Version 1.00

This script comes with ABSOLUTELY NO WARRANTY.
This is free software, and you are welcome to redistribute it
under certain conditions. See CC BY-NC-SA 4.0 for details.
https://creativecommons.org/licenses/by-nc-sa/4.0/

Usage: `mella [OPTIONS] SOURCE TARGET`

## Explanation
Mella is a bash script for file uploads to ownCloud.

Store your ownCloud credentials in `~/.mella.conf` or any other file and pass it's path via the `-c` commandline switch.
Target is you ownCloud WebDAV URL. You can find it by clicking on "Settings" in the lower left hand corner of ownCloud's webinterface.

## Options
```
 -c FILE  optional path to credentials file (default is ~/.mella.conf)
 -v       increase verbosity
 -h       show this message
 -V       show version number
```

## Examples
```
 mella -c myconfig.conf backup.tar.gz http://demo.owncloud.org/remote.php/webdav/
 mella backup.tar.gz http://demo.owncloud.org/remote.php/webdav/backup_dir
```

## Usage
* Save this shell script to e.g. `/usr/local/bin/mella` and make it executable: `chmod +x /usr/local/bin/mella`
* Create a new file in your home directory called `.mella.conf` and list your username and password as the only content, separated by a colon `username:password`.
