---
title: -addmodule
ms.date: 03/09/2018
helpviewer_keywords:
- /addmodule compiler option [Visual Basic]
- addmodule compiler option [Visual Basic]
- -addmodule compiler option [Visual Basic]
ms.assetid: fb4b89d4-4926-4f20-868d-427fa28497b2
ms.openlocfilehash: 3e5c94cce8b16649854050855800ac1bf2fc6572
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580575"
---
# <a name="-addmodule"></a><span data-ttu-id="58685-102">-addmodule</span><span class="sxs-lookup"><span data-stu-id="58685-102">-addmodule</span></span>
<span data-ttu-id="58685-103">Entraîne la mise à disposition par le compilateur de toutes les informations de type à partir du ou des fichiers spécifiés, pour le projet en cours de compilation.</span><span class="sxs-lookup"><span data-stu-id="58685-103">Causes the compiler to make all type information from the specified file(s) available to the project you are currently compiling.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58685-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58685-104">Syntax</span></span>  
  
```  
-addmodule:fileList  
```  
  
## <a name="arguments"></a><span data-ttu-id="58685-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="58685-105">Arguments</span></span>  
 `fileList`  
 <span data-ttu-id="58685-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="58685-106">Required.</span></span> <span data-ttu-id="58685-107">Liste délimitée par des virgules des fichiers qui contiennent des métadonnées, mais ne contiennent pas de manifestes d’assembly.</span><span class="sxs-lookup"><span data-stu-id="58685-107">Comma-delimited list of files that contain metadata but do not contain assembly manifests.</span></span> <span data-ttu-id="58685-108">Les noms de fichiers contenant des espaces doivent être entourés de guillemets ( » «).</span><span class="sxs-lookup"><span data-stu-id="58685-108">File names containing spaces should be surrounded by quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="58685-109">Notes</span><span class="sxs-lookup"><span data-stu-id="58685-109">Remarks</span></span>  
 <span data-ttu-id="58685-110">Les fichiers répertoriés par le `fileList` paramètre doit être créé avec le `-target:module` option, ou avec l’équivalent d’un autre compilateur `-target:module`.</span><span class="sxs-lookup"><span data-stu-id="58685-110">The files listed by the `fileList` parameter must be created with the `-target:module` option, or with another compiler's equivalent to `-target:module`.</span></span>  
  
 <span data-ttu-id="58685-111">Tous les modules ajoutés par `-addmodule` doit être dans le même répertoire que le fichier de sortie au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="58685-111">All modules added with `-addmodule` must be in the same directory as the output file at run time.</span></span> <span data-ttu-id="58685-112">Autrement dit, vous pouvez spécifier un module dans n’importe quel répertoire au moment de la compilation, mais le module doit être dans le répertoire de l’application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="58685-112">That is, you can specify a module in any directory at compile time, but the module must be in the application directory at run time.</span></span> <span data-ttu-id="58685-113">Si elle n’est pas le cas, vous obtenez un <xref:System.TypeLoadException> erreur.</span><span class="sxs-lookup"><span data-stu-id="58685-113">If it is not, you get a <xref:System.TypeLoadException> error.</span></span>  
  
 <span data-ttu-id="58685-114">Si vous spécifiez (implicitement ou explicitement) n’importe quel[-cible (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md) option autre que `-target:module` avec `-addmodule`, les fichiers que vous transmettez à `-addmodule` deviennent partie intégrante de l’assembly du projet.</span><span class="sxs-lookup"><span data-stu-id="58685-114">If you specify (implicitly or explicitly) any[-target (Visual Basic)](../../../visual-basic/reference/command-line-compiler/target.md) option other than `-target:module` with `-addmodule`, the files you pass to `-addmodule` become part of the project's assembly.</span></span> <span data-ttu-id="58685-115">Un assembly est requis pour exécuter un fichier de sortie qui contient un ou plusieurs fichiers ajoutés avec `-addmodule`.</span><span class="sxs-lookup"><span data-stu-id="58685-115">An assembly is required to run an output file that has one or more files added with `-addmodule`.</span></span>  
  
 <span data-ttu-id="58685-116">Utilisez [/reference (Visual Basic)](../../../visual-basic/reference/command-line-compiler/reference.md) pour importer les métadonnées à partir d’un fichier qui contient un assembly.</span><span class="sxs-lookup"><span data-stu-id="58685-116">Use [/reference (Visual Basic)](../../../visual-basic/reference/command-line-compiler/reference.md) to import metadata from a file that contains an assembly.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="58685-117">Le `-addmodule` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="58685-117">The `-addmodule` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="58685-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="58685-118">Example</span></span>  
 <span data-ttu-id="58685-119">Le code suivant crée un module.</span><span class="sxs-lookup"><span data-stu-id="58685-119">The following code creates a module.</span></span>  
  
 [!code-vb[VbVbalrCompiler#47](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/addmodule_1.vb)]  
  
 <span data-ttu-id="58685-120">Le code suivant importe les types du module.</span><span class="sxs-lookup"><span data-stu-id="58685-120">The following code imports the module's types.</span></span>  
  
 [!code-vb[VbVbalrCompiler#48](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/addmodule_2.vb)]  
  
 <span data-ttu-id="58685-121">Lorsque vous exécutez `t1`, elle génère `802`.</span><span class="sxs-lookup"><span data-stu-id="58685-121">When you run `t1`, it outputs `802`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58685-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58685-122">See also</span></span>
- [<span data-ttu-id="58685-123">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="58685-123">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="58685-124">-target (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="58685-124">-target (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/target.md)
- [<span data-ttu-id="58685-125">-référence (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="58685-125">-reference (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/reference.md)
- [<span data-ttu-id="58685-126">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="58685-126">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
