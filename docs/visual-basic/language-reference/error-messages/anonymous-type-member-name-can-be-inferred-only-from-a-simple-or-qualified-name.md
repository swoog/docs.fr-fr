---
title: Le nom du membre de type anonyme ne peut être déduit qu’à partir d’un nom simple ou qualifié sans argument
ms.date: 07/20/2015
f1_keywords:
- vbc36556
- bc36556
helpviewer_keywords:
- BC36556
ms.assetid: e3ba1f33-3a71-4f03-9b04-ed5ec17de17c
ms.openlocfilehash: 4d91b7a3c57db38fde3cf371773e8d64834a8f72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715268"
---
# <a name="anonymous-type-member-name-can-be-inferred-only-from-a-simple-or-qualified-name-with-no-arguments"></a>Le nom du membre de type anonyme ne peut être déduit qu’à partir d’un nom simple ou qualifié sans argument
Impossible de déduire un nom de membre de type anonyme à partir d’une expression complexe.  
  
```vb  
Dim numbers() As Integer = {1, 2, 3, 4, 5}  
' Not valid.  
' Dim instanceName1 = New With {numbers(3)}  
```  
  
 Pour plus d’informations sur les sources à partir de laquelle les types anonymes peuvent et ne peut pas déduire les types et les noms de membres, consultez [Comment : Déduire les Types dans les déclarations de types anonymes et les noms de propriété](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md).  
  
 **ID d’erreur :** BC36556  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Assignez l’expression à un nom de membre, comme indiqué dans le code suivant :  
  
    ```  
    Dim instanceName2 = New With {.number = numbers(3)}  
    ```  
  
## <a name="see-also"></a>Voir aussi
- [Types anonymes](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
- [Guide pratique pour Déduire les Types dans les déclarations de types anonymes et les noms de propriété](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-infer-property-names-and-types-in-anonymous-type-declarations.md)
