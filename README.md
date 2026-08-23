
## Waybar config

My config is almost a copy-paste of the [mechabar](https://github.com/Sejjy/MechaBar) repository, make sure to check it if you are encounetering any issues !\
It also is a lot more neutral, and has more stuff right of the bat, with more explanations as well.

# Preview 
| ![Preview](./assets/noobarch.png) |
| :---------------------------------------: |

### Requirements

The only difference with the original regarding this part is that I swapped all occurences of kitty with Ghostty, [as per the original README explained](#configuration).

### Installation
(Section taken from the original README)

1. Back up your current Waybar configuration:

	```bash
	mv ~/.config/waybar{,.bak}
	```

2. Clone the repository:

	```bash
	git clone https://github.com/NoobArch/Waybar.git ~/.config/waybar
	```

3. Install the dependencies and restart Waybar:

	```bash
	~/.config/waybar/install
	```

	<details>
	<summary>Dependencies (7)</summary>

	| Package                 | Command         | Description                                                                    |
	| ----------------------  | --------------- | ------------------------------------------------------------------------------ |
	| `bluez-utils`           | `bluetoothctl`  | Development and debugging utilities for the bluetooth protocol stack<tr></tr>  |
	| `brightnessctl`         | `brightnessctl` | Lightweight brightness control tool<tr></tr>                                   |
	| `fzf`                   | `fzf`           | Command-line fuzzy finder<tr></tr>                                             |
	| `libnotify`             | `notify-send`   | Library for sending desktop notifications<tr></tr>                             |
	| `networkmanager`        | `nmcli`         | Network connection manager and user applications<tr></tr>                      |
	| `pacman-contrib`        | `checkupdates`  | Contributed scripts and tools for pacman systems                               |

    Optional:

	| Package                | Description                                                                    |
	| ---------------------- | ------------------------------------------------------------------------------ |
	| `otf-commit-mono-nerd` | Patched font Commit Mono from nerd fonts library                               |

	> If you prefer a different font, see the [Configuration](#configuration) section below.

	</details>

#

### Configuration
(Section taken from the original README)

<details>
<summary>Terminal</summary>

If you use a different terminal emulator, replace every instance of `kitty` in the module files.
For example:

```jsonc
// ~/.config/waybar/modules/custom/power.jsonc

"custom/power": {
	// "on-click": "kitty -e ~/.config/waybar/scripts/power",
	"on-click": "ghostty -e ~/.config/waybar/scripts/power",
}
```

#

</details>

<details>
<summary>Fonts</summary>

Different fonts render characters in different sizes, which can affect the layout.
Import your preferred font file from the [fonts](./styles/fonts/) directory to `style.css`.
For example:

```css
/* @import "styles/fonts/commit-mono.css"; */
@import "styles/fonts/jetbrains-mono.css";
```

#

</details>

<details>
<summary>Themes</summary>

To change the theme, import your preferred theme file from the [themes](./styles/themes/) directory to `style.css`.
For example:

```css
/* @import "styles/themes/catppuccin-mocha.css"; */
@import "styles/themes/catppuccin-latte.css";
```

#

</details>

<details>
<summary>Icons</summary>

You can search for icons on [Nerd Fonts: Cheat Sheet ↗](https://www.nerdfonts.com/cheat-sheet).
For example:

```
gentoo
```

_Matches: `nf-dev-gentoo`, `nf-linux-gentoo`, `nf-md-gentoo`*_

_*Most modules use Material Design Icons (`nf-md-*`) for consistency._

#

</details>

<details>
<summary>Custom module</summary>

The leftmost module has no default function and is left for you to configure.
For example:

```jsonc
// ~/.config/waybar/modules/custom/user.jsonc

"custom/user": {
	"on-click": "/path/to/your/script", // Run your own script
	"on-click-right": "pkill -SIGUSR2 waybar", // Restart Waybar
}
```

</details>

> [!WARNING]
> The temperature module required me to tweak the thermal-zone, the default is one, try switching it back if it doesn't show up

#

### References
(Section taken from the original README)

- [Waybar wiki](https://github.com/Alexays/Waybar/wiki)
- [Nerd Fonts wiki: Glyph Sets](https://github.com/ryanoasis/nerd-fonts/wiki/Glyph-Sets-and-Code-Points)
