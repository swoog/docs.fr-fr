---
title: -utf8output (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- -utf8output compiler option [Visual Basic]
- utf8output compiler option [Visual Basic]
- /utf8output compiler option [Visual Basic]
ms.assetid: 8ab36b1e-027a-49ac-85b4-f48997d9e4d6
ms.openlocfilehash: 753c92cdf2124ee7fb1b471c7bc543b6db6f3daa
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33653583"
---
# <a name="-utf8output-visual-basic"></a><span data-ttu-id="cb59f-102">-utf8output (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cb59f-102">-utf8output (Visual Basic)</span></span>
<span data-ttu-id="cb59f-103">Affiche les résultats de la compilation au format d'encodage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="cb59f-103">Displays compiler output using UTF-8 encoding.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb59f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb59f-104">Syntax</span></span>  
  
```  
-utf8output[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="cb59f-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="cb59f-105">Arguments</span></span>  
 <span data-ttu-id="cb59f-106">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="cb59f-106">`+` &#124; `-`</span></span>  
 <span data-ttu-id="cb59f-107">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="cb59f-107">Optional.</span></span> <span data-ttu-id="cb59f-108">La valeur par défaut de cette option est `-utf8output-`, ce qui signifie que la sortie du compilateur n’utilise pas le codage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="cb59f-108">The default for this option is `-utf8output-`, which means compiler output does not use UTF-8 encoding.</span></span> <span data-ttu-id="cb59f-109">Spécification de `-utf8output` est identique à la spécification `-utf8output+`.</span><span class="sxs-lookup"><span data-stu-id="cb59f-109">Specifying `-utf8output` is the same as specifying `-utf8output+`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cb59f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cb59f-110">Remarks</span></span>  
 <span data-ttu-id="cb59f-111">Dans certaines configurations internationales, sortie du compilateur ne peut pas être affiché correctement dans la console.</span><span class="sxs-lookup"><span data-stu-id="cb59f-111">In some international configurations, compiler output cannot be displayed correctly in the console.</span></span> <span data-ttu-id="cb59f-112">Dans ce cas, utilisez `-utf8output` et rediriger la sortie du compilateur vers un fichier.</span><span class="sxs-lookup"><span data-stu-id="cb59f-112">In such situations, use `-utf8output` and redirect compiler output to a file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cb59f-113">Le `-utf8output` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="cb59f-113">The `-utf8output` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cb59f-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="cb59f-114">Example</span></span>  
 <span data-ttu-id="cb59f-115">Le code suivant compile `In.vb` et indique au compilateur d’afficher de sortie à l’aide du codage UTF-8.</span><span class="sxs-lookup"><span data-stu-id="cb59f-115">The following code compiles `In.vb` and directs the compiler to display output using UTF-8 encoding.</span></span>  
  
```console  
vbc -utf8output in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="cb59f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb59f-116">See Also</span></span>  
 [<span data-ttu-id="cb59f-117">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cb59f-117">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="cb59f-118">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="cb59f-118">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
