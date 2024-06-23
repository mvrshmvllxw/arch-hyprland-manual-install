# sddm theme

> sudo git clone https://github.com/keyitdev/sddm-astronaut-theme.git /usr/share/sddm/themes/sddm-astronaut-theme

> sudo cp /usr/share/sddm/themes/sddm-astronaut-theme/Fonts/* /usr/share/fonts/

> sudo nano /etc/sddm.conf

    [Theme]
    Current=sddm-astronaut-theme

to change login background add image to

    /usr/share/sddm/themes/sddm-astronaut-theme/

and edit

    /usr/share/sddm/themes/sddm-astronaut-theme/theme.conf

# wallpapers

> paru -S swww

> swww-daemon (or reboot and hyprland config will start swww)

reboot or

> sudo systemctl enable swww-daemon.service

set image:

> swww img path/to/img

# wlogout

> paru -S wlogout

`~/.config/wlogout`

# swaylock

> sudo apcman -S swaylock

`~/.config/swaylock`

# dunst of swaync

> sudo pacman -S dunst

`~/.Config/dunst`

> sudo pacman -S swaync

`~/.config/swaync`

# rofi

> paru -S rofi-lbonn-wayland-git

`~/.config/rofi`

# link

wlogout rofi swaync swaylock theme

install from https://github.com/zDyanTB/HyprNova