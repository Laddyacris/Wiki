---
description: >-
  Ce tutoriel est destiné aux débutants, afin de les aider à jouer facilement
  aux jeux arcade sur Recalbox.
---

# L'arcade facile sur Recalbox

## Introduction \(6.0-DragonBlaze\)

L'arcade est depuis longtemps l'émulation la plus compliquée à cause de sa nature : Les bornes d'arcade n'utilisent pas toutes le même hardware, et doivent donc toutes être émulées indépendamment.  
Imaginez que vous voulez jouer à 5 jeux d'arcade différents, vous pourriez avoir à utiliser cinq émulateurs différents. Alors que si vous souhaitez jouer à cinq jeux SNES vous pourrez utiliser un seul et même émulateur SNES.

Et c'est pour cela que MAME a été inventé : Mame peut être assimilé à un meta-émulateur, rassemblant les différents émulateurs de chaque borne d'arcade en un seul système, ce qui permet à l'utilisateur de jouer facilement à des jeux d'arcade sans aucune connaissance du hardware de la borne d'arcade faisant tourner ceux ci.

Ce n'est pas un petit exploit, et c'est pourquoi MAME est si compliqué à utiliser.

## Principes généraux de l'émulation MAME

Il n'y a que deux principes généraux à comprendre pour utiliser facilement MAME sur votre Recalbox : les romsets et les fichiers de BIOS/drivers

### Les romsets

Un romset est l'ensemble des différentes roms de jeux émulées par une version donnée de MAME.  
Un romset contient des roms parents qui sont des roms contenant la version 'principale' d'un jeu et des roms clones qui sont des versions 'alternatives' des roms parents. Comme vous vous en doutez, dans la plupart des cas on peut se débarrasser des roms clones pour n'utiliser que les roms principales \(appelées parents en arcade\)

La majorité du code utilisé pour faire fonctionner ces roms de jeux est inclus dans l'exécutable de MAME. Malheureusement, cela veut dire qu'il y a une relation forte et interdépendante entre une version de MAME et les versions des roms de jeux : quand une nouvelle version de MAME sort, il est parfois nécessaire pour les développeurs de mettre à jour les roms de jeux pour qu'elles fonctionnent parfaitement avec la nouvelle version de l'émulateur.

Pour dire les choses simplement : si vous utilisez une version précise de l'émulateur MAME, par exemple la version 0.78, vous devez récupérer et utiliser la version 0.78 du romset. Certains jeux d'un autre romset peuvent marcher avec votre version 0.78 de MAME mais **le seul moyen d'être absolument sûr que la grande majorité des jeux fonctionnent, est de toujours utiliser une version de MAME avec le romset de même version**.

Pour des version récentes de MAME \(comme celle utilisée par fba\_libretro\) il y a de moins en moins de roms de jeux mises à jour et il est parfois possible d'utiliser un romset plus ancien et d'avoir tout de même la plupart des jeux jouables.

### BIOS / Drivers

Certaines roms de jeux d'un romset peuvent nécessiter des fichiers de BIOS, le cas le plus connu étant les jeux neogeo. Utilisons ceux ci comme exemple :  
Si vous voulez utiliser des jeux neogeo, vous allez devoir copier le fichier de BIOS/driver \(dans ce cas neogeo.zip\) dans le même répertoire que la rom du jeu. C'est tout !

Bien sûr si vous utilisez des sous répertoires pour vos jeux \(genre ou hardware par exemple\), vous devrez copier les fichiers de BIOS dans chaque répertoire contenant des jeux qui les nécessitent. **Etant donné que ces fichiers de BIOS sont plutôt petits en taille, il est plus simple de les copier tous dans chacun de vos sous-répertoires.**

Où trouver ces fichiers de BIOS me dites vous ? Eh bien c'est plutôt simple : dans votre romset !

Si un jeu ne se lance pas et revient directement à l'écran d'Emulationstation, essayez de trouver le BIOS correspondant et copiez-le dans le répertoire de votre rom de jeu.

## L’émulation arcade sur Recalbox

