# NoobArch Waybar config

My config is an amalgamation of several repos (ordered) : [anonymous-red/waybar](https://github.com/sansroot/hypr-dots/tree/anonymous-red/waybar), [mechabar](https://github.com/Sejjy/MechaBar), and [waybar-pomodoro-timer](https://github.com/niraletter/waybar-pomodoro-timer). Make sure to check them out !\

# Preview 
| ![Preview](./assets/noobarch_waybar.png) |
| :---------------------------------------: |

## Installation

1. Back up your current Waybar configuration:

	```bash
	mv ~/.config/waybar{,.bak}
	```

2. Clone the repository:

	```bash
	git clone https://github.com/NoobArch/Waybar.git ~/.config/waybar
	```

3. Dependencies : 
	<details>
	<summary>Dependencies (6)</summary>

	| Package                 | Command         | Description                                                                    |
	| ----------------------  | --------------- | ------------------------------------------------------------------------------ |
	| `bluez-utils`           | `bluetoothctl`  | Development and debugging utilities for the bluetooth protocol stack<tr></tr>  |
	| `brightnessctl`         | `brightnessctl` | Lightweight brightness control tool<tr></tr>                                   |
	| `fzf`                   | `fzf`           | Command-line fuzzy finder<tr></tr>                                             |
	| `libnotify`             | `notify-send`   | Library for sending desktop notifications<tr></tr>                             |
	| `networkmanager`        | `nmcli`         | Network connection manager and user applications<tr></tr>                      |
	| `pacman-contrib`        | `checkupdates`  | Contributed scripts and tools for pacman systems                               |

	</details>

## Credits 
I took the general aspect of [anonymous-red/waybar](https://github.com/sansroot/hypr-dots/tree/anonymous-red/waybar), changed it's colors to match my config, swapped the places of some modules, added the networkmodule, and made some other minor CSS tweaks. \
Then added the bluetooth, pulseaudio, backlight and temperature of [mechabar](https://github.com/Sejjy/MechaBar).
Finally, added the [waybar-pomodoro-timer](https://github.com/niraletter/waybar-pomodoro-timer).
