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
ms.openlocfilehash: 89bcd6e0e7c1cc867bf853dc9bbe96628942ace2
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44078935"
---
# <a name="building-from-the-command-line-visual-basic"></a><span data-ttu-id="9b1a0-102">Génération à partir de la ligne de commande (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9b1a0-102">Building from the Command Line (Visual Basic)</span></span>
<span data-ttu-id="9b1a0-103">Un projet Visual Basic se compose d’un ou plusieurs fichiers sources séparés.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-103">A Visual Basic project is made up of one or more separate source files.</span></span> <span data-ttu-id="9b1a0-104">Pendant le processus appelé compilation, ces fichiers sont regroupés en un seul package, un seul fichier exécutable qui peut être exécuté en tant qu’application.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-104">During the process known as compilation, these files are brought together into one package—a single executable file that can be run as an application.</span></span>  
  
 <span data-ttu-id="9b1a0-105">Visual Basic fournit un compilateur de ligne de commande comme alternative aux programmes de compilation dans l’environnement de développement intégré (IDE) Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-105">Visual Basic provides a command-line compiler as an alternative to compiling programs from within the Visual Studio integrated development environment (IDE).</span></span> <span data-ttu-id="9b1a0-106">Le compilateur de ligne de commande est conçu pour les situations dans lequel vous n’avez pas besoin l’ensemble complet des fonctionnalités de l’IDE, par exemple, lorsque vous utilisez ou écriture pour les ordinateurs avec un espace de stockage ou mémoire limitées sur le système.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-106">The command-line compiler is designed for situations in which you do not require the full set of features in the IDE—for example, when you are using or writing for computers with limited system memory or storage space.</span></span>  
  
  <span data-ttu-id="9b1a0-107">Pour compiler des fichiers sources à partir de l’IDE de Visual Studio, choisissez le **Build** commande à partir de la **Build** menu.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-107">To compile source files from within the Visual Studio IDE, choose the **Build** command from the **Build** menu.</span></span>  
  
> [!TIP]
>  <span data-ttu-id="9b1a0-108">Lorsque vous générez des fichiers projet à l’aide de l’IDE Visual Studio, vous pouvez afficher des informations sur associé **vbc** commande et ses commutateurs dans la fenêtre Sortie.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-108">When you build project files by using the Visual Studio IDE, you can display information about the associated **vbc** command and its switches in the output window.</span></span> <span data-ttu-id="9b1a0-109">Pour afficher ces informations, ouvrez le [boîte de dialogue Options, projets et Solutions, générer et exécuter](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), puis définissez le **niveau de détail de sortie de génération de projet MSBuild** à **Normal** ou un niveau plus élevé de commentaires.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-109">To display this information, open the [Options Dialog Box,  Projects and Solutions, Build and Run](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), and then set the **MSBuild project build output verbosity** to **Normal** or a higher level of verbosity.</span></span> <span data-ttu-id="9b1a0-110">Pour plus d’informations, consultez l’article [Comment : afficher, enregistrer et configurer des fichiers journaux de génération](https://msdn.microsoft.com/library/75d38b76-26d6-4f43-bbe7-cbacd7cc81e7).</span><span class="sxs-lookup"><span data-stu-id="9b1a0-110">For more information, see [How to: View, Save, and Configure Build Log Files](https://msdn.microsoft.com/library/75d38b76-26d6-4f43-bbe7-cbacd7cc81e7).</span></span>  
  
 <span data-ttu-id="9b1a0-111">Vous pouvez compiler des fichiers projet (.vbproj) à une invite de commandes à l’aide de MSBuild.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-111">You can compile project (.vbproj) files at a command prompt by using MSBuild.</span></span> <span data-ttu-id="9b1a0-112">Pour plus d’informations, consultez [de ligne de commande référence](/visualstudio/msbuild/msbuild-command-line-reference) et [procédure pas à pas : utilisation de MSBuild](/visualstudio/msbuild/walkthrough-using-msbuild).</span><span class="sxs-lookup"><span data-stu-id="9b1a0-112">For more information, see [Command-Line Reference](/visualstudio/msbuild/msbuild-command-line-reference) and [Walkthrough: Using MSBuild](/visualstudio/msbuild/walkthrough-using-msbuild).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9b1a0-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9b1a0-113">In This Section</span></span>  
 [<span data-ttu-id="9b1a0-114">Guide pratique : appeler le compilateur de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="9b1a0-114">How to: Invoke the Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/how-to-invoke-the-command-line-compiler.md)  
 <span data-ttu-id="9b1a0-115">Décrit comment appeler le compilateur de ligne de commande à l’invite de MS-DOS ou à partir d’un sous-répertoire spécifique.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-115">Describes how to invoke the command-line compiler at the MS-DOS prompt or from a specific subdirectory.</span></span>  
  
 [<span data-ttu-id="9b1a0-116">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="9b1a0-116">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 <span data-ttu-id="9b1a0-117">Fournit une liste d’exemples de lignes de commande que vous pouvez modifier pour votre usage personnel.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-117">Provides a list of sample command lines that you can modify for your own use.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="9b1a0-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b1a0-118">Related Sections</span></span>  
 [<span data-ttu-id="9b1a0-119">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9b1a0-119">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 <span data-ttu-id="9b1a0-120">Fournit des listes d’options du compilateur, organisées par ordre alphabétique ou par objet.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-120">Provides lists of compiler options, organized alphabetically or by purpose.</span></span>  
  
 [<span data-ttu-id="9b1a0-121">Compilation conditionnelle</span><span class="sxs-lookup"><span data-stu-id="9b1a0-121">Conditional Compilation</span></span>](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)  
 <span data-ttu-id="9b1a0-122">Décrit comment compiler des sections de code.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-122">Describes how to compile particular sections of code.</span></span>  
  
 [<span data-ttu-id="9b1a0-123">Génération et nettoyage de solutions et de projets dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9b1a0-123">Building and Cleaning Projects and Solutions in Visual Studio</span></span>](/visualstudio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio)  
 <span data-ttu-id="9b1a0-124">Décrit comment organiser ce que sera inclus dans les différentes versions, choisissez Propriétés du projet et vous assurer que les projets sont générés dans le bon ordre.</span><span class="sxs-lookup"><span data-stu-id="9b1a0-124">Describes how to organize what will be included in different builds, choose project properties, and ensure that projects build in the correct order.</span></span>
