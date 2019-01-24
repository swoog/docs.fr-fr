---
title: Début &#39;. &#39; ou &#39;! &#39; ne peut apparaître qu’à l’intérieur d’un &#39;avec&#39; instruction
ms.date: 07/20/2015
f1_keywords:
- vbc30157
- bc30157
helpviewer_keywords:
- BC30157
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
ms.openlocfilehash: e64318d4ececbd887f55a1a202cc2d58c90c8fc7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54625950"
---
# <a name="leading-3939-or-3939-can-only-appear-inside-a-39with39-statement"></a>Début &#39;. &#39; ou &#39;! &#39; ne peut apparaître qu’à l’intérieur d’un &#39;avec&#39; instruction
Un point (.) ou un point d’exclamation ( !) qui n’est pas à l’intérieur un `With` bloc se produit sans expression à gauche. Accès au membre (`.`) et l’accès au membre de dictionnaire (`!`) nécessitent une expression spécifiant l’élément qui contient le membre. Cela doit apparaître immédiatement à gauche de l’accesseur ou comme cible d’un `With` bloc contenant l’accès au membre.  
  
 **ID d’erreur :** BC30157  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Vérifiez que le `With` bloc est correctement formaté.  
  
2.  S’il existe aucune `With` bloquer, ajoutez une expression à gauche de l’accesseur qui correspond à un élément défini contenant le membre.  
  
## <a name="see-also"></a>Voir aussi
- [Caractères spéciaux dans le code](../../../visual-basic/programming-guide/program-structure/special-characters-in-code.md)
- [With...End With (instruction)](../../../visual-basic/language-reference/statements/with-end-with-statement.md)
