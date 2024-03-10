# Launsh

A minimal terminal-based alternative to dmenu_path + {dmenu, rofi, wmenu, ...etc}, straight from my dotfiles :).

## Dependencies

+ fzf

## Install

```sh
git clone https://github.com/ocku/launsh.git
mkdir -pv ~/.local/bin/
install launsh ~/.local/bin/
```

^ Make sure to add `~/.local/bin` to your `$PATH`.

### Using Sway + Alacritty

If you're using Sway and Alacritty, add these three lines to your sway config.

`.config/sway/config`
```sway
# ... defs

# define the command to invoke our launcher
set $menu alacritty --class launsh -e launsh

# ... keybinds

# start the launcher when $mod+d is pressed
bindsym $mod+d exec $menu

# ... window rules

# make sure launsh runs in a floating window
for_window [app_id="launsh"] floating enable
```

### Using anything else

If you're not using sway, make sure to change the command inside the `run` function at the start of `launsh`, which is configured to use `swaymsg exec` by default.

