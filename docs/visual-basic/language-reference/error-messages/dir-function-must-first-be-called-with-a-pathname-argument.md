---
title: '&#39;Dir&#39; fonction doit d’abord être appelée avec un &#39;PathName&#39; argument'
ms.date: 07/20/2015
f1_keywords:
- vbrDIR_IllegalCall
ms.assetid: 7b5d149f-be91-4ac3-8262-86a360894e7d
ms.openlocfilehash: f7e9ef9cc6309f24ae9f8963e910b41180c029b7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54518486"
---
# <a name="39dir39-function-must-first-be-called-with-a-39pathname39-argument"></a><span data-ttu-id="210b0-102">&#39;Dir&#39; fonction doit d’abord être appelée avec un &#39;PathName&#39; argument</span><span class="sxs-lookup"><span data-stu-id="210b0-102">&#39;Dir&#39; function must first be called with a &#39;PathName&#39; argument</span></span>
<span data-ttu-id="210b0-103">Un appel initial à la `Dir` fonction n’inclut pas le `PathName` argument.</span><span class="sxs-lookup"><span data-stu-id="210b0-103">An initial call to the `Dir` function does not include the `PathName` argument.</span></span> <span data-ttu-id="210b0-104">Le premier appel à `Dir` doit inclure un `PathName`, mais les appels suivants à `Dir` n’avez pas besoin d’inclure des paramètres permettant d’extraire l’élément suivant.</span><span class="sxs-lookup"><span data-stu-id="210b0-104">The first call to `Dir` must include a `PathName`, but subsequent calls to `Dir` do not need to include parameters to retrieve the next item.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="210b0-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="210b0-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="210b0-106">Fournir un `PathName` argument dans l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="210b0-106">Supply a `PathName` argument in the function call.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="210b0-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="210b0-107">See also</span></span>
- <xref:Microsoft.VisualBasic.FileSystem.Dir%2A>
