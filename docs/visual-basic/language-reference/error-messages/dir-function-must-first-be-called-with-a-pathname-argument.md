---
title: La fonction ’Dir’ doit d’abord être appelée avec un argument ’Pathname’
ms.date: 07/20/2015
f1_keywords:
- vbrDIR_IllegalCall
ms.assetid: 7b5d149f-be91-4ac3-8262-86a360894e7d
ms.openlocfilehash: 1a5d6ed145199ae995a98b6c1180fa3aedf9942c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834155"
---
# <a name="dir-function-must-first-be-called-with-a-pathname-argument"></a><span data-ttu-id="9341a-102">La fonction ’Dir’ doit d’abord être appelée avec un argument ’Pathname’</span><span class="sxs-lookup"><span data-stu-id="9341a-102">'Dir' function must first be called with a 'PathName' argument</span></span>
<span data-ttu-id="9341a-103">Un appel initial à la `Dir` fonction n’inclut pas le `PathName` argument.</span><span class="sxs-lookup"><span data-stu-id="9341a-103">An initial call to the `Dir` function does not include the `PathName` argument.</span></span> <span data-ttu-id="9341a-104">Le premier appel à `Dir` doit inclure un `PathName`, mais les appels suivants à `Dir` n’avez pas besoin d’inclure des paramètres permettant d’extraire l’élément suivant.</span><span class="sxs-lookup"><span data-stu-id="9341a-104">The first call to `Dir` must include a `PathName`, but subsequent calls to `Dir` do not need to include parameters to retrieve the next item.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="9341a-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="9341a-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="9341a-106">Fournir un `PathName` argument dans l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="9341a-106">Supply a `PathName` argument in the function call.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9341a-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9341a-107">See also</span></span>

- <xref:Microsoft.VisualBasic.FileSystem.Dir%2A>
