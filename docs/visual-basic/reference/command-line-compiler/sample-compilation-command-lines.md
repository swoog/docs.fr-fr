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
ms.openlocfilehash: 601f8f3a5ea86da060b2d26796b2299d87946443
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54547798"
---
# <a name="sample-compilation-command-lines-visual-basic"></a><span data-ttu-id="35be8-102">Exemples de lignes de commande de compilation (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="35be8-102">Sample compilation command lines (Visual Basic)</span></span>
<span data-ttu-id="35be8-103">Comme alternative à compiler les programmes Visual Basic dans Visual Studio, vous pouvez compiler à partir de la ligne de commande pour produire des fichiers exécutables (.exe) ou des fichiers de bibliothèque de liens dynamiques (.dll).</span><span class="sxs-lookup"><span data-stu-id="35be8-103">As an alternative to compiling Visual Basic programs from within Visual Studio, you can compile from the command line to produce executable (.exe) files or dynamic-link library (.dll) files.</span></span>  
  
 <span data-ttu-id="35be8-104">Le compilateur de ligne de commande Visual Basic prend en charge un ensemble complet des options qui contrôlent l’entrée et sortie de fichiers, assemblys, débogage et des options de préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="35be8-104">The Visual Basic command-line compiler supports a complete set of options that control input and output files, assemblies, and debug and preprocessor options.</span></span> <span data-ttu-id="35be8-105">Chaque option est disponible sous deux formes interchangeables : `-option` et `/option`.</span><span class="sxs-lookup"><span data-stu-id="35be8-105">Each option is available in two interchangeable forms: `-option` and `/option`.</span></span> <span data-ttu-id="35be8-106">Cette documentation présente uniquement le `-option` formulaire.</span><span class="sxs-lookup"><span data-stu-id="35be8-106">This documentation shows only the `-option` form.</span></span>  
  
 <span data-ttu-id="35be8-107">Le tableau suivant répertorie certains exemples de lignes de commande que vous pouvez modifier pour votre usage personnel.</span><span class="sxs-lookup"><span data-stu-id="35be8-107">The following table lists some sample command lines you can modify for your own use.</span></span>  
  
|<span data-ttu-id="35be8-108">À</span><span class="sxs-lookup"><span data-stu-id="35be8-108">To</span></span>|<span data-ttu-id="35be8-109">Utilisez</span><span class="sxs-lookup"><span data-stu-id="35be8-109">Use</span></span>|  
|--------|---------|  
|<span data-ttu-id="35be8-110">Compilez le fichier.vb et créer File.exe</span><span class="sxs-lookup"><span data-stu-id="35be8-110">Compile File.vb and create File.exe</span></span>|`vbc -reference:Microsoft.VisualBasic.dll File.vb`|  
|<span data-ttu-id="35be8-111">Compilez le fichier.vb et créer File.dll</span><span class="sxs-lookup"><span data-stu-id="35be8-111">Compile File.vb and create File.dll</span></span>|`vbc -target:library File.vb`|  
|<span data-ttu-id="35be8-112">Compilez le fichier.vb et créer My.exe</span><span class="sxs-lookup"><span data-stu-id="35be8-112">Compile File.vb and create My.exe</span></span>|`vbc -out:My.exe File.vb`|  
|<span data-ttu-id="35be8-113">Compilez le fichier.vb et créer une bibliothèque et un assembly de référence nommé File.dll</span><span class="sxs-lookup"><span data-stu-id="35be8-113">Compile File.vb and create both a library and a reference assembly named File.dll</span></span>|`vbc -target:library -ref:.\debug\bin\ref\file.dll File.vb`|
|<span data-ttu-id="35be8-114">Compilez tous les fichiers Visual Basic dans le répertoire actif, avec les optimisations sur et `DEBUG` symbole, produire File2.exe</span><span class="sxs-lookup"><span data-stu-id="35be8-114">Compile all Visual Basic files in the current directory, with optimizations on and the `DEBUG` symbol defined, producing File2.exe</span></span>|`vbc -define:DEBUG=1 -optimize -out:File2.exe *.vb`|  
|<span data-ttu-id="35be8-115">Compiler tous les fichiers Visual Basic dans le répertoire actif, produisant une version debug de File2.dll sans afficher le logo ou les avertissements</span><span class="sxs-lookup"><span data-stu-id="35be8-115">Compile all Visual Basic files in the current directory, producing a debug version of File2.dll without displaying the logo or warnings</span></span>|`vbc -target:library -out:File2.dll -nowarn -nologo -debug *.vb`|  
|<span data-ttu-id="35be8-116">Compiler tous les fichiers Visual Basic dans le répertoire actif en Something.dll</span><span class="sxs-lookup"><span data-stu-id="35be8-116">Compile all Visual Basic files in the current directory to Something.dll</span></span>|`vbc -target:library -out:Something.dll *.vb`|  
  
> [!TIP]
>  <span data-ttu-id="35be8-117">Lorsque vous générez un projet à l’aide de l’IDE Visual Studio, vous pouvez afficher des informations sur associé **vbc** commande avec ses options du compilateur dans la fenêtre Sortie.</span><span class="sxs-lookup"><span data-stu-id="35be8-117">When you build a project by using the Visual Studio IDE, you can display information about the associated **vbc** command with its compiler options in the output window.</span></span> <span data-ttu-id="35be8-118">Pour afficher ces informations, ouvrez le [boîte de dialogue Options, projets et Solutions, générer et exécuter](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), puis définissez le **niveau de détail de sortie de génération de projet MSBuild** à **Normal** ou un niveau plus élevé de commentaires.</span><span class="sxs-lookup"><span data-stu-id="35be8-118">To display this information, open the [Options Dialog Box,  Projects and Solutions, Build and Run](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), and then set the **MSBuild project build output verbosity** to **Normal** or a higher level of verbosity.</span></span>   
  
## <a name="see-also"></a><span data-ttu-id="35be8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35be8-119">See also</span></span>
- [<span data-ttu-id="35be8-120">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="35be8-120">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="35be8-121">Compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="35be8-121">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
