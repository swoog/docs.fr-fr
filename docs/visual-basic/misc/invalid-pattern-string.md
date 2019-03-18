---
title: Chaîne de modèle non valide
ms.date: 07/20/2015
ms.assetid: ec1aecdb-5339-4a93-be71-eec56b1d7438
ms.openlocfilehash: bc2e91060ca1b0e21ea28b0f08febc3e0c54f4f1
ms.sourcegitcommit: 5c1abeec15fbddcc7dbaa729fabc1f1f29f12045
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58027309"
---
# <a name="invalid-pattern-string"></a><span data-ttu-id="577b0-102">Chaîne de modèle non valide</span><span class="sxs-lookup"><span data-stu-id="577b0-102">Invalid pattern string</span></span>
<span data-ttu-id="577b0-103">La chaîne de modèle spécifiée dans l’opération `Like` d’une recherche n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="577b0-103">The pattern string specified in the `Like` operation of a search is invalid.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="577b0-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="577b0-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="577b0-105">Examinez les caractères valides des expressions de liste.</span><span class="sxs-lookup"><span data-stu-id="577b0-105">Review the valid characters for list expressions.</span></span>  
  
2.  <span data-ttu-id="577b0-106">Dans la plage de modèles, vérifiez que le caractère de début de plage est inférieur au caractère de fin de plage, comme dans `[a-z]`.</span><span class="sxs-lookup"><span data-stu-id="577b0-106">In the pattern range, ensure that the start range character is less than the end range character, as in `[a-z]`.</span></span>  
  
3.  <span data-ttu-id="577b0-107">Dans la plage de modèles, vérifiez que plusieurs traits d’union ne se situent pas les uns à côté des autres, comme dans `[a--z]`.</span><span class="sxs-lookup"><span data-stu-id="577b0-107">In the pattern range, ensure that there are not multiple hyphens next to each other, as in `[a--z]`.</span></span>  
  
4.  <span data-ttu-id="577b0-108">Terminez les plages de modèles par un crochet fermant.</span><span class="sxs-lookup"><span data-stu-id="577b0-108">End pattern ranges with a closing bracket.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="577b0-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="577b0-109">See also</span></span>

- [<span data-ttu-id="577b0-110">Like (opérateur)</span><span class="sxs-lookup"><span data-stu-id="577b0-110">Like Operator</span></span>](../../visual-basic/language-reference/operators/like-operator.md)
