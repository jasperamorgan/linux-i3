# linux-i3
Notes and configs for Linux i3 configs

# Device configs

## Set the screen resolution for i3.

1/ Use xrandr to identify attached displays and available resolutions:

`xrandr`

2/ Exec xrandr from the  i3 config

Edit ~/i3/config

Add `exec --no-startup-id xrandr --output OUTPUT --mode MODE`

Example `exec --no-startup-id xrandr --output eDP1 --mode 2048x1152`
