<h1>Tuto pour résoudre les problèmes Monogame</h1>

<h2>Tous les using sont en rouge</h2>

  ![image](https://user-images.githubusercontent.com/90217410/211167009-65300581-81f0-4767-8a0a-8c4e21c2aa07.png)


  Si tous les using sont en rouge, c'est que les package Nuget ne sont pas retrouvé par le projet.
  ![image](https://user-images.githubusercontent.com/90217410/211167028-e900c42e-f53b-4dcd-b9af-e56af6c3f5ec.png)

  En faite si les package ont été installés sur un autre PC, il sont installés localement et ont un chemin d'accès unique.
  Donc quand on charge sont projet depuis un autre pc, il se peut que ceux-ci ne soient pas retrouvés.

  1) Pour résoudre cela Il faut en premier, garder la liste des package (car on va les désinstallés et réinstaller plus tard).
  2) Après cela, il faut donc désinstallé tous les package du projet en allant dans l'editeur des package Nuget, et en cliquant sur la croix rouge sur chaque package.
  ![image](https://user-images.githubusercontent.com/90217410/211166911-bf27b66f-a594-423b-8be5-fa1b573a5506.png)

  3) Lorsqu'ils sont tous désinstallé, allez dans source du package en haut à droite et cliquez sur le logo paramètre.
  4) Dans les paramètre de source du package, créez une nouvelle source avec comme lien de source: C:\Users\UTILISATEUR\.nuget\packages

  5) Puis séléctionnez votre nouvelle source en haut a droite, et réinstallez tous vos package.
  Si les étapes ont été suivies correctement, les package devraint être chargés correctement. Et ne plus avoir de problème dans l'image ci dessous.
  ![image](https://user-images.githubusercontent.com/90217410/211167030-2ac006c7-1239-4556-8b54-d438bc8d7855.png)
