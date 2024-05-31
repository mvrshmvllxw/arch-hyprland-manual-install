# VSCode

> paru -S code code-features code-marketplace 

> cp -r ~/Downlaods/arch-hyprdots/.Config/code ~/.Config/code

# another

> paru -S vim neovim fastfetch btop htop cava ranger ktorrent kget ark spectacle

# ONLY IF NEED

paru -S --needed pipewire pipewire-alsa pipewire-audio pipewire-jack pipewire-pulse gst-plugin-pipewire wireplumber pavucontrol pamixer networkmanager network-manager-applet bluez bluez-utils blueman brightnessctl udiskie

paru -S --needed  polkit-gnome xdg-desktop-portal-hyprland pacman-contrib python-pyamdgpuinfo parallel jq imagemagick qt5-imageformats ffmpegthumbs kde-cli-tools kservice5 libnotify

paru -S --needed  hyprland dunst rofi-lbonn-wayland-git waybar swww swaylock-effects-git wlogout grimblast-git hyprpicker slurp swappy cliphist

paru -S --skipreview --needed firefox kitty dolphin ark vim neofetch fastfetch btop htop cava ranger neovim ktorrent kget ark octopi okular kate gwenview kimageformats elisa mpv spectacle kompare pace kcalc snapper-tools reflector-simple timeshift pokemon-colorscripts-git imv nautilus

paru -S telegram-desktop steam obs-studio

# kernel

linux zen

    sudo pacman -S linux-zen linux-zen-headers

systemd-boot:

    ls /efi/loader/entries

add *zen.conf to default kernel (c41197fa2992e6*zen.conf)

    su root

    kwrite /efi/loader/loader.conf


# if nvidia dkms need

    paru -S --skipreview inux-zen-headers nvidia-dkms nvidia-utils

vulkan-intel for intel, nvidia utils for nvidia or vulkan radeon for radeon


# firefox

install theme & addblock

https://addons.mozilla.org/en-US/firefox/addon/hatsune-miku-dancing-animated/

https://addons.mozilla.org/en-US/firefox/addon/adblocker-ultimate/

enable customization

Type `about:config` in URL Bar and set to enable css themes:

    toolkit.legacyUserProfileCustomizations.stylesheets > true 

delete window control buttons

> about:support

open profile direcory (click button) and create file `/chrome/userChrome.css`

add

> .titlebar-buttonbox-container{ display:none } 


# additional packages (ONLY IF NEED)

paru -S otf-noto-sans-cjk ttf-maple ttf-material-design-iconic-font ttf-mononoki-nerd

paru -S flameshot retroarch mangohud lutris piper dosbox goverlay easyeffects openrgb bottles gamemode lib32-gamemode minigalaxy portproton heroic-games-launcher-bin protonup-qt protonup-ng-git steam-rom-manager-bin discover-overlay gpu-screen-recorder-git replay-sorcery antimicrox qjoypad noisetorch

paru -S ccache zram-generator dbus-broker-units rqbalance corectrl displaycal modem-manager-gui nohang ananicy-cpp uksmd libinput-gestures fancontrol-gui emote trash-cli-git downgrade gamescope


# telegram theme

telegram https://t.me/addtheme/Hyprgram

# hyprland default scale

gtk env = GDK_SCALE,1.2
env = XCURSOR_SIZE,32
env = QT_SCALE_FACTOR,1.2

relogin 

run apps:
QT_SCALE_FACTOR=1.2 virtualbox
GDK_SCALE=1.2 steam

links in `/usr/share/applications/` change to

`Exec=env GDK_SCALE=1.2 /usr/bin/steam-runtime %U
vulkan`


