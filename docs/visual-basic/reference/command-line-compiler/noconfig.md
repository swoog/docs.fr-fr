---
title: -noconfig
ms.date: 03/13/2018
helpviewer_keywords:
- noconfig compiler option [Visual Basic]
- -noconfig compiler option [Visual Basic]
- /noconfig compiler option [Visual Basic]
ms.assetid: a7405067-bd21-4171-adf4-a126fa3ad6c3
ms.openlocfilehash: b707899c845b6b08e008fe229497f682c930044a
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65588844"
---
# <a name="-noconfig"></a><span data-ttu-id="ed8c5-102">-noconfig</span><span class="sxs-lookup"><span data-stu-id="ed8c5-102">-noconfig</span></span>
<span data-ttu-id="ed8c5-103">Spécifie que le compilateur ne doit pas automatiquement référencer les assemblys .NET Framework couramment utilisés ou importer les `System` et `Microsoft.VisualBasic` espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-103">Specifies that the compiler should not automatically reference the commonly used .NET Framework assemblies or import the `System` and `Microsoft.VisualBasic` namespaces.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed8c5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed8c5-104">Syntax</span></span>  
  
```  
-noconfig  
```  
  
## <a name="remarks"></a><span data-ttu-id="ed8c5-105">Notes</span><span class="sxs-lookup"><span data-stu-id="ed8c5-105">Remarks</span></span>  
 <span data-ttu-id="ed8c5-106">Le `-noconfig` option indique au compilateur de ne pas compiler avec le fichier Vbc.rsp, qui se trouve dans le même répertoire que le fichier Vbc.exe.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-106">The `-noconfig` option tells the compiler not to compile with the Vbc.rsp file, which is located in the same directory as the Vbc.exe file.</span></span> <span data-ttu-id="ed8c5-107">Le fichier Vbc.rsp référence les assemblys .NET Framework couramment utilisés et importe le `System` et `Microsoft.VisualBasic` espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-107">The Vbc.rsp file references the commonly used .NET Framework assemblies and imports the `System` and `Microsoft.VisualBasic` namespaces.</span></span> <span data-ttu-id="ed8c5-108">Le compilateur fait implicitement référence à l’assembly System.dll, sauf si le `-nostdlib` option est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-108">The compiler implicitly references the System.dll assembly unless the `-nostdlib` option is specified.</span></span> <span data-ttu-id="ed8c5-109">Le `-nostdlib` option indique au compilateur de ne pas compiler avec Vbc.rsp ou de référencer automatiquement l’assembly System.dll.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-109">The `-nostdlib` option tells the compiler not to compile with Vbc.rsp or automatically reference the System.dll assembly.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ed8c5-110">Les assemblys Mscorlib.dll et de Microsoft.VisualBasic.dll sont toujours référencés.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-110">The Mscorlib.dll and Microsoft.VisualBasic.dll assemblies are always referenced.</span></span>  
  
 <span data-ttu-id="ed8c5-111">Vous pouvez modifier le fichier Vbc.rsp pour spécifier les options de compilateur supplémentaires qui doivent être incluses dans chaque compilation Vbc.exe (sauf lorsque vous spécifiez la `-noconfig` option).</span><span class="sxs-lookup"><span data-stu-id="ed8c5-111">You can modify the Vbc.rsp file to specify additional compiler options that should be included in every Vbc.exe compilation (except when specifying the `-noconfig` option).</span></span> <span data-ttu-id="ed8c5-112">Pour plus d’informations, consultez [@ (Spécifier un fichier réponse)](../../../visual-basic/reference/command-line-compiler/specify-response-file.md).</span><span class="sxs-lookup"><span data-stu-id="ed8c5-112">For more information, see [@ (Specify Response File)](../../../visual-basic/reference/command-line-compiler/specify-response-file.md).</span></span>  
  
 <span data-ttu-id="ed8c5-113">Le compilateur traite les options passées à la `vbc` commande dernière.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-113">The compiler processes the options passed to the `vbc` command last.</span></span> <span data-ttu-id="ed8c5-114">Par conséquent, toute option sur la ligne de commande remplace le paramètre de la même option dans le fichier Vbc.rsp.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-114">Therefore, any option on the command line overrides the setting of the same option in the Vbc.rsp file.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ed8c5-115">Le `-noconfig` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ed8c5-115">The `-noconfig` option is not available from within the Visual Studio development environment; it is available only when compiling from the command line.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed8c5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed8c5-116">See also</span></span>

- [<span data-ttu-id="ed8c5-117">-nostdlib (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ed8c5-117">-nostdlib (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/nostdlib.md)
- [<span data-ttu-id="ed8c5-118">Compilateur de ligne de commande de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ed8c5-118">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)
- [<span data-ttu-id="ed8c5-119">@ (spécifier un fichier réponse)</span><span class="sxs-lookup"><span data-stu-id="ed8c5-119">@ (Specify Response File)</span></span>](../../../visual-basic/reference/command-line-compiler/specify-response-file.md)
- [<span data-ttu-id="ed8c5-120">-référence (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ed8c5-120">-reference (Visual Basic)</span></span>](../../../visual-basic/reference/command-line-compiler/reference.md)
