---
title: Dépassement de capacité (erreur d'exécution Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrERRID_Overflow
ms.assetid: c6a23279-3086-412a-bcff-ff8ed2cb8c6f
ms.openlocfilehash: 9db79071c4895d49680352bde2d0824a3756d941
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33594173"
---
# <a name="overflow-visual-basic-run-time-error"></a><span data-ttu-id="4b06d-102">Dépassement de capacité (erreur d'exécution Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4b06d-102">Overflow (Visual Basic Run-Time Error)</span></span>
<span data-ttu-id="4b06d-103">Un dépassement de capacité se produit lorsque vous essayez d’une assignation qui dépasse les limites de la cible de l’affectation.</span><span class="sxs-lookup"><span data-stu-id="4b06d-103">An overflow results when you attempt an assignment that exceeds the limits of the assignment's target.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="4b06d-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="4b06d-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="4b06d-105">Assurez-vous que les résultats de type de données, des calculs et des affectations de conversions ne sont pas trop grande pour être représentée dans la plage de variables autorisées pour ce type de valeur et affectez la valeur à une variable d’un type qui peuvent contenir une plus grande plage de valeurs , si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="4b06d-105">Make sure that results of assignments, calculations, and data type conversions are not too large to be represented within the range of variables allowed for that type of value, and assign the value to a variable of a type that can hold a larger range of values, if necessary.</span></span>  
  
2.  <span data-ttu-id="4b06d-106">Assurez-vous que les affectations aux propriétés correspondent à la plage de la propriété à laquelle elles ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="4b06d-106">Make sure assignments to properties fit the range of the property to which they are made.</span></span>  
  
3.  <span data-ttu-id="4b06d-107">Assurez-vous que les nombres utilisés dans les calculs sont convertis en entiers n’ont pas de résultats supérieurs aux entiers.</span><span class="sxs-lookup"><span data-stu-id="4b06d-107">Make sure that numbers used in calculations that are coerced into integers do not have results larger than integers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b06d-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b06d-108">See Also</span></span>  
 <xref:System.Int32.MaxValue?displayProperty=nameWithType>  
 <xref:System.Double.MaxValue?displayProperty=nameWithType>  
 [<span data-ttu-id="4b06d-109">Types de données</span><span class="sxs-lookup"><span data-stu-id="4b06d-109">Data Types</span></span>](../../../visual-basic/language-reference/data-types/data-type-summary.md)  
 [<span data-ttu-id="4b06d-110">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="4b06d-110">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
