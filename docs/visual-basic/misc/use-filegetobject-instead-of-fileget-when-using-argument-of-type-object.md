---
title: Utilisez &#39;FileGetObject&#39; au lieu de &#39;FileGet&#39; quand l’argument de type &#39;objet&#39;
ms.date: 07/20/2015
ms.assetid: 090b8088-895a-482a-9362-606596bac304
ms.openlocfilehash: 2edb80f6df95774e0ea5a7b51e57925845d7ba75
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33640415"
---
# <a name="use-39filegetobject39-instead-of-39fileget39-when-using-argument-of-type-39object39"></a><span data-ttu-id="94b0d-102">Utilisez &#39;FileGetObject&#39; au lieu de &#39;FileGet&#39; quand l’argument de type &#39;objet&#39;</span><span class="sxs-lookup"><span data-stu-id="94b0d-102">Use &#39;FileGetObject&#39; instead of &#39;FileGet&#39; when using argument of type &#39;Object&#39;</span></span>
<span data-ttu-id="94b0d-103">La méthode `FileGet` comprend un argument de type `Object`.</span><span class="sxs-lookup"><span data-stu-id="94b0d-103">The `FileGet` method includes an argument of type `Object`.</span></span> <span data-ttu-id="94b0d-104">`FileGetObject` doit être utilisé à la place de `FileGet` pour éviter toute ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="94b0d-104">`FileGetObject` should be used in place of `FileGet` to avoid ambiguities.</span></span>  
  
 <span data-ttu-id="94b0d-105">Notez que les fonctionnalités offertes par `My.Computer.Filesystem` proposent une plus grande facilité d’utilisation et des performances accrues par rapport à `FileGet` ou `FileGetObject`.</span><span class="sxs-lookup"><span data-stu-id="94b0d-105">Notice that the functionality offered by `My.Computer.Filesystem` offers greater ease of use and performance than either `FileGet` or `FileGetObject`.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="94b0d-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="94b0d-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="94b0d-107">Remplacez `FileGet` par `FileGetObject`.</span><span class="sxs-lookup"><span data-stu-id="94b0d-107">Replace `FileGet` with `FileGetObject`.</span></span>  
  
2.  <span data-ttu-id="94b0d-108">Effectuez un cast sur le type de l’argument `Object` pour en faire un type plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="94b0d-108">Cast the `Object` argument to a more specific type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94b0d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94b0d-109">See Also</span></span>  
   
 [<span data-ttu-id="94b0d-110">My.Computer.FileSystem</span><span class="sxs-lookup"><span data-stu-id="94b0d-110">My.Computer.FileSystem</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem)
