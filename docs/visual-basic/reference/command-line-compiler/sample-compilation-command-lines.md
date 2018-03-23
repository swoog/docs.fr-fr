---
title: Exemples de lignes de commande de compilation (Visual Basic)
ms.date: 03/13/2018
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- command line [Visual Basic], compilers
- compilation [Visual Basic], command-line
- command-line compilers
- compiling source code [Visual Basic], from command line
- Visual Basic compiler, sample command lines
ms.assetid: 5bfbb487-5f47-4267-969a-39dfb917beeb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cf20e2916efd2eb10065be22c319e34ddb2bda9a
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2018
---
# <a name="sample-compilation-command-lines-visual-basic"></a><span data-ttu-id="d7416-102">Exemples de lignes de commande de compilation (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d7416-102">Sample compilation command lines (Visual Basic)</span></span>
<span data-ttu-id="d7416-103">En guise d’alternative à la compilation de programmes Visual Basic depuis [!INCLUDE[vsprvs](~/includes/vsprvs-md.md)], vous pouvez les compiler depuis la ligne de commande pour produire des fichiers exécutables (.exe) ou des fichiers de bibliothèque de liens dynamiques (.dll).</span><span class="sxs-lookup"><span data-stu-id="d7416-103">As an alternative to compiling Visual Basic programs from within [!INCLUDE[vsprvs](~/includes/vsprvs-md.md)], you can compile from the command line to produce executable (.exe) files or dynamic-link library (.dll) files.</span></span>  
  
 <span data-ttu-id="d7416-104">Le compilateur de ligne de commande Visual Basic prend en charge un ensemble complet des options qui contrôlent l’entrée et de sortie des fichiers, des assemblys, débogage et des options de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="d7416-104">The Visual Basic command-line compiler supports a complete set of options that control input and output files, assemblies, and debug and preprocessor options.</span></span> <span data-ttu-id="d7416-105">Chaque option est disponible sous deux formes interchangeables : `-option` et `/option`.</span><span class="sxs-lookup"><span data-stu-id="d7416-105">Each option is available in two interchangeable forms: `-option` and `/option`.</span></span> <span data-ttu-id="d7416-106">Cette documentation ne décrit que le `-option` formulaire.</span><span class="sxs-lookup"><span data-stu-id="d7416-106">This documentation shows only the `-option` form.</span></span>  
  
 <span data-ttu-id="d7416-107">Le tableau suivant répertorie certains exemples de lignes de commande que vous pouvez modifier pour votre usage personnel.</span><span class="sxs-lookup"><span data-stu-id="d7416-107">The following table lists some sample command lines you can modify for your own use.</span></span>  
  
|<span data-ttu-id="d7416-108">À</span><span class="sxs-lookup"><span data-stu-id="d7416-108">To</span></span>|<span data-ttu-id="d7416-109">Utilisez</span><span class="sxs-lookup"><span data-stu-id="d7416-109">Use</span></span>|  
|--------|---------|  
|<span data-ttu-id="d7416-110">Compilez le fichier.vb et créer File.exe</span><span class="sxs-lookup"><span data-stu-id="d7416-110">Compile File.vb and create File.exe</span></span>|`vbc -reference:Microsoft.VisualBasic.dll File.vb`|  
|<span data-ttu-id="d7416-111">Compilez le fichier.vb et créer File.dll</span><span class="sxs-lookup"><span data-stu-id="d7416-111">Compile File.vb and create File.dll</span></span>|`vbc -target:library File.vb`|  
|<span data-ttu-id="d7416-112">Compilez le fichier.vb et créer My.exe</span><span class="sxs-lookup"><span data-stu-id="d7416-112">Compile File.vb and create My.exe</span></span>|`vbc -out:My.exe File.vb`|  
|<span data-ttu-id="d7416-113">Compilez le fichier.vb et créer une bibliothèque et un assembly de référence nommé File.dll</span><span class="sxs-lookup"><span data-stu-id="d7416-113">Compile File.vb and create both a library and a reference assembly named File.dll</span></span>|`vbc -target:library -ref:.\debug\bin\ref\file.dll File.vb`|
|<span data-ttu-id="d7416-114">Tous les fichiers Visual Basic dans le répertoire actif, avec les optimisations se compiler sur et `DEBUG` symbole défini, afin de produire File2.exe</span><span class="sxs-lookup"><span data-stu-id="d7416-114">Compile all Visual Basic files in the current directory, with optimizations on and the `DEBUG` symbol defined, producing File2.exe</span></span>|`vbc -define:DEBUG=1 -optimize -out:File2.exe *.vb`|  
|<span data-ttu-id="d7416-115">Compilez tous les fichiers Visual Basic dans le répertoire actif, produisant une version debug de File2.dll sans afficher le logo ou les avertissements</span><span class="sxs-lookup"><span data-stu-id="d7416-115">Compile all Visual Basic files in the current directory, producing a debug version of File2.dll without displaying the logo or warnings</span></span>|`vbc -target:library -out:File2.dll -nowarn -nologo -debug *.vb`|  
|<span data-ttu-id="d7416-116">Compilez tous les fichiers Visual Basic dans le répertoire en cours en Something.dll</span><span class="sxs-lookup"><span data-stu-id="d7416-116">Compile all Visual Basic files in the current directory to Something.dll</span></span>|`vbc -target:library -out:Something.dll *.vb`|  
  
> [!TIP]
>  <span data-ttu-id="d7416-117">Lorsque vous générez un projet à l’aide de l’IDE de Visual Studio, vous pouvez afficher les informations associé **vbc** commande avec les options du compilateur dans la fenêtre Sortie.</span><span class="sxs-lookup"><span data-stu-id="d7416-117">When you build a project by using the Visual Studio IDE, you can display information about the associated **vbc** command with its compiler options in the output window.</span></span> <span data-ttu-id="d7416-118">Pour afficher ces informations, ouvrez le [boîte de dialogue Options, projets et Solutions, générer et exécuter](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), puis définissez le **détail de sortie de génération du projet MSBuild** à **Normal** ou augmenter le niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="d7416-118">To display this information, open the [Options Dialog Box,  Projects and Solutions, Build and Run](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), and then set the **MSBuild project build output verbosity** to **Normal** or a higher level of verbosity.</span></span>   
  
## <a name="see-also"></a><span data-ttu-id="d7416-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7416-119">See Also</span></span>  
 [<span data-ttu-id="d7416-120">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d7416-120">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="d7416-121">Compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="d7416-121">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
