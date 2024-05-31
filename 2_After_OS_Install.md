# wi-fi

use win+q to open kitty (terminal)

win+c to close window

write `ls` or just press `Enter` in kitty if a warning bothers you

connect to wi-fi

```bash
nmcli dev wifi
# replace SID_NAME and WIFI_PASSWORD
nmcli dev wifi connect SSID_NAME password WIFI_PASSWORD
# check status
nmcli dev status
# for disconnect
nmcli dev disconnect wlan0
# if got any errors try
sudo systemctl restart NetworkManager
```
# enable bluetooth

> sudo systemctl enable bluetooth.service 

> sudo systemctl restart bluetooth.service

# hyprconf 

download and set the hyprland config

> curl -o ~/.config/hypr/hyprland.conf https://raw.githubusercontent.com/mvrshmvllxw/arch-hyprdots/main/.config/hypr/hyprland.conf

use nano to edit it 

> nano ~/.config/hypr/hyprland.conf

first of all, edit the settings for the monitor, window control keys and application launch key

default: 

    win+q - close, win+w - fullscreen,
    win+z - terminal (kitty), win+s - nautilus, win+f - firefox,
    win+1,+2,+3 - change desktop,
    win+right_mouse - change window size
    capslock - switch keyboard layout

# pacman keys

> gpg --refresh-keys

> sudo pacman-key --init

> sudo pacman-key --populate archlinux

> sudo pacman -Sy archlinux-keyring

> sudo pacman -Su

# pacman

> sudo nano /etc/pacman.conf

check or uncomment:

    Color
    VerbosePkgLists
    ParallelDownloads = 5

add:

    ILoveCandy

# mirrors

> sudo pacman -S reflector

> sudo reflector --verbose --latest 15 --sort rate --save /etc/pacman.d/mirrorlist

> sudo pacman -Sy

> sudo pacman -Su


# user dirs

> sudo pacman -S xdg-user-dirs

> xdg-user-dirs-update

# git 

> sudo pacman -S --needed base-devel git

# paru (for aur packages)

> cd ~/Downloads

> git clone https://aur.archlinux.org/paru.git

> cd paru

> makepkg -si

# chaotic aur

> sudo pacman-key --recv-key 3056513887B78AEB --keyserver keyserver.ubuntu.com

> sudo pacman-key --lsign-key 3056513887B78AEB

> sudo pacman -U 'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-keyring.pkg.tar.zst'

> sudo pacman -U 'https://cdn-mirror.chaotic.cx/chaotic-aur/chaotic-mirrorlist.pkg.tar.zst'

> sudo pacman -Sy

# flatpak (optional)

> sudo pacman -S flatpak

# snapcraft (optional)

> cd ~/Downloads/

> git clone https://aur.archlinux.org/snapd.git

> cd snapd

> makepkg -si

> sudo systemctl enable --now snapd.socket

> sudo pacman -S apparmor

> systemctl start apparmor.service

> sudo systemctl enable --now snapd.apparmor.service