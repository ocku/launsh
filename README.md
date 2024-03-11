# Launsh

A minimal, terminal-based alternative to dmenu_path + {dmenu, rofi, wmenu, ...etc}.

![image](https://github.com/ocku/launsh/assets/147977941/4b68798e-21c4-4ca0-bb77-3213914ffdcd)

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

If you're using Sway and Alacritty, add the following to your Sway config. 

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

If you're not using Sway, make sure to change the `run` function at the start of `launsh`, which is set to use `swaymsg exec` by default.

