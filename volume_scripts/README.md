CC Zero, <jaggz.h@gmail.com>

# Some scripts for working with pulseaudio system volume

Lets you save and restore volume. Useful in scripts.

Example:

``
$ volstore
$ volset 33
$ play alarm.wav
$ volrestore
```

## Installation:

1. volstore and volrestore use a file in ~/tmp/ which you might not have.
1. mkdir ~/tmp  (or edit those scripts to change the path)
1. Copy or symlink these scripts into your favorite bin/ dir

## Notes:

1. volmuteget is a link to volget.  It can be named anything with the word 'mute' in it and it'll be in "get the mute state" mode, otherwise it defaults to outputting the volume.
