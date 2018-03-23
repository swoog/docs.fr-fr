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
ms.openlocfilehash: a7c3fac318e05c5e3d6fb9dd7117cac70ead03dc
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="sample-compilation-command-lines-visual-basic"></a><span data-ttu-id="845be-102">Exemples de lignes de commande de compilation (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="845be-102">Sample compilation command lines (Visual Basic)</span></span>
<span data-ttu-id="845be-103">En guise d’alternative à la compilation [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] programmes depuis [!INCLUDE[vsprvs](~/includes/vsprvs-md.md)], vous pouvez les compiler depuis la ligne de commande pour produire des fichiers exécutables (.exe) ou des fichiers de bibliothèque de liens dynamiques (.dll).</span><span class="sxs-lookup"><span data-stu-id="845be-103">As an alternative to compiling [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] programs from within [!INCLUDE[vsprvs](~/includes/vsprvs-md.md)], you can compile from the command line to produce executable (.exe) files or dynamic-link library (.dll) files.</span></span>  
  
 <span data-ttu-id="845be-104">Le [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] compilateur de ligne de commande prend en charge un jeu complet d’options qui contrôlent les fichiers d’entrée et de sortie, assemblys et de débogage et du préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="845be-104">The [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] command-line compiler supports a complete set of options that control input and output files, assemblies, and debug and preprocessor options.</span></span> <span data-ttu-id="845be-105">Chaque option est disponible sous deux formes interchangeables : `-option` et `/option`.</span><span class="sxs-lookup"><span data-stu-id="845be-105">Each option is available in two interchangeable forms: `-option` and `/option`.</span></span> <span data-ttu-id="845be-106">Cette documentation ne décrit que le `-option` formulaire.</span><span class="sxs-lookup"><span data-stu-id="845be-106">This documentation shows only the `-option` form.</span></span>  
  
 <span data-ttu-id="845be-107">Le tableau suivant répertorie certains exemples de lignes de commande que vous pouvez modifier pour votre usage personnel.</span><span class="sxs-lookup"><span data-stu-id="845be-107">The following table lists some sample command lines you can modify for your own use.</span></span>  
  
|<span data-ttu-id="845be-108">À</span><span class="sxs-lookup"><span data-stu-id="845be-108">To</span></span>|<span data-ttu-id="845be-109">Utilisez</span><span class="sxs-lookup"><span data-stu-id="845be-109">Use</span></span>|  
|--------|---------|  
|<span data-ttu-id="845be-110">Compilez le fichier.vb et créer File.exe</span><span class="sxs-lookup"><span data-stu-id="845be-110">Compile File.vb and create File.exe</span></span>|`vbc -reference:Microsoft.VisualBasic.dll File.vb`|  
|<span data-ttu-id="845be-111">Compilez le fichier.vb et créer File.dll</span><span class="sxs-lookup"><span data-stu-id="845be-111">Compile File.vb and create File.dll</span></span>|`vbc -target:library File.vb`|  
|<span data-ttu-id="845be-112">Compilez le fichier.vb et créer My.exe</span><span class="sxs-lookup"><span data-stu-id="845be-112">Compile File.vb and create My.exe</span></span>|`vbc -out:My.exe File.vb`|  
|<span data-ttu-id="845be-113">Compiler tous les [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] sur les fichiers dans le répertoire actif, avec les optimisations et les `DEBUG` symbole défini, afin de produire File2.exe</span><span class="sxs-lookup"><span data-stu-id="845be-113">Compile all [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] files in the current directory, with optimizations on and the `DEBUG` symbol defined, producing File2.exe</span></span>|`vbc -define:DEBUG=1 -optimize -out:File2.exe *.vb`|  
|<span data-ttu-id="845be-114">Compilez tous les [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] fichiers dans le répertoire actif, produisant une version debug de File2.dll sans afficher le logo ou les avertissements</span><span class="sxs-lookup"><span data-stu-id="845be-114">Compile all [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] files in the current directory, producing a debug version of File2.dll without displaying the logo or warnings</span></span>|`vbc -target:library -out:File2.dll -nowarn -nologo -debug *.vb`|  
|<span data-ttu-id="845be-115">Compilez tous les [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] fichiers dans le répertoire en cours en Something.dll</span><span class="sxs-lookup"><span data-stu-id="845be-115">Compile all [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] files in the current directory to Something.dll</span></span>|`vbc -target:library -out:Something.dll *.vb`|  
  
 <span data-ttu-id="845be-116">Lors de la compilation à partir de la ligne de commande, vous devez explicitement référencer le Microsoft [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] bibliothèque d’exécution via le `-reference` option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="845be-116">When compiling from the command line, you must explicitly reference the Microsoft [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] run-time library through the `-reference` compiler option.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="845be-117">Lorsque vous générez un projet à l’aide de l’IDE de Visual Studio, vous pouvez afficher les informations associé **vbc** commande avec les options du compilateur dans la fenêtre Sortie.</span><span class="sxs-lookup"><span data-stu-id="845be-117">When you build a project by using the Visual Studio IDE, you can display information about the associated **vbc** command with its compiler options in the output window.</span></span> <span data-ttu-id="845be-118">Pour afficher ces informations, ouvrez le [boîte de dialogue Options, projets et Solutions, générer et exécuter](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), puis définissez le **détail de sortie de génération du projet MSBuild** à **Normal** ou augmenter le niveau de détail.</span><span class="sxs-lookup"><span data-stu-id="845be-118">To display this information, open the [Options Dialog Box,  Projects and Solutions, Build and Run](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), and then set the **MSBuild project build output verbosity** to **Normal** or a higher level of verbosity.</span></span> <span data-ttu-id="845be-119">Pour plus d’informations, consultez l’article [Comment : afficher, enregistrer et configurer des fichiers journaux de génération](http://msdn.microsoft.com/library/75d38b76-26d6-4f43-bbe7-cbacd7cc81e7).</span><span class="sxs-lookup"><span data-stu-id="845be-119">For more information, see [How to: View, Save, and Configure Build Log Files](http://msdn.microsoft.com/library/75d38b76-26d6-4f43-bbe7-cbacd7cc81e7).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="845be-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="845be-120">See Also</span></span>  
 [<span data-ttu-id="845be-121">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="845be-121">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="845be-122">Compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="845be-122">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
