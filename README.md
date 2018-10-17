# Lock Screen After Resume

A user space script to guarantee screen lock.

## Why is this necessery?

In my desktop environment,  that is,  on the GNOME desktop,  the screen before locking may appear very rarely after resumed.  As a result of examining various next-best solutions,  I decided to implement a mechanism to guarantee the lock after resume,  not before suspend.

This script considers a long CPU stop as suspend.  When the suspend is detected, it calls the screen lock command.  The screen will be visible for a brief time until the script works.  But it will be somewhat better if it remains visible.

## Prerequisites

- `xdg-screensaver` (if you use in GNOME desktop environment)

## Installation

```sh
sudo cp lock-screen-after-resume /usr/local/bin
lock-screen-after-resume.desktop.example ~/.config/autostart/lock-screen-after-resume.desktop
```

## Configuration

See help (`-h` option) for more details.

## Development

Developed and tested on [Arch Linux](https://archlinux.org/).
