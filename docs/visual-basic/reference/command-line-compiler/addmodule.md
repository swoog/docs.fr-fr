---
title: -addmodule
ms.date: 03/09/2018
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- /addmodule compiler option [Visual Basic]
- addmodule compiler option [Visual Basic]
- -addmodule compiler option [Visual Basic]
ms.assetid: fb4b89d4-4926-4f20-868d-427fa28497b2
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: c17d5541fe2d02ba88f4c5ef259b2248f371dfe5
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-addmodule"></a><span data-ttu-id="bf943-102">-addmodule</span><span class="sxs-lookup"><span data-stu-id="bf943-102">-addmodule</span></span>
<span data-ttu-id="bf943-103">Entraîne la mise à disposition par le compilateur de toutes les informations de type à partir du ou des fichiers spécifiés, pour le projet en cours de compilation.</span><span class="sxs-lookup"><span data-stu-id="bf943-103">Causes the compiler to make all type information from the specified file(s) available to the project you are currently compiling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bf943-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf943-104">Syntax</span></span>  
  
```  
-addmodule:fileList  
```  
  
## <a name="arguments"></a><span data-ttu-id="bf943-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="bf943-105">Arguments</span></span>  
 `fileList`  
 <span data-ttu-id="bf943-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bf943-106">Required.</span></span> <span data-ttu-id="bf943-107">Délimitée par des virgules de liste de fichiers qui contiennent des métadonnées, mais ne contiennent pas de manifestes d’assembly.</span><span class="sxs-lookup"><span data-stu-id="bf943-107">Comma-delimited list of files that contain metadata but do not contain assembly manifests.</span></span> <span data-ttu-id="bf943-108">Les noms de fichiers contenant des espaces doivent être entourés de guillemets (« »).</span><span class="sxs-lookup"><span data-stu-id="bf943-108">File names containing spaces should be surrounded by quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bf943-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bf943-109">Remarks</span></span>  
 <span data-ttu-id="bf943-110">Les fichiers répertoriés par le `fileList` paramètre doit être créé avec la `-target:module` option, ou avec l’équivalent d’un autre compilateur `-target:module`.</span><span class="sxs-lookup"><span data-stu-id="bf943-110">The files listed by the `fileList` parameter must be created with the `-target:module` option, or with another compiler's equivalent to `-target:module`.</span></span>  
  
 <span data-ttu-id="bf943-111">Tous les modules ajoutés avec `-addmodule` doivent être dans le même répertoire que le fichier de sortie au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bf943-111">All modules added with `-addmodule` must be in the same directory as the output file at run time.</span></span> <span data-ttu-id="bf943-112">Autrement dit, vous pouvez spécifier un module dans n’importe quel répertoire au moment de la compilation, mais le module doit être dans le répertoire de l’application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="bf943-112">That is, you can specify a module in any directory at compile time, but the module must be in the application directory at run time.</span></span> <span data-ttu-id="bf943-113">Si elle n’est pas le cas, vous obtenez un <xref:System.TypeLoadException> erreur.</span><span class="sxs-lookup"><span data-stu-id="bf943-113">If it is not, you get a <xref:System.TypeLoadException> error.</span></span>  
  
 <span data-ttu-id="bf943-114">Si vous spécifiez (implicitement ou explicitement) n’importe quel[-cible (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md) option autre que `-target:module` avec `-addmodule`, les fichiers que vous passez à `-addmodule` font partie de l’assembly du projet.</span><span class="sxs-lookup"><span data-stu-id="bf943-114">If you specify (implicitly or explicitly) any[-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md) option other than `-target:module` with `-addmodule`, the files you pass to `-addmodule` become part of the project's assembly.</span></span> <span data-ttu-id="bf943-115">Un assembly est requis pour exécuter un fichier de sortie qui contient un ou plusieurs fichiers ajoutés avec `-addmodule`.</span><span class="sxs-lookup"><span data-stu-id="bf943-115">An assembly is required to run an output file that has one or more files added with `-addmodule`.</span></span>  
  
 <span data-ttu-id="bf943-116">Utilisez [/reference (Visual Basic)](../../../visual-basic/reference/command-line-compiler/reference.md) pour importer des métadonnées à partir d’un fichier qui contient un assembly.</span><span class="sxs-lookup"><span data-stu-id="bf943-116">Use [/reference (Visual Basic)](../../../visual-basic/reference/command-line-compiler/reference.md) to import metadata from a file that contains an assembly.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bf943-117">Le `-addmodule` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="bf943-117">The `-addmodule` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bf943-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="bf943-118">Example</span></span>  
 <span data-ttu-id="bf943-119">Le code suivant crée un module.</span><span class="sxs-lookup"><span data-stu-id="bf943-119">The following code creates a module.</span></span>  
  
 [!code-vb[VbVbalrCompiler#47](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/addmodule_1.vb)]  
  
 <span data-ttu-id="bf943-120">Le code suivant importe les types du module.</span><span class="sxs-lookup"><span data-stu-id="bf943-120">The following code imports the module's types.</span></span>  
  
 [!code-vb[VbVbalrCompiler#48](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/addmodule_2.vb)]  
  
 <span data-ttu-id="bf943-121">Lorsque vous exécutez `t1`, elle génère `802`.</span><span class="sxs-lookup"><span data-stu-id="bf943-121">When you run `t1`, it outputs `802`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf943-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf943-122">See Also</span></span>  
 [<span data-ttu-id="bf943-123">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bf943-123">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="bf943-124">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bf943-124">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)  
 [<span data-ttu-id="bf943-125">-référence (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="bf943-125">-reference (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/reference.md)  
 [<span data-ttu-id="bf943-126">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="bf943-126">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
