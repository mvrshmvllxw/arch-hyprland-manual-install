# necessary software

> sudo pacman -S gnome-text-editor nautilus firefox network-manager-applet telegram-desktop 

# system soft

> paru -S pipewire-alsa pipewire-pulse gst-plugin-pipewire pavucontrol pamixer network-manager-applet bluez bluez-utils blueman brightnessctl udiskie xdg-desktop-portal-gtk

# waybar

download the entire repository to install the configs

> cd ~/Downloads

> git clone https://github.com/mvrshmvllxw/arch-hyprdots.git

copy waybar configs

> cp -r ~/Downlaods/arch-hyprdots/.Config/waybar ~/.Config/waybar

install waybar

> pacman -S waybar

if you need edit configs use

> gnome-text-editor ~/.config/waybar/config 

> gnome-text-editor ~/.config/waybar/style.css

> gnome-text-editor ~/.config/waybar/theme.css


# install gnome apps theme

> paru -S nwg-shell

now you can use gui `nwg-look` to check or change gtk theme

cp folders:

> cp -r ~/Downlaods/arch-hyprdots/.Config/gtk-3.0 ~/.Config/gtk-3.0

> cp -r ~/Downlaods/arch-hyprdots/.Config/gtk-4.0 ~/.Config/gtk-4.0

> cp -r ~/Downlaods/arch-hyprdots/.Config/nwg-look ~/.Config/nwg-look

> cp -r ~/Downlaods/arch-hyprdots/.themes ~/.themes

to apply theme from terminal (or use `nwg-look`)

> gsettings set org.gnome.desktop.interface gtk-theme 'Rose-Pine'

if you need to turn on gnome dark scheme 

> gsettings set org.gnome.desktop.interface color-scheme 'prefer-dark'


# install kde apps theme

install utils to change theme

> sudo pacman -S qt5ct qt6ct kvantum qt5-wayland qt6-wayland kvantum-qt5 kconfig kde-cli-tools qt5-tools

now you can use `kvantummanager` and `qt6ct` for gui theming (use qt6ct if icons didn't set)

set kde theme to Kvantum

> kwriteconfig6 --file kdeglobals --group KDE --key widgetStyle kvantum-dark

> kwriteconfig6 --file kdeglobals --group General --key ColorScheme Kvantum

copy kvantum theme and qt6ct settings

> cp -r ~/Downlaods/arch-hyprdots/.Config/Kvantum ~/.Config/Kvantum

> cp -r ~/Downlaods/arch-hyprdots/.Config/qt6ct ~/.Config/qt6ct


# icons

install icons

> paru -S tela-circle-icon-theme-all

apply for kde apps

> kwriteconfig6 --file ~/.config/kdeglobals --group Icons --key Theme 'Tela-circle-pink'

apply for gnome apps

> gsettings set org.gnome.desktop.interface icon-theme 'Tela-circle-pink'

! instead of 'Tela-circle-pink' you can specify any other color from this package

# cursor

> paru -S bibata-cursor-theme

apply for kde

> kwriteconfig6 --file ~/.config/kcminputrc --group Mouse --key cursorTheme Bibata-Original-Ice

apply for gnome

> gsettings set org.gnome.desktop.interface cursor-theme 'Bibata-Original-Ice'

apply for hyprland

>hyprctl setcursor Bibata-Original-Ice 24

apply to..? (just need)

> sudo nano /usr/share/icons/default/index.theme 

    [Icon Theme]
    Inherits=Bibata-Original-Ice

apply to sddm 

> sudo nano /etc/sddm.conf

add

    [Theme]
    CursorSize=24
    CursorTheme=Bibata-Original-Ice

if any bugs try:

    copy folder from /usr/share/icons/Bibata-Original-Ice

    to ~/.local/share/icons and  ~/.icons

or install

    plasma-desktop gnome


