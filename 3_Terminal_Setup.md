# fonts

> sudo pacman -S otf-font-awesome ttf-firacode-nerd ttf-cascadia-code ttf-cascadia-code-nerd ttf-jetbrains-mono-nerd ttf-nerd-fonts-symbols

# fish shell

> sudo pacman -S fish

> fish

> chsh -s (which fish)

> echo 'set -g fish_greeting' >> ~/.config/fish/config.fish

# kitty

download kitty config 

> curl -o ~/.config/kitty/kitty.conf https://raw.githubusercontent.com/mvrshmvllxw/arch-hyprland-manual-install/main/.config/kitty/kitty.conf

download and set theme (from fish!)

> set THEMENAME Hardcore

(to choose another theme change 'Hardcore')

> set THEME https://raw.githubusercontent.com/dexpota/kitty-themes/master/themes/$THEMENAME.conf && wget "$THEME" -P ~/.config/kitty/kitty-themes/ && ln -sf ~/.config/kitty/kitty-themes/$THEMENAME.conf ~/.config/kitty/theme.conf

# lsd

> sudo pacman -S lsd

> echo "alias ls 'lsd'" >> ~/.config/fish/config.fish

> exec fish

# starship

> sudo pacman -S starship

> curl -o ~/.config/starship.toml https://raw.githubusercontent.com/mvrshmvllxw/arch-hyprland-manual-install/main/.config/starship.toml

> echo 'starship init fish | source' >> ~/.config/fish/config.fish


