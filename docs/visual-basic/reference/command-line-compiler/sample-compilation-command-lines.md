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
ms.openlocfilehash: 0771ed41d6c58ce7cc98435b405f5819e45393db
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61916758"
---
# <a name="sample-compilation-command-lines-visual-basic"></a>Exemples de lignes de commande de compilation (Visual Basic)
Comme alternative à compiler les programmes Visual Basic dans Visual Studio, vous pouvez compiler à partir de la ligne de commande pour produire des fichiers exécutables (.exe) ou des fichiers de bibliothèque de liens dynamiques (.dll).  
  
 Le compilateur de ligne de commande Visual Basic prend en charge un ensemble complet des options qui contrôlent l’entrée et sortie de fichiers, assemblys, débogage et des options de préprocesseur. Chaque option est disponible sous deux formes interchangeables : `-option` et `/option`. Cette documentation présente uniquement le `-option` formulaire.  
  
 Le tableau suivant répertorie certains exemples de lignes de commande que vous pouvez modifier pour votre usage personnel.  
  
|À|Utilisez|  
|--------|---------|  
|Compilez le fichier.vb et créer File.exe|`vbc -reference:Microsoft.VisualBasic.dll File.vb`|  
|Compilez le fichier.vb et créer File.dll|`vbc -target:library File.vb`|  
|Compilez le fichier.vb et créer My.exe|`vbc -out:My.exe File.vb`|  
|Compilez le fichier.vb et créer une bibliothèque et un assembly de référence nommé File.dll|`vbc -target:library -ref:.\debug\bin\ref\file.dll File.vb`|
|Compilez tous les fichiers Visual Basic dans le répertoire actif, avec les optimisations sur et `DEBUG` symbole, produire File2.exe|`vbc -define:DEBUG=1 -optimize -out:File2.exe *.vb`|  
|Compiler tous les fichiers Visual Basic dans le répertoire actif, produisant une version debug de File2.dll sans afficher le logo ou les avertissements|`vbc -target:library -out:File2.dll -nowarn -nologo -debug *.vb`|  
|Compiler tous les fichiers Visual Basic dans le répertoire actif en Something.dll|`vbc -target:library -out:Something.dll *.vb`|  
  
> [!TIP]
>  Lorsque vous générez un projet à l’aide de l’IDE Visual Studio, vous pouvez afficher des informations sur associé **vbc** commande avec ses options du compilateur dans la fenêtre Sortie. Pour afficher ces informations, ouvrez le [boîte de dialogue Options, projets et Solutions, générer et exécuter](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), puis définissez le **niveau de détail de sortie de génération de projet MSBuild** à **Normal** ou un niveau plus élevé de commentaires.   
  
## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