Comme la page wiki [L'arcade avancée sur Recalbox](https://github.com/recalbox/recalbox-os/wiki/L%27arcade-avanc%C3%A9e-sur-Recalbox-%28FR%29) l'explique, il y a plusieurs émulateurs arcade inclus dans Recalbox.

Nous n'aurons besoin que de deux d'entre eux pour lancer la majorité des jeux arcades sur votre Raspberry Pi.

Ces deux systèmes sont :

* Mame
  * _mame/romset version :_ 0.78
  * _répertoire des roms :_ mame
* FBA\_libretro
  * FBA est une version alternative de MAME \(émulant moins de bornes d'arcade\) mais il fonctionne suivant les mêmes principes que je je viens juste d'expliquer.
  * _mame/fba romset version :_ 0.189 correspond au romset FBA 0.2.97.44
  * _répertoire des roms:_ fba\_libretro

Certains jeux ne fonctionneront sur Recalbox qu'avec Mame et d'autres qu'avec FBA\_libretro.

Suivez le document [BestArcade4Recalbox](https://docs.google.com/spreadsheets/d/1F5tBguhRxpj1AQcnDWF6AVSx4av_Gm3cDQedQB7IECk/edit?usp=sharing) pour déterminer quel est le bon émulateur pour le jeu auquel vous souhaitez jouer.

## Configurons votre recalbox !

Tout d'abord téléchargez les full romsets pour les deux émulateurs : romset 0.78 pour mame et romset 0.189 \(ou romset FBA 0.2.97.44\) pour fba\_libretro.  
Si vous ne trouvez par le romset dans la version, une version supérieure peut être téléchargée, mais elle devra être rendue compatible en suivant les étapes de [https://github.com/recalbox/recalbox-os/wiki/V%C3%A9rifier-la-version-de-vos-roms-avec-clrmamepro-%28FR%29](https://github.com/recalbox/recalbox-os/wiki/V%C3%A9rifier-la-version-de-vos-roms-avec-clrmamepro-%28FR%29)

Vous préféreriez surement télécharger chaque jeu un par un car les full romsets ont une taille plutôt énorme, mais il est rarement facile de trouver des roms individuelles et d'être sûr qu'elles sont dans la bonne version.  
Les full romsets sont le seul moyen sûr d'éviter les prises de tête !

Vous n'êtes plus qu'à quelques minutes avant de jouer à des jeux d'arcade excellents sur votre Recalbox.

### Copie des BIOS/drivers

Tout d'abord nous allons copier les fichiers BIOS/drivers de nos romsets, contrairement aux BIOS des autres consoles ceux ci ne se copient pas dans le répertoire bios mais dans le répertoire des roms :

* Récupérez les fichiers suivants du romset 0.78 pour MAME et copiez les dans le répertoire des roms mame, la liste complète de ces fichiers est la suivante : _acpsx.zip, cpzn1.zip, cpzn2.zip, cvs.zip, decocass.zip, konamigx.zip, megaplay.zip, megatech.zip, neogeo.zip, nss.zip, pgm.zip, playch10.zip, skns.zip, stvbios.zip, taitofx1.zip, tps.zip_
* Récupérez les fichiers suivants du romset 0.189 \(FBA 0.2.97.44\) pour fba\_libretro et copiez les dans le répertoire des roms fba\_libretro, je n'ai eu besoin que de deux d'entre eux : _neogeo.zip_et _pgm.zip_

### Copie des jeux

* Vérifiez dans le document [BestArcade4Recalbox](https://docs.google.com/spreadsheets/d/1F5tBguhRxpj1AQcnDWF6AVSx4av_Gm3cDQedQB7IECk/edit?usp=sharing) quel est le bon émulateur à utiliser pour le jeu que vous souhaitez émuler :
  * si le jeu est dans l'onglet mame, copiez la rom du jeu \(fichier zip non décompressé\) depuis votre romset 0.78 vers votre répertoire de roms mame
  * si le jeu est dans l'onglet fba\_libretro, copiez la rom du jeu \(fichier zip non décompressé\) depuis votre romset 0.189 \(FBA 0.2.97.44\) vers votre répertoire de roms fba\_libretro
  * si le jeu est dans l'onglet not found or not working tab, devinez quoi ?
* JOUEZ ! \(ou pas\)

## Trucs supplémentaires

* Si vous voulez cacher vos fichiers de BIOS dans EmulationStation, cachez les en utilisant le menu select
* Rappelez vous, si vous voulez utiliser des sous répertoires dans vos répertoires de roms, faites une copie des fichiers de BIOS/drivers dans chacun des sous-répertoires et déplacez ensuite vos jeux dans les sous-répertoires
* Lire [L'arcade avancée sur Recalbox](https://github.com/recalbox/recalbox-os/wiki/L%27arcade-avanc%C3%A9e-sur-Recalbox-%28FR%29)

