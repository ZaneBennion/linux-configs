# linux-configs

Distro: Omarchy
Theme: [Monochrome](https://github.com/Swarnim114/omarchy-monochrome-theme)
Background: [Light Orb](https://github.com/euandeas/omarchy-flexoki-light-theme/blob/main/backgrounds/flexoki-light-orb.png)

## Keyd

Used for making capslock act as esc when pressed and ctrl when held

1. Install keyd with package manager
2. Start keyd `sudo systemctl enable keyd --now`
3. Put config file in `/etc/keyd/default.conf`
4. Reload the config with `sudo keyd reload`

Put the following in `/etc/libinput/local-overrides.quirks`

```
[Serial Keyboards]

MatchUdevType=keyboard
MatchName=keyd*keyboard
AttrKeyboardIntegration=internal
```

## Tmux

1. clone repo

```
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

2. Put config file in home directory
3. Make sure you do `<leader> I` to insure tpm installs plugins
