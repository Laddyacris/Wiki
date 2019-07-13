# Neogeo Unibios

## What Unibios does:

* Change region \(Europe/USA/Japan\) and Mode: \(AES/MVS\)  
* Access the soft dip to change game Difficulty/Life/Time etc  
* In-game Cheat database  
* Jukebox music player… and a lot more!  

## How to install it on PiFBA:

1. Get it here \(version 3.2\): [http://unibios.free.fr/download.html](http://unibios.free.fr/download.html)  
2. Extract the downloaded file, rename uni-bios.rom to asia-s3.rom.  
3. Open your own neogeo.zip, there should be a asia-s3.rom file inside, back it up if needed.  
4. Put the new renamed asia-s3.rom into neogeo.zip, replace it with the old one.  
5. Now upload the new neogeo.zip back to the Recalbox share folders, on both \bios and \finalburnalpha  

## How to install it on Fba\_libretro :

Launch a game and enter in the retroarch menu \( **Hotkey + B** \)

Go to

> Quick Menu &gt; Options

and set :  
&gt;

> Neo geo mode &gt; unibios

## Usage:

For Pifba

* Start up any neogeo game, you will see the new UNIVERSE BIOS v3.2 splash screen.  
* During this startup screen, press and hold BXY for region/mode setup, or hold ABX for dip switch menu.  
* To access the in-game menu, press and hold BXY+START at the same time.  

For fba libretro

* Start up any neogeo game, you will see the new UNIVERSE BIOS splash screen.  
* During this startup screen, press and hold CBA \(XBA\) for region/mode setup - Press C to exit 
* To access the in-game menu, press and hold CBA \(XBA\) +START at the same time.  

For dip switch Menu in fba libretro During UNIVERSE BIOS Splash screen , hold A+X+Y

Setting up the soft dip :

For active blood : Region Japan / Mode arcade

slot metal slug

blood &gt; on

Press C to exit.

## BIOS

Neo Geo requires a neogeo.zip BIOS file. It will be placed with your ROMs in

```text
/recalbox/share/roms/neogeo
or
/recalbox/share/roms/fba_libreto
or
/recalbox/share/roms/fba
```

These are the contents of a verified working neogeo.zip BIOS file

```text
000-lo.lo
asia-s3.rom
japan-j3.bin
neo-geo.rom
ng-lo.rom
ng-sfix.rom
ng-sm1.rom
sfix.sfix
sm1.sm1
sp-1v1_3db8c.bin
sp-45.sp1
sp-e.sp1
sp-j2.sp1
sp-s.sp1
sp-s2.sp1
sp-u2.sp1
sp1.jipan.1024
uni-bios_1_0.rom
uni-bios_1_1.rom
uni-bios_1_2.rom
uni-bios_1_2o.rom
uni-bios_1_3.rom
uni-bios_2_0.rom
uni-bios_2_1.rom
uni-bios_2_2.rom
uni-bios_2_3.rom
uni-bios_2_3o.rom
uni-bios_3_0.rom
uni-bios_3_1.rom
vs-bios.rom
```

