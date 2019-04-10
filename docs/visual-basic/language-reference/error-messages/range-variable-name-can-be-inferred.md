---
title: Le nom de la variable de portée peut être déduit uniquement à partir d’un nom qualifié ou d’un nom simple sans arguments
ms.date: 07/20/2015
f1_keywords:
- vbc36599
- bc36599
helpviewer_keywords:
- BC36599
ms.assetid: 17763dbe-f74f-4ccb-8086-cb7e45ec4d12
ms.openlocfilehash: a0b5633bb0efb3c67f73810552ef9a14ac3d0c70
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59331648"
---
# <a name="range-variable-name-can-be-inferred-only-from-a-simple-or-qualified-name-with-no-arguments"></a>Le nom de la variable de portée peut être déduit uniquement à partir d’un nom qualifié ou d’un nom simple sans arguments
Un élément de programmation qui prend un ou plusieurs arguments est inclus dans une requête LINQ. Le compilateur ne peut pas déduire une variable de portée à partir de cet élément de programmation.  
  
 **ID d’erreur :** BC36599  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Fournissez un nom de variable explicite pour l’élément de programmation, comme indiqué dans le code suivant :  
  
```  
Dim query = From var1 In collection1   
            Select VariableAlias= SampleFunction(var1), var1  
```  
  
## <a name="see-also"></a>Voir aussi

- [Introduction à LINQ dans Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Select, clause](../../../visual-basic/language-reference/queries/select-clause.md)
