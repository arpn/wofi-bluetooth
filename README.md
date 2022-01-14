# wofi-bluetooth

Essentially the same as [rofi-bluetooth](https://github.com/nickclyde/rofi-bluetooth) except for [wofi](https://hg.sr.ht/~scoopta/wofi).

## Dependencies:

1. [wofi](https://hg.sr.ht/~scoopta/wofi) (`community/wofi` in Arch Linux)
2. bluetoothctl (from `extra/bluez-utils` in Arch Linux)

## Usage

Clone, `cd wofi-bluetooth` and run `./wofi-bluetooth`. It might be convenient to add the script to your `$PATH`.

### Waybar configuration

`NOTE:` In order to properly display the bluetooth icon, you will need to use an iconic font in your bar, e.g. [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts).

Add this to your [waybar](https://github.com/Alexays/Waybar) config
```
"bluetooth": {
    "format": "{icon}",
    "format-icons": {
        "enabled": "",
        "disabled": ""
    },
    "on-click": "wofi-bluetooth"
}
```
and then add `bluetooth` to your modules in that same config file.

`NOTE:` You have to specify the full path to `wofi-bluetooth` if you didn't add it to your `$PATH`.

