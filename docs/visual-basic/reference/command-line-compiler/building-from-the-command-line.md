---
title: Génération à partir de la ligne de commande (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- builds [Visual Basic], command-line
- Visual Basic compiler, about Visual Basic compiler
- command line [Visual Basic], compilers
- command line [Visual Basic], building from
- command line [Visual Basic], builds
- compilers [Visual Basic], invoking from command line
- command-line builds
- compiling source code
- command-line compilers [Visual Basic], Visual Basic
- command line [Visual Basic], Visual Basic
ms.assetid: e61947e9-a42e-4717-a699-5f70a98cdd03
ms.openlocfilehash: 798baa90308c83e42b335635fb23a9983f5180fb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61839382"
---
# <a name="building-from-the-command-line-visual-basic"></a>Génération à partir de la ligne de commande (Visual Basic)
Un projet Visual Basic se compose d’un ou plusieurs fichiers sources séparés. Pendant le processus appelé compilation, ces fichiers sont regroupés en un seul package, un seul fichier exécutable qui peut être exécuté en tant qu’application.  
  
 Visual Basic fournit un compilateur de ligne de commande comme alternative aux programmes de compilation dans l’environnement de développement intégré (IDE) Visual Studio. Le compilateur de ligne de commande est conçu pour les situations dans lequel vous n’avez pas besoin l’ensemble complet des fonctionnalités de l’IDE, par exemple, lorsque vous utilisez ou écriture pour les ordinateurs avec un espace de stockage ou mémoire limitées sur le système.  
  
  Pour compiler des fichiers sources à partir de l’IDE de Visual Studio, choisissez le **Build** commande à partir de la **Build** menu.  
  
> [!TIP]
>  Lorsque vous générez des fichiers projet à l’aide de l’IDE Visual Studio, vous pouvez afficher des informations sur associé **vbc** commande et ses commutateurs dans la fenêtre Sortie. Pour afficher ces informations, ouvrez le [boîte de dialogue Options, projets et Solutions, générer et exécuter](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), puis définissez le **niveau de détail de sortie de génération de projet MSBuild** à **Normal** ou un niveau plus élevé de commentaires. Pour plus d'informations, voir [Procédure : Afficher, enregistrer et configurer les fichiers journaux de génération](/visualstudio/ide/how-to-view-save-and-configure-build-log-files).  
  
 Vous pouvez compiler des fichiers projet (.vbproj) à une invite de commandes à l’aide de MSBuild. Pour plus d’informations, consultez [de ligne de commande référence](/visualstudio/msbuild/msbuild-command-line-reference) et [procédure pas à pas : Utiliser MSBuild](/visualstudio/msbuild/walkthrough-using-msbuild).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour appeler le compilateur de ligne de commande](../../../visual-basic/reference/command-line-compiler/how-to-invoke-the-command-line-compiler.md)  
 Décrit comment appeler le compilateur de ligne de commande à l’invite de MS-DOS ou à partir d’un sous-répertoire spécifique.  
  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 Fournit une liste d’exemples de lignes de commande que vous pouvez modifier pour votre usage personnel.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 Fournit des listes d’options du compilateur, organisées par ordre alphabétique ou par objet.  
  
 [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)  
 Décrit comment compiler des sections de code.  
  
 [Génération et nettoyage de solutions et de projets dans Visual Studio](/visualstudio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio)  
 Décrit comment organiser ce que sera inclus dans les différentes versions, choisissez Propriétés du projet et vous assurer que les projets sont générés dans le bon ordre.
