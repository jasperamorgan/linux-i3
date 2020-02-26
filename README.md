# linux-i3
Notes and configs for Linux i3.

# i3 Config

## Desktops

TODO: Which apps go to which desktops. Current idea:

1: Email (Thunderbird?)  

2: Chat Apps (Slack, MS Teams)

3: Browser (Firefox / Brave)

4: (Empty)

5: Terminals

6: IDEs (Spacemacs, VS Code)

7: Browsers (Surf, Palemoon)

8: KVM (OSX, Windows) 

9: (Empty)

# Appearance (

1. [Yaru Theme](./yaru-theme.md)


# Device configs

## Set the screen resolution for i3.

1/ Use xrandr to identify attached displays and available resolutions:

`xrandr`

2/ Exec xrandr from the  i3 config

Edit ~/i3/config

Add `exec --no-startup-id xrandr --output OUTPUT --mode MODE`

Example `exec --no-startup-id xrandr --output eDP1 --mode 2048x1152`

## Set natural mouse/touchpad scrolling

1/ Edit `/usr/share/X11/xorg.conf.d/40-libinput.conf`

2/ Add natural scrolling to the mouse config

```
Section "InputClass"
        Identifier "libinput pointer catchall"
        MatchIsPointer "on"
        MatchDevicePath "/dev/input/event*"
        Driver "libinput"
        Option "NaturalScrolling" "True"
EndSection
```

3/ Add natural scrolling to the touchpad config

```
Section "InputClass"
        Identifier "libinput touchpad catchall"
        MatchIsTouchpad "on"
        MatchDevicePath "/dev/input/event*"
        Driver "libinput"
        Option "NaturalScrolling" "True"
EndSection
```
## Two finger touchpad right click

TODO
