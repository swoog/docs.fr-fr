---
title: Dépassement de capacité (erreur d'exécution Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrERRID_Overflow
ms.assetid: c6a23279-3086-412a-bcff-ff8ed2cb8c6f
ms.openlocfilehash: 7546676b85465577b357b7ad0757b4db8d40dbe3
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42934437"
---
# <a name="overflow-visual-basic-run-time-error"></a><span data-ttu-id="46db2-102">Dépassement de capacité (erreur d'exécution Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="46db2-102">Overflow (Visual Basic Run-Time Error)</span></span>
<span data-ttu-id="46db2-103">Un dépassement de capacité se produit lorsque vous essayez d’une assignation qui dépasse les limites de la cible de l’assignation.</span><span class="sxs-lookup"><span data-stu-id="46db2-103">An overflow results when you attempt an assignment that exceeds the limits of the assignment's target.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="46db2-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="46db2-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="46db2-105">Assurez-vous que les résultats de type de données, des calculs et des attributions de conversions ne sont pas trop grand pour être représenté dans la plage de variables autorisées pour ce type de valeur et affectez la valeur à une variable d’un type qui peuvent contenir un grand nombre de valeurs , si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="46db2-105">Make sure that results of assignments, calculations, and data type conversions are not too large to be represented within the range of variables allowed for that type of value, and assign the value to a variable of a type that can hold a larger range of values, if necessary.</span></span>  
  
2.  <span data-ttu-id="46db2-106">Assurez-vous que les affectations aux propriétés correspondent à la plage de la propriété à laquelle elles ont été effectuées.</span><span class="sxs-lookup"><span data-stu-id="46db2-106">Make sure assignments to properties fit the range of the property to which they are made.</span></span>  
  
3.  <span data-ttu-id="46db2-107">Assurez-vous que les numéros utilisés dans les calculs sont convertis en entiers n’ont pas de résultats supérieurs aux entiers.</span><span class="sxs-lookup"><span data-stu-id="46db2-107">Make sure that numbers used in calculations that are coerced into integers do not have results larger than integers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46db2-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46db2-108">See Also</span></span>  
 <xref:System.Int32.MaxValue?displayProperty=nameWithType>  
 <xref:System.Double.MaxValue?displayProperty=nameWithType>  
 [<span data-ttu-id="46db2-109">Types de données</span><span class="sxs-lookup"><span data-stu-id="46db2-109">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)  
 [<span data-ttu-id="46db2-110">Types d’erreurs</span><span class="sxs-lookup"><span data-stu-id="46db2-110">Error Types</span></span>](../../../visual-basic/programming-guide/language-features/error-types.md)
