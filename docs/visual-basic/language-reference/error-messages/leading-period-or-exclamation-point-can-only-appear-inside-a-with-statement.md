---
title: Un caractère '.' ou '!' de début ne peut apparaître que dans une instruction 'With'
ms.date: 07/20/2015
f1_keywords:
- vbc30157
- bc30157
helpviewer_keywords:
- BC30157
ms.assetid: 70daaee1-14f9-45b7-9f30-53794310b95e
ms.openlocfilehash: 15390fb506fe9bca10f6917f5b26451a5569bece
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61921119"
---
# <a name="leading--or--can-only-appear-inside-a-with-statement"></a>Un caractère '.' ou '!' de début ne peut apparaître que dans une instruction 'With'
Un point (.) ou un point d’exclamation ( !) qui n’est pas à l’intérieur un `With` bloc se produit sans expression à gauche. Accès au membre (`.`) et l’accès au membre de dictionnaire (`!`) nécessitent une expression spécifiant l’élément qui contient le membre. Cela doit apparaître immédiatement à gauche de l’accesseur ou comme cible d’un `With` bloc contenant l’accès au membre.  
  
 **ID d’erreur :** BC30157  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Vérifiez que le `With` bloc est correctement formaté.  
  
2. S’il existe aucune `With` bloquer, ajoutez une expression à gauche de l’accesseur qui correspond à un élément défini contenant le membre.  
  
## <a name="see-also"></a>Voir aussi

- [Caractères spéciaux dans le code](../../../visual-basic/programming-guide/program-structure/special-characters-in-code.md)
- [With...End With (instruction)](../../../visual-basic/language-reference/statements/with-end-with-statement.md)
