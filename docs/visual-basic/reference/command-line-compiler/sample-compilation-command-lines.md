---
title: Exemples de lignes de commande de compilation (Visual Basic)
ms.date: 03/13/2018
helpviewer_keywords:
- command line [Visual Basic], compilers
- compilation [Visual Basic], command-line
- command-line compilers
- compiling source code [Visual Basic], from command line
- Visual Basic compiler, sample command lines
ms.assetid: 5bfbb487-5f47-4267-969a-39dfb917beeb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7b0f1fc1d269801efdbf2e89d10679dc8159851f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653661"
---
# <a name="sample-compilation-command-lines-visual-basic"></a>Exemples de lignes de commande de compilation (Visual Basic)
Comme alternative à compiler les programmes Visual Basic dans Visual Studio, vous pouvez compiler à partir de la ligne de commande pour produire des fichiers exécutables (.exe) ou des fichiers de bibliothèque de liens dynamiques (.dll).  
  
 Le compilateur de ligne de commande Visual Basic prend en charge un ensemble complet des options qui contrôlent l’entrée et de sortie des fichiers, des assemblys, débogage et des options de préprocesseur. Chaque option est disponible sous deux formes interchangeables : `-option` et `/option`. Cette documentation ne décrit que le `-option` formulaire.  
  
 Le tableau suivant répertorie certains exemples de lignes de commande que vous pouvez modifier pour votre usage personnel.  
  
|À|Utilisez|  
|--------|---------|  
|Compilez le fichier.vb et créer File.exe|`vbc -reference:Microsoft.VisualBasic.dll File.vb`|  
|Compilez le fichier.vb et créer File.dll|`vbc -target:library File.vb`|  
|Compilez le fichier.vb et créer My.exe|`vbc -out:My.exe File.vb`|  
|Compilez le fichier.vb et créer une bibliothèque et un assembly de référence nommé File.dll|`vbc -target:library -ref:.\debug\bin\ref\file.dll File.vb`|
|Tous les fichiers Visual Basic dans le répertoire actif, avec les optimisations se compiler sur et `DEBUG` symbole défini, afin de produire File2.exe|`vbc -define:DEBUG=1 -optimize -out:File2.exe *.vb`|  
|Compilez tous les fichiers Visual Basic dans le répertoire actif, produisant une version debug de File2.dll sans afficher le logo ou les avertissements|`vbc -target:library -out:File2.dll -nowarn -nologo -debug *.vb`|  
|Compilez tous les fichiers Visual Basic dans le répertoire en cours en Something.dll|`vbc -target:library -out:Something.dll *.vb`|  
  
> [!TIP]
>  Lorsque vous générez un projet à l’aide de l’IDE de Visual Studio, vous pouvez afficher les informations associé **vbc** commande avec les options du compilateur dans la fenêtre Sortie. Pour afficher ces informations, ouvrez le [boîte de dialogue Options, projets et Solutions, générer et exécuter](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), puis définissez le **détail de sortie de génération du projet MSBuild** à **Normal** ou augmenter le niveau de détail.   
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
