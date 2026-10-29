
## Desktop environments

|Desktop environment|General style|Pros|Cons|
|---|---|---|---|
|KDE Plasma|Feature-rich and highly customizable|Many settings and visual options; familiar desktop layout; broad application suite|Lots of options can feel overwhelming|
|GNOME|Clean, streamlined, keyboard-friendly|Consistent design; simple default experience; strong accessibility support|Customization often relies on extensions; workflow may feel unfamiliar|
|Xfce|Traditional and lightweight|Fast, stable, and modest on resources; easy to customize|Default appearance can feel dated|
|Cinnamon|Traditional desktop, popular with Linux Mint|Familiar layout; approachable settings; good balance of features and simplicity|Less lightweight and flexible than some alternatives|
|MATE|Classic, traditional desktop|Simple, dependable, and relatively lightweight|Fewer modern features and visual effects|
|LXQt|Minimal and lightweight|Good for older or low-resource computers|Fewer integrated tools and less polish than larger DEs|
|Budgie|Modern and straightforward|Attractive default layout; relatively easy to use|Smaller ecosystem and fewer customization options than KDE or GNOME|

## Window managers

|Window manager|Style|Pros|Cons|
|---|---|---|---|
|i3|Tiling|Keyboard-driven; predictable layout; well documented|Requires configuration; may feel unfamiliar at first|
|Sway|Tiling, Wayland-based|i3-like workflow with Wayland support|Some programs or workflows may need adjustments|
|bspwm|Tiling|Scriptable and flexible|Requires more manual setup|
|Hyprland|Tiling, Wayland-based|Modern effects and extensive customization|Configuration can be involved; updates may require maintenance|
|Openbox|Floating|Lightweight; windows can be moved and resized freely|A standalone setup needs panels, menus, and other components|
|Fluxbox|Floating|Lightweight and simple|Less integrated and less actively developed than many modern options|
|AwesomeWM|Tiling and floating|Highly configurable through Lua|Requires comfort with configuration and scripting|

## Quick guide

- Want an easy, complete desktop? Try KDE Plasma, GNOME, Cinnamon, or Xfce.
- Want a lightweight desktop? Try Xfce, MATE, or LXQt.
- Want windows arranged automatically and keyboard-driven? Try i3, Sway, or Hyprland.
- Want to build a custom desktop from components? Try a standalone window manager such as Openbox or bspwm.

A desktop environment already includes a window manager, so most people choose either a DE or a standalone WM setup. You can install more than one and select one when logging in.

there are more obscure one that is used by tinkerer or advanced user

| Name                              | Type                                      | What makes it distinctive                                          | Pros                                                                     | Cons                                                            |
| --------------------------------- | ----------------------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------ | --------------------------------------------------------------- |
| Enlightenment (E)                 | Desktop environment / window manager      | Highly themed desktop with its own visual style and tools          | Lightweight for its feature set; lots of visual customization            | Unusual settings and workflow can take time to learn            |
| Moksha                            | Desktop environment                       | Bodhi Linux’s desktop, descended from Enlightenment                | Lightweight; familiar panels and menus; distinctive look                 | Smaller ecosystem; fewer guides and packages than major DEs     |
| Trinity Desktop Environment (TDE) | Desktop environment                       | Continues the classic KDE 3 desktop design                         | Traditional layout; relatively modest system requirements                | Older-style design; smaller community and application ecosystem |
| UKUI                              | Desktop environment                       | A traditional desktop developed for the Ubuntu Kylin ecosystem     | Familiar layout; integrates its own desktop utilities                    | Less widely used outside its target ecosystem                   |
| ROX Desktop                       | Desktop environment / collection of tools | A modular desktop built around the ROX-Filer file manager          | Lightweight; components can be used independently                        | Not as integrated or actively prominent as mainstream desktops  |
| LXDE                              | Desktop environment                       | Older, lightweight desktop based on GTK                            | Fast and simple on modest hardware                                       | Much of its development has shifted toward LXQt                 |
| Regolith                          | Desktop environment / configured i3 setup | Combines a tiling workflow with a ready-made desktop configuration | Easier starting point than assembling a tiling setup yourself            | More opinionated; closely tied to its chosen components         |
| Qtile                             | Tiling window manager                     | Its configuration is written in Python                             | Programmable; flexible layouts and widgets                               | Requires comfort with configuration and Python                  |
| Xmonad                            | Tiling window manager                     | Configured and extended using Haskell                              | Powerful, predictable, and highly customizable                           | Haskell creates a steep learning curve                          |
| dwm                               | Dynamic tiling window manager             | Configuration is changed in C and compiled                         | Very small and fast; behavior can be customized extensively              | Changes require editing and compiling source code               |
| herbstluftwm                      | Manual tiling window manager              | Uses a tree of frames that can be split and rearranged             | Flexible manual layouts; commands are scriptable                         | Minimal out of the box; setup takes work                        |
| spectrwm                          | Tiling window manager                     | A compact, keyboard-driven design inspired by minimal WMs          | Lightweight; straightforward configuration                               | Small feature set and community                                 |
| Niri                              | Wayland compositor                        | Places windows in horizontally scrolling columns                   | Distinctive workflow; windows don’t have to be squeezed into fixed tiles | Different from conventional desktops; Wayland-only              |
| Wayfire                           | Wayland compositor                        | Offers a plugin-based desktop with visual effects                  | Customizable; can provide a composited desktop feel                      | Plugin and configuration choices can add setup complexity       |
| labwc                             | Wayland compositor                        | A lightweight, stacking compositor inspired by Openbox             | Familiar floating-window workflow; minimal design                        | You may need to add panels, launchers, and other desktop tools  |

Quick distinction: A desktop environment like Enlightenment or Trinity comes with a broader set of desktop tools. A window manager or compositor like dwm, Niri, or labwc mainly handles windows, so you may need to assemble the rest of the desktop yourself. The exact line can blur for projects that include extra utilities.

quick note that computer can be used with or without an DE or WM
it can be used through a TUI more commonly called an Terminal