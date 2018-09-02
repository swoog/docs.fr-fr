---
title: Dépassement de capacité (erreur d'exécution Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrERRID_Overflow
ms.assetid: c6a23279-3086-412a-bcff-ff8ed2cb8c6f
ms.openlocfilehash: 7546676b85465577b357b7ad0757b4db8d40dbe3
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43466038"
---
# <a name="overflow-visual-basic-run-time-error"></a>Dépassement de capacité (erreur d'exécution Visual Basic)
Un dépassement de capacité se produit lorsque vous essayez d’une assignation qui dépasse les limites de la cible de l’assignation.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Assurez-vous que les résultats de type de données, des calculs et des attributions de conversions ne sont pas trop grand pour être représenté dans la plage de variables autorisées pour ce type de valeur et affectez la valeur à une variable d’un type qui peuvent contenir un grand nombre de valeurs , si nécessaire.  
  
2.  Assurez-vous que les affectations aux propriétés correspondent à la plage de la propriété à laquelle elles ont été effectuées.  
  
3.  Assurez-vous que les numéros utilisés dans les calculs sont convertis en entiers n’ont pas de résultats supérieurs aux entiers.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Int32.MaxValue?displayProperty=nameWithType>  
 <xref:System.Double.MaxValue?displayProperty=nameWithType>  
 [Types de données](../../../visual-basic/language-reference/data-types/index.md)  
 [Types d’erreurs](../../../visual-basic/programming-guide/language-features/error-types.md)
