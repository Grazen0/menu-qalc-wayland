# menu-qalc
A calculator for Rofi/dmenu(2)

[Screencast](https://gfycat.com/SociableDopeyHerald)

## Installation
Arch Linux AUR: [menu-qalc](https://aur.archlinux.org/packages/menu-qalc/)

## Dependencies
- [libqalculate](https://archlinux.org/packages/extra/x86_64/libqalculate/)
- [wl-clipboard](https://github.com/bugaevc/wl-clipboard)
- [Wofi](https://archlinux.org/packages/extra/x86_64/wofi/), [fuzzel](https://archlinux.org/packages/extra/x86_64/fuzzel/) or
  dmenu[(2)](https://aur.archlinux.org/packages/dmenu2/)

## Usage
`menu-qalc` uses `qalc` as the backend and will accept any operations `qalc` is able to do:

    = 4+4
    = (4+2)/(4+3)
    = 4^2
    = sqrt(4)
    = c(2)
    = '500 + 25%'
    = '1000 EUR to USD'

The answer can be copied to the clipboard and used for further calculations
inside (or outside) Rofi/dmenu.

If launched outside of Rofi/dmenu the expression may need quotation marks.

## Custom Usage
To launch directly into the calculator, use the following command (useful if
bound to "super + equal" in [sxhkd](https://github.com/baskerville/sxhkd),
[i3](https://i3wm.org/) or the like):

    = -- [rofi/dmenu parameters]

For example:

    = -- -location 2 -width 100

### Force usage of `dmenu`
By default, if `wofi` or `fuzzel` is installed, it will be used. You can force `menu-qalc`
to use `dmenu` or any other `dmenu`-like application:

    = --dmenu=dmenu
