# dwm-Windows-11
dwm themed like Windows 11 or something.

# Installation

## Font Installation
1. Run "`sudo -i`"
2. Run "`cp /path/to/DejaVuSansMono.zip /usr/share/fonts`"
3. cd to "`/usr/share/fonts`"
4. I recommend making a folder so you can tell between normal Deja Vu Sans Mono and Deja Vu Sans Mono Nerd Font. So run "`mkdir DejaVuSansMonoNerd`" or whatever you want to call the folder
5. You are done

## dwm Installation
1. cd to "`dwm-6.3`"
2. Change keybinds in "`config.h`" if desired (default ModKey is Mod4Key or Super/Windows button)
3. Run "`sudo make install`"
4. add "`exec dwm`" to your ~/.xinitrc

### dwm Installation Notes
You can install dwm without root. Just run "`make`" and then do the path to the "`dwm`" executable in your "`~/.xinitrc`" Example:\
"`exec ~/.suckless/dwm-6.3/dwm`"

### Keybinds
|Action         | Result        |
|---------------|---------------|
|`Win + Return` | Open Terminal |
|`Win + C`      | Kill          |
|`Win + D`      | Open dmenu    |

## dmenu Installation
1. cd to "`dmenu-5.1`"
2. Edit "`config.h`" if desired
3. Run "`sudo make install`"

### dmenu Installation Notes
If you edited dwm's:
````
static const char *fonts[]          = { "DejaVuSansMono Nerd Font:style=Book:size=11" };
static const char dmenufont[]       = "DejaVuSansMono Nerd Font:style=Book:size=11";
````
or
````
static const unsigned int borderpx  = 1;        /* border pixel of windows */
````
You may want to read the top of "`dmenu-5.1/patches/dmenu-bottomleft-4.8.diff`" file as you may want to re-patch dmenu.

# Status Bar
I am not including a status bar program due to the fact that everyone's hardware is different. If you want a status bar program I would recommend dwmblocks. My setup for dwmblocks in @ github (https://github.com/XxVaD3r/dwmblocks-ux31a). If you use an ASUS UX31A laptop then all of those scripts should work.
