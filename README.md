# Lock Screen After Resume

A user space script to guarantee screen lock.

## Why is this necessery?

In my desktop environment,  that is,  on the GNOME desktop,  the screen before locking may appear very rarely after resumed.  As a result of examining various next-best solutions,  I decided to implement a mechanism to guarantee the lock after resume,  not before suspend.

This script considers a long CPU stop as resume.  When the resume is detected, the script calls screen lock command (`xdg-screensaver lock` by default).  The screen will be visible for a brief time until the script works.  But it will be somewhat better if it remains visible.

## Prerequisites

- `xdg-screensaver` (if you use in GNOME desktop environment)

## Installation

`~/.config/autostart/lock-screen-after-resume.desktop`:

```
[Desktop Entry]
Type=Application
Name=Lock Screen After Resume
Exec=/path/to/lock-screen-after-resume
X-GNOME-Autostart-enabled=true
```

## Configuration

See help (`-h` option) for more details.

## Development

Developed and tested on [Arch Linux](https://archlinux.org/).
