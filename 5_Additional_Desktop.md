

## sddm theme

> sudo git clone https://github.com/keyitdev/sddm-astronaut-theme.git /usr/share/sddm/themes/sddm-astronaut-theme

> sudo cp /usr/share/sddm/themes/sddm-astronaut-theme/Fonts/* /usr/share/fonts/

> sudo nano /etc/sddm.conf

    [Theme]
    Current=sddm-astronaut-theme

to change login background add image to

    /usr/share/sddm/themes/sddm-astronaut-theme/

and edit

    /usr/share/sddm/themes/sddm-astronaut-theme/theme.conf


## wallpapers

> paru -S swww

> swww-daemon (or reboot and hyprland config will start swww)

set image:

> swww img path/to/img

reboot or

> sudo systemctl enable swww-daemon.service

## wlogout

> paru -S wlogout

> cp -r ~/Downlaods/arch-hyprdots/.Config/wlogout ~/.Config/wlogout

## swaylock

> sudo apcman -S swaylock

> cp -r ~/Downlaods/arch-hyprdots/.Config/swaylock ~/.Config/swaylock


## dunst

> sudo pacman -S dunst

> cp -r ~/Downlaods/arch-hyprdots/.Config/dunst ~/.Config/dunst

## rofi

> paru -S rofi-lbonn-wayland-git

> cp -r ~/Downlaods/arch-hyprdots/.Config/rofi ~/.Config/rofi
