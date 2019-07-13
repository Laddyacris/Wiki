# L'arcade avancée sur Recalbox

Cette page est la suite de [L'arcade facile pour Recalbox](https://github.com/recalbox/recalbox-os/wiki/L%27arcade-facile-sur-Recalbox-%28FR%29)

## BestArcade4Recalbox

Vous pouvez trouver ici la liste des jeux mame les plus importants et leur état de fonctionnement sur mame et fba\_libretro : [BestArcade4Recalbox](https://docs.google.com/spreadsheets/d/1F5tBguhRxpj1AQcnDWF6AVSx4av_Gm3cDQedQB7IECk/edit#gid=131171669&vpid=A179)

## Type de romset : non-merged, split et merged

Il existe trois types de romset :

* en split, les fichiers en communs entre parents et clones ne sont que dans le zip parent. pour utiliser un clone ilf faut donc avoir les deux roms parent et clone
* en non-merged, tous les fichiers nécessaires pour le clone sont dans le zip de celui-ci
* en merged, parent et clone sont fusionnés dans le même zip

Le plus intéressant est donc le romset non-merged

## ClrMamePro

Pour vérifier la compatibilité de vos jeux, vous pouvez utiliser clrmamepro et le [tutoriel correspondant](https://github.com/recalbox/recalbox-os/wiki/V%C3%A9rifier-la-version-de-vos-roms-avec-clrmamepro-%28FR%29).

## Tous les émulateurs arcades sur la Recalbox

> Vous pouvez maintenant utiliser jusqu'à quatre émulateurs arcade différents dans la dernière version de Recalbox \(mame, imame4all, piFba, fba libretro\) et l'émulateur "simulé" Neogeo. Vous pouvez choisir le core que vous souhaitez utiliser dans [recalbox.conf](https://github.com/recalbox/recalbox-os/wiki/recalbox.conf-%28FR%29)

### **piFBA**

_Recalbox \(toutes les versions\)_

* piFBA est le mieux optimisé des émulateurs FBA sur la RecalBox mais est compatible avec beaucoup moins de jeux que fba\_libretro. A n'utiliser que si vous avez un pi0/1 ou si vous voulez améliorez les performances d'un jeu particulier ramant sur fba\_libretro
* Il utilise le romset MAME version: **FBA 0.2.96.71** qui est basé sur le set MAME 0.114 \(Avril 2007\)
* Poids : 3.62GB
* Romsets émulées : 684 \(Pas de clone dans ce set\)
* _répertoire des roms :_ fba
* Vous pouvez trouver la liste des jeux compatibles sur la RecalBox à l'emplacement suivant [/recalbox/share/roms/fba/clrmamepro/piFBA\_gamelist.txt](https://raw.githubusercontent.com/recalbox/recalbox-buildroot/rb-4.0.X/board/recalbox/fsoverlay/recalbox/share_init/roms/fba/clrmamepro/piFBA_gamelist.txt)
* Vous trouverez le fichier .dat pour vérifier les roms avec clrmamepro à l'emplacement suivant [/recalbox/share/roms/fba/clrmamepro/fba\_029671\_od\_release\_10\_working\_roms.dat](https://raw.githubusercontent.com/recalbox/recalbox-buildroot/rb-4.0.X/board/recalbox/fsoverlay/recalbox/share_init/roms/fba/clrmamepro/fba_029671_od_release_10_working_roms.dat)

### **imame4all**

_Recalbox \(toutes les versions\)_

* imame4all est recommandé pour les vieux jeux qui ne fonctionnent pas avec piFBA
* Il utilise le romset MAME version: **0.37b5** \(Juillet 2000\)
* Poids : 1.86GB
* Romsets émulées : 2 270 \(inclu clones etc...\)
* Active Sets 2241/2241
* ·Parents 560/560
* ·Clones 990/990
* ·Others 690/690
* ·BIOS 1/1
* _\(Si un jeu ne marche pas dans le romset 0.37b5, vous pouvez essayer avec le jeu du romset mame 0.81\)_
* _répertoire des roms :_ mame
* Vous pouvez trouver la liste des jeux compatibles sur la RecalBox à l'emplacement suivant [/recalbox/board/recalbox/share/roms/mame/clrmamepro/imame4all\_gamelist.txt](https://raw.githubusercontent.com/recalbox/recalbox-buildroot/rb-4.0.X/board/recalbox/fsoverlay/recalbox/share_init/roms/mame/clrmamepro/imame4all/imame4all_gamelist.txt)
* Vous trouverez le fichier .dat pour vérifier les roms avec clrmamepro à l'emplacement suivant [/recalbox/share/roms/mame/clrmamepro/imame4all.dat](https://raw.githubusercontent.com/recalbox/recalbox-buildroot/rb-4.0.X/board/recalbox/fsoverlay/recalbox/share_init/roms/mame/clrmamepro/imame4all/imame4all.dat)

### **lr-mame2003**

_Recalbox \( depuis la v3.3.0-beta-11\)_

* lr-mame2003 est un emulateur plus récent que imame4all. Beaucoup plus de jeux sont fonctionnels mais cet émulateur n'est disponible que sur RPI2 et RPI3.
* mame romset version : **0.78** \(December 2003\)
* Taille : 1.86GB
* Romsets emulés : 4 705 \(includes clones etc...\)
* Active Sets 4705/4705
* ·Parents 1042/1042
* ·Clones 2039/2039
* ·Others 1624/1624
* ·BIOS 1/1
* _répertoire des roms :_ mame
* Vous pouvez trouver la liste des jeux compatibles sur la RecalBox à l'emplacement suivant _\(bientôt\)_
* Vous trouverez le fichier .dat pour vérifier les roms avec clrmamepro à l'emplacement suivant [/recalbox/recalbox-os/master/wiki/dat/mame2003.dat](https://raw.githubusercontent.com/recalbox/recalbox-buildroot/rb-4.0.X/board/recalbox/fsoverlay/recalbox/share_init/roms/mame/clrmamepro/mame2003/mame2003.dat)

### **lr-mame2003-plus**

MAME 2003-Plus \(également appelé MAME 2003+ et mame2003-plus\) est un noyau d'émulateur de système arcade libretro qui met l'accent sur des performances élevées et une compatibilité étendue avec les périphériques mobiles, les ordinateurs à carte unique, les systèmes intégrés et autres plates-formes similaires.

Afin de tirer parti des performances et des exigences matérielles moindres d'une architecture MAME antérieure, MAME 2003-Plus a commencé avec le code base de MAME 2003, lui-même dérivé de xmame 0.78. Sur cette base, les contributeurs de MAME 2003-Plus ont rétro porté le support de plusieurs centaines de jeux supplémentaires, ainsi que d’autres fonctionnalités non présentes à l’origine dans MAME 0.78.

MAME Version: 0.78-0.188 \(MAME 0.78 en tant que ligne de base avec d'autres ROM basées sur des jeux de roms MAME ultérieurs\)

* Active Sets: 4850
* BIOS: 15
* CHDs: 30
* Samples: 66 + 6 Optional "Soundtrack Samples"
* [MAME 2003-Plus XML DAT File](https://github.com/libretro/mame2003-plus-libretro/blob/master/metadata/mame2003-plus.xml)

### **lr-mame2010**

\_Recalbox \(depuis recalbox 2018.02.x\). Basé sur le romset mame 0.139

* MAME Version: 0.139 \(August 2010\) Active Sets: 8782
* •BIOS: 67
* •CHDs: 406
* •Samples: 70 \(4 samples manquants\)

### **AdvanceMame 3.x**

\_Recalbox \(depuis recalbox 4.1\) emulateur standalone, initialement ajouté pour la configuration pour écrans CRT. Il est basé sur le romset mame 0.106.

* Mame Version : Mame 0.106 \(Mai 2006\) Active Sets: 6166
* BIOS: 26
* CHDs: 86
* Samples: 64 \(3 samples manquants\)

### **libretro FBA**

* libretro FBA est un core de libretro basé sur FBA, il est le seul a faire tourner certains systèmes \(CPS3 par exemple\) mais est moins rapide que piFBA

_Recalbox \(depuis 6.0\)_

* Il utilise le set de rom FBA version : **FBA 0.2.97.44** qui est basé sur le set MAME 0.189
* Vous pouvez trouver le changelog de FBA à l'emplacement suivant [fbalpha changelog](https://www.fbalpha.com/view/240/)
* Vous trouverez le fichier .dat pour vérifier les roms avec clrmamepro à l'emplacement suivant [fba 0.2.97.44 dat](https://github.com/libretro/fbalpha/tree/master/dats)

### **Neogeo \(simulé\)**

Le système Neogeo n'est pas un émulateur en soit.  
Il permet d'isoler séparément les jeux neogeo des autres jeux d'arcade, ils apparaîtront alors comme un système dédié dans EmulationStation.  
Par défaut il utilise FBA libretro. Vous pouvez utiliser le fichier dat suivant pour créer et vérifier votre romset : [FBA 0.2.97.44 Neogeo Only](https://github.com/libretro/fbalpha/blob/master/dats/FB%20Alpha%20%28ClrMame%20Pro%20XML%2C%20Arcade%20only%29.dat)

