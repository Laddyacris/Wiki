# Advanced Arcade on Recalbox

This page is the follow-up to [Easy Arcade on Recalbox](./)

## BestArcade4Recalbox

You can find here a list of the most important mame games and their working status on mame and fba\_libretro : [BestArcade4Recalbox](https://docs.google.com/spreadsheets/d/1F5tBguhRxpj1AQcnDWF6AVSx4av_Gm3cDQedQB7IECk/edit#gid=131171669&vpid=A179)

## ClrMamePro

In order to verify the roms your have, you can use clrmamepro, and use the [clrmamepro tutorial](https://github.com/recalbox/recalbox-os/wiki/Check-your-roms-version-with-clrmamepro-%28EN%29)

## All the arcade systems on the Recalbox

> You have now access to up to 4 systems in last version of Recalbox \(mame, imame4all, piFba, fba libretro\) and one "fake" system Neogeo. You can chose the core you want to use in [recalbox.conf](https://github.com/recalbox/recalbox-os/wiki/recalbox.conf-%28EN%29)

### **piFBA**

_Recalbox \(all versions\)_

* piFBA is the most optimized FBA emulator on Recalbox but has a far less better compatibility list than fba\_libretro. Use only if you own a pi0/1 or if a specific game has performance issues on fba\_libretro
* It uses the FBA romset version : **FBA 0.2.96.71** which is based on MAME 0.114 \(April 2007\)
* Size : 3.62GB
* Romsets emulated : 684 \(no clones in this\)
* _roms folder :_ fba
* You can find the list of compatible games in your recalbox at [/recalbox/share/roms/fba/clrmamepro/piFBA\_gamelist.txt](https://raw.githubusercontent.com/digitalLumberjack/recalbox-buildroot/recalbox/board/recalbox/share/roms/fba/clrmamepro/piFBA_gamelist.txt)
* You can find the .dat file with rom checksum for clrmamepro at [/recalbox/share/roms/fba/clrmamepro/fba\_029671\_od\_release\_10\_working\_roms.dat](https://raw.githubusercontent.com/digitalLumberjack/recalbox-buildroot/recalbox/board/recalbox/share/roms/fba/clrmamepro/fba_029671_od_release_10_working_roms.dat)

### **imame4all**

_Recalbox \(all versions\)_

* imame4all is recommended for older games that does not run in piFBA
* It uses the mame romset version : **0.37b5** \(July 2000\)
* Size : 1.86GB
* Romsets emulated : 2 270 \(includes clones etc...\)
* Active Sets 2241/2241
* ·Parents 560/560
* ·Clones 990/990
* ·Others 690/690
* ·BIOS: 1
* Samples: 35
* CHDs: 0
* _roms folder:_ mame
* You can find the list of compatible games in your recalbox at[/recalbox/board/recalbox/share/roms/mame/clrmamepro/imame4all\_gamelist.txt](https://raw.githubusercontent.com/digitalLumberjack/recalbox-buildroot/recalbox/board/recalbox/share/roms/mame/clrmamepro/imame4all_gamelist.txt)
* You can find the .dat file with rom checksum for clrmamepro at [/recalbox/share/roms/mame/clrmamepro/imame4all.dat](https://raw.githubusercontent.com/digitalLumberjack/recalbox-buildroot/recalbox/board/recalbox/share/roms/mame/clrmamepro/imame4all.dat)
* If a game doesn't work with imame4all \(MAME 0.37b5 romsets\), you can try `lr-mame2003`with a MAME 0.78 ROM set

### **lr-mame2003**

_Recalbox \(since v3.3.0-beta-11\)_

* lr-mame2003 is more recent mame emulator than imame4all. It brings new games compatibility and is only available on RPI2
* It uses the mame romset version : **0.78** \(December 2003\)
* Romsets emulated : 4,705
* Active Sets 4705/4705
* ·Parents 1042/1042
* ·Clones 2039/2039
* ·Others 1624/1624
* ·BIOS: 15
* Samples: 56
* CHDs: 56
* _roms folder:_ mame
* You can find the list of compatible games in your recalbox at \(coming soon\)\_
* You can find the .dat file with rom checksum for clrmamepro at [/recalbox/recalbox-os/master/wiki/dat/mame2003.dat](https://raw.githubusercontent.com/recalbox/recalbox-os/master/wiki/dat/mame2003.dat)

### **libretro FBA**

* libretro FBA is a libretro version of FBA. It brings new games compatibility and is only available on RPI2. For exemple, it's the only one can lauch capcom [CPSIII](https://en.wikipedia.org/wiki/CP_System_III#List_of_games) games.

_Recalbox \(since 6.0\)_

* It uses the FBA romset version : _FBA 0.2.97.44_ which is based on MAME 0.189
* You can find the changelog at [fbalpha changelog](https://www.fbalpha.com/view/240/)
* You can find the list of compatible games in your recalbox at [/libretro/libretro-fba/blob/master/gamelist.txt](https://gitlab.com/recalbox/recalbox/blob/master/package/recalbox-romfs/recalbox-romfs-fba_libretro/roms/fba_libretro/clrmamepro/fba_libretro_gamelist.txt)
* You can find the .dat file with rom checksum for clrmamepro at [/recalbox/recalbox-os/master/wiki/dat/fba\_0.2.97.42.dat](https://gitlab.com/recalbox/recalbox/blob/master/package/recalbox-romfs/recalbox-romfs-fba_libretro/roms/fba_libretro/clrmamepro/FB%20Alpha%20v0.2.97.42.dat)

### **Neogeo system**

The Neogeo system is not an emulator itself. You need to configure the core to use in [recalbox.conf](https://github.com/recalbox/recalbox-os/wiki/recalbox.conf-%28EN%29). This will allow you to visually separate the NeoGeo games from the other arcade games, they will appear as a dedicated system in Emulation Station

