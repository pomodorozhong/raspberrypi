# Headless setup for ssh

Reference: [Headless Raspberry Pi 4 SSH WiFi Setup (Mac + Windows, 10 Steps) – desertbot.io](https://web.archive.org/web/20211221043445/https://desertbot.io/blog/headless-raspberry-pi-4-ssh-wifi-setup)

## Mac

```
touch /Volumes/boot/ssh
```

## Windows

### Method 1

+ Open up a command line
+ Switch to the drive and root where `boot` is located. Type:

```
type NUL >> ssh
```

+ Verify that file `ssh` was created

### Method 2

+ Run `Notepad`
+ In a new file put in one space and nothing more
+ Click File / Save As ...
+ Be sure to set Save as type to All Files (so the file is NOT saved with a .txt extension)
+ Call the file `ssh` and save it
+ Close the file
