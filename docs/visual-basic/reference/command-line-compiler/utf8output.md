---
title: -utf8output (Visual Basic)
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- -utf8output compiler option [Visual Basic]
- utf8output compiler option [Visual Basic]
- /utf8output compiler option [Visual Basic]
ms.assetid: 8ab36b1e-027a-49ac-85b4-f48997d9e4d6
caps.latest.revision: ''
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 97f90b39046aebe0cd15c7e033d8e588045491f7
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="-utf8output-visual-basic"></a><span data-ttu-id="7bcf4-102">-utf8output (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7bcf4-102">-utf8output (Visual Basic)</span></span>
<span data-ttu-id="7bcf4-103">Affiche les résultats de la compilation au format d'encodage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-103">Displays compiler output using UTF-8 encoding.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7bcf4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bcf4-104">Syntax</span></span>  
  
```  
-utf8output[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="7bcf4-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="7bcf4-105">Arguments</span></span>  
 <span data-ttu-id="7bcf4-106">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="7bcf4-106">`+` &#124; `-`</span></span>  
 <span data-ttu-id="7bcf4-107">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-107">Optional.</span></span> <span data-ttu-id="7bcf4-108">La valeur par défaut de cette option est `-utf8output-`, ce qui signifie que la sortie du compilateur n’utilise pas le codage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-108">The default for this option is `-utf8output-`, which means compiler output does not use UTF-8 encoding.</span></span> <span data-ttu-id="7bcf4-109">Spécification de `-utf8output` est identique à la spécification `-utf8output+`.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-109">Specifying `-utf8output` is the same as specifying `-utf8output+`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7bcf4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7bcf4-110">Remarks</span></span>  
 <span data-ttu-id="7bcf4-111">Dans certaines configurations internationales, sortie du compilateur ne peut pas être affiché correctement dans la console.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-111">In some international configurations, compiler output cannot be displayed correctly in the console.</span></span> <span data-ttu-id="7bcf4-112">Dans ce cas, utilisez `-utf8output` et rediriger la sortie du compilateur vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-112">In such situations, use `-utf8output` and redirect compiler output to a file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7bcf4-113">Le `-utf8output` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-113">The `-utf8output` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7bcf4-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="7bcf4-114">Example</span></span>  
 <span data-ttu-id="7bcf4-115">Le code suivant compile `In.vb` et indique au compilateur d’afficher de sortie à l’aide du codage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="7bcf4-115">The following code compiles `In.vb` and directs the compiler to display output using UTF-8 encoding.</span></span>  
  
```console  
vbc -utf8output in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="7bcf4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bcf4-116">See Also</span></span>  
 [<span data-ttu-id="7bcf4-117">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7bcf4-117">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="7bcf4-118">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="7bcf4-118">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
