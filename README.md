# Raspberry Pi Backup Images

Backup images and files for the multiple raspberry pi that are used.

## Authors

- [Juan Martinez Alonso](https://www.github.com/jmaralo)

## Installation

There are two methods to install the images to a raspberry pi:

### Using the disk image

The disk images can be found in the organization drive [here](https://drive.google.com/drive/folders/1GN090vUitxXud5ipQjksEpp0q7bFJphh?usp=share_link). Just flash it to the SD card as any other image and it is good to go.

### Using the backup files

The contents of `/files` are the files that must be uploaded to an already working raspberry with an OS.

This can be done with the `scp` command from the terminal. Go to the folder where both the `rc.local` and `dhcpcd.conf` files are located and run:

```bash
scp <raspberry_user>@<raspberry_ip>:/etc/rc.local rc.local
scp <raspberry_user>@<raspberry_ip>:/etc/dhcpcd.conf dhcpcd.conf
```

where `<raspberry_user>` is the username of the raspberry user (pi by default) and `<raspberry_ip>` is the current ip of the raspberry pi.
