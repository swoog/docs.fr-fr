---
title: -verbose
ms.date: 03/13/2018
helpviewer_keywords:
- verbose compiler option [Visual Basic]
- -verbose compiler option [Visual Basic]
- /verbose compiler option [Visual Basic]
ms.assetid: d1aec0c1-0261-421d-9adc-5b13756100be
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a5f257fce67d8e348b69404411c12ded785cfd68
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33652127"
---
# <a name="-verbose"></a><span data-ttu-id="376b9-102">-verbose</span><span class="sxs-lookup"><span data-stu-id="376b9-102">-verbose</span></span>
<span data-ttu-id="376b9-103">Indique au compilateur générer des messages d’état et d’erreur détaillés.</span><span class="sxs-lookup"><span data-stu-id="376b9-103">Causes the compiler to produce verbose status and error messages.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="376b9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="376b9-104">Syntax</span></span>  
  
```  
-verbose[+ | -]  
```  
  
## <a name="arguments"></a><span data-ttu-id="376b9-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="376b9-105">Arguments</span></span>  
 <span data-ttu-id="376b9-106">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="376b9-106">`+` &#124; `-`</span></span>  
 <span data-ttu-id="376b9-107">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="376b9-107">Optional.</span></span> <span data-ttu-id="376b9-108">Spécification de `-verbose` est identique à la spécification `-verbose+`, ce qui entraîne le compilateur à émettre des messages détaillés.</span><span class="sxs-lookup"><span data-stu-id="376b9-108">Specifying `-verbose` is the same as specifying `-verbose+`, which causes the compiler to emit verbose messages.</span></span> <span data-ttu-id="376b9-109">La valeur par défaut de cette option est `-verbose-`.</span><span class="sxs-lookup"><span data-stu-id="376b9-109">The default for this option is `-verbose-`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="376b9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="376b9-110">Remarks</span></span>  
 <span data-ttu-id="376b9-111">Le `-verbose` option affiche des informations sur le nombre total d’erreurs émises par le compilateur, signale les assemblys chargés par un module et affiche les fichiers qui sont en cours de compilation.</span><span class="sxs-lookup"><span data-stu-id="376b9-111">The `-verbose` option displays information about the total number of errors issued by the compiler, reports which assemblies are being loaded by a module, and displays which files are currently being compiled.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="376b9-112">Le `-verbose` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="376b9-112">The `-verbose` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="376b9-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="376b9-113">Example</span></span>  
 <span data-ttu-id="376b9-114">Le code suivant compile `In.vb` et indique au compilateur d’afficher des informations d’état détaillées.</span><span class="sxs-lookup"><span data-stu-id="376b9-114">The following code compiles `In.vb` and directs the compiler to display verbose status information.</span></span>  
  
```console  
vbc -verbose in.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="376b9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="376b9-115">See Also</span></span>  
 [<span data-ttu-id="376b9-116">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="376b9-116">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="376b9-117">Exemples de lignes de commande de compilation</span><span class="sxs-lookup"><span data-stu-id="376b9-117">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
