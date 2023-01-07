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

<h2>Erreur dotnet lors de l'execution de mgcb-editor</h2>
  
  ![image](https://user-images.githubusercontent.com/90217410/211167692-6dc373f5-6a48-4c8c-850c-b69c848689d9.png)
 
   Si vous avez une erreur de ce genre, c'est que vous avez sans doute la mauvaise version de mgcb-editor
  
  Pour vérifier cela, vous pouvez faire dotnet tool list -g dans un cmd et si mgcb-editor est en 3.8.1, le problème vien de la vesion.
  
  ![image](https://user-images.githubusercontent.com/90217410/211167699-daec41f4-6bc1-429f-b206-67fc1f94e888.png)

  
  1)En premier on désinstalle mgcb-editor en faisant dotnet tool uninstall dotnet-mgcb-editor -g
  2)Puis on réinstalle la bonne version avec dotnet tool install --global dotnet-mgcb-editor --version 3.8.0.1641
  3)Après cela vous pouvez vérifier la version avec la commande dotnet tool list -g
  
  ![image](https://user-images.githubusercontent.com/90217410/211167710-6f043a04-35af-4a3e-af75-ce6488c7bf4c.png)
  
  4)Lorsqu'il est réinstallé, assurez vous de bien changer le chemin (ouvrir avec) du Content.mgcb dans votre projet par celui dans C:\Users\UTILISATEUR\.dotnet\tools
  
  ![image](https://user-images.githubusercontent.com/90217410/211167720-51eb0cbb-85eb-461a-b315-33d0445226ad.png)

  5)Si après changement, le content.mgcb ne se lance pas, c'est que vous avez probablement pas let Net core 3.1. Vérifiez en faisait mgcb-editor dans une console et si vous avez ce message c'est que s'est le cas:

![image](https://user-images.githubusercontent.com/90217410/211167862-8d119258-5dec-4e23-9ff6-4636423fdfac.png)

  Installez le Net Core 3.1 sur le site officle de microsoft: [![Uploading image.png…]()](https://dotnet.microsoft.com/en-us/download/dotnet/3.1)

