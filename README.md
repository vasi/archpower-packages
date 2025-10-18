# ArchPOWER packages

Additional packages for [ArchPOWER](https://archlinuxpower.org/) that I find useful.

These are mostly quick ports from the [Arch build system](https://wiki.archlinux.org/title/Arch_build_system) and [Arch User Repository](https://wiki.archlinux.org/title/Arch_User_Repository). They complement packages in the [main repo](https://github.com/kth5/archpower) and [TechFlash's extras repo](https://github.com/techflashYT/archpower-extra-pkgs).

## Packages

A non-exhaustive list:

* [bear](bear) to generate compile_commands.json
* [libffi7](libffi7) to allow running [recent builds of PowerPC browsers](https://github.com/chzigotzky/Web-Browsers-and-Suites-for-Linux-PPC/releases)
* [KOffice](tde-office), an office suite from the [Trinity Desktop](https://www.trinitydesktop.org/)
* [mouseemu](mouseemu) to emulate middle/right button clicks on laptops with a single trackpad button
* [ncdu](ncdu) to explore directory space usage
* [neovim](neovim), a fast CLI editor
* [Ted](ted), a word processor
* [docklike-plugin](xfce4-docklike-plugin), a panel applet for XFCE to allow dock-like semantics (mixed launchers and tasks)
* Some tools for smaller window managers:
  * [archlinux-xdg-menu](archlinux-xdg-menu) to create menus for many WMs
  * [dunst](dunst) for notifications in minimal window managers
  * [skippy-xd](skippy-xd-git) for [Exposé](https://en.wikipedia.org/wiki/Mission_Control_(macOS))-like window switching
  * [tint2](tint2), a dock
  * [YAD](yad-gtk2) for UI scripting

Build I've found less-useful personally, but still thought are worth saving, are in the [experimental](experimental) directory:

* Geany, a nice GUI text editor that runs far too slowly
* dte, a CLI text editor I find hard to use
* Kakoune, a CLI text editor that's quite usable, but not quite as nice as neovim
* MATE, a entire desktop, a fork of Gnome 2
* pbbuttonsd, which used to be critical for handling power management and special buttons on PowerPC laptops, but hasn't been maintained foryears
* plank, another dock
* tilde, a CLI editor whose theme I find too bright

## Caveats

* This isn't even close to a coherent set of packages, just ones that I'm interested in right now
* I make no commitment to update these in the future
* These are just PKGBUILDs, no binaries are made publicly available
* I've only tested these on 32-bit PowerPC

## Usage

To use these, just build with `makepkg` as usual. I strongly suggest building on a ppc64 VM (or modern hardware), and setting up [icecream](https://github.com/icecc/icecream) to distribute builds to a faster box. Some builds depend on others in the repo, you'll find out when makepkg complains about missing dependencies—I don't provide any tool for recursive builds, or building the whole repo in the right order.

## Licensing

Licensed under the [Zero-clause BSD license](LICENSE).
