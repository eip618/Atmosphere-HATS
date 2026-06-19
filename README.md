
![Banner](img/banner.png?raw=true)
=====

### Support __My__ Work

If you find __my__ project useful, please consider supporting me by buying me a coffee! I work tirelessly on Atmosphere to bring YOU such useful changes as:
- 2 label changes
- ???

<a href="https://www.buymeacoffee.com/sthetixofficial" target="_blank">
  <img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" >
</a>

![License](https://img.shields.io/badge/License-GPLv2-blue.svg)
[![Chat on Discord](https://img.shields.io/badge/Discord-5865f2?logo=discord&logoColor=white)](https://discordapp.com/invite/ZdqEhed)
![Made with Notepad++](img/np++.png?raw=true)

Atmosphere-HATS is an unofficial fork of Atmosphère. It is not the official Atmosphère repository and is not affiliated with or endorsed by the upstream Atmosphère project.

This fork currently carries small UX-focused changes, including changing the System Settings eMMC indicator from the upstream `S` / `E` labels to clearer `SYS` / `EMU` labels.

Atmosphère is a work-in-progress customized firmware for the Nintendo Switch.

Components
=====

Atmosphère consists of multiple components, each of which replaces/modifies a different component of the system:

* Fusée: First-stage Loader, responsible for loading and validating stage 2 (custom TrustZone) plus package2 (Kernel/FIRM sysmodules), and patching them as needed. This replaces all functionality normally in Package1loader/NX Bootloader.
* Exosphère: Customized TrustZone, to run a customized Secure Monitor
* Thermosphère: EL2 EmuNAND support, i.e. backing up and using virtualized/redirected NAND images
* Stratosphère: Custom Sysmodule(s), both Rosalina style to extend the kernel/provide new features, and of the loader reimplementation style to hook important system actions
* Troposphère: Application-level Horizon OS patches, used to implement desirable CFW features

Licensing
=====

This software is licensed under the terms of the GPLv2, with exemptions for specific projects noted below.

You can find a copy of the license in the [LICENSE file](LICENSE).

Exemptions:
* [Nintendo](https://github.com/Nintendo) is exempt from GPLv2 licensing and may (at its option) instead license any source code authored for the Atmosphère project under the Zero-Clause BSD license.

Credits
=====

Atmosphère is currently being developed and maintained by __sthetix__.<br>
In no particular order, we credit the following for their invaluable contributions:

* __sthetix__ for his groundbreaking UX/UI changes
* __switchbrew__ for the [libnx](https://github.com/switchbrew/libnx) project and the extensive [documentation, research and tool development](http://switchbrew.org) pertaining to the Nintendo Switch.
* __devkitPro__ for the [devkitA64](https://devkitpro.org/) toolchain and libnx support.
* __ReSwitched Team__ for additional [documentation, research and tool development](https://reswitched.github.io/) pertaining to the Nintendo Switch.
* __ChaN__ for the [FatFs](http://elm-chan.org/fsw/ff/00index_e.html) module.
* __Marcus Geelnard__ for the [bcl-1.2.0](https://sourceforge.net/projects/bcl/files/bcl/bcl-1.2.0) library.
* __naehrwert__ and __st4rk__ for the original [hekate](https://github.com/nwert/hekate) project and its hwinit code base.
* __CTCaer__ for the continued [hekate](https://github.com/CTCaer/hekate) project's fork and the [minerva_tc](https://github.com/CTCaer/minerva_tc) project.
* __m4xw__ for development of the [emuMMC](https://github.com/m4xw/emummc) project.
* __Riley__ for suggesting "Atmosphere" as a Horizon OS reimplementation+customization project name.
* __hedgeberg__ for research and hardware testing.
* __lioncash__ for code cleanup and general improvements.
* __jaames__ for designing and providing Atmosphère's graphical resources.
* Everyone who submitted entries for Atmosphère's [splash design contest](https://github.com/Atmosphere-NX/Atmosphere-splashes).
* _All those who actively contribute to the Atmosphère repository._
