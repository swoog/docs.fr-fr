---
title: La première instruction de ce &#39;Sub New&#39; doit être un appel à &#39;MyBase.New&#39; ou &#39;MyClass.New&#39; (aucun constructeur Accessible sans paramètres)
ms.date: 07/20/2015
f1_keywords:
- bc30148
- vbc30148
helpviewer_keywords:
- BC30148
ms.assetid: 4426e8fc-cb39-4eb8-ba95-503cd32fcc89
ms.openlocfilehash: 75832ae88908094c1cb74ce04ad84c0d2ae91e68
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54728893"
---
# <a name="first-statement-of-this-39sub-new39-must-be-a-call-to-39mybasenew39-or-39myclassnew39-no-accessible-constructor-without-parameters"></a>La première instruction de ce &#39;Sub New&#39; doit être un appel à &#39;MyBase.New&#39; ou &#39;MyClass.New&#39; (aucun constructeur Accessible sans paramètres)
La première instruction de ce 'Sub New' doit être un appel à 'MyBase.New' ou 'MyClass.New', car classe de base\<basename >' de '\<derivedname >' n’a pas de 'Sub New' accessible qui peut être appelé sans argument.  
  
 Dans une classe dérivée, chaque constructeur doit appeler un constructeur de classe de base (`MyBase.New`). Si la classe de base a un constructeur sans paramètre accessible aux classes dérivées, `MyBase.New` peut être appelé automatiquement. Si ce n’est pas le cas, un constructeur de classe de base doit être appelé avec des paramètres, et il ne peut pas être effectuée automatiquement. Dans ce cas, la première instruction de chaque constructeur de classe dérivée doit appeler un constructeur paramétrable sur la classe de base, ou appeler un autre constructeur dans la classe dérivée qui appelle un constructeur de classe de base.  
  
 **ID d’erreur :** BC30148  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Appeler `MyBase.New` en fournissant les paramètres requis ou appelez un constructeur homologue qui effectue un appel de ce type.  
  
     Par exemple, si la classe de base a un constructeur est déclaré comme `Public Sub New(ByVal index as Integer)`, la première instruction dans dérivé constructeur de classe peut être `MyBase.New(100)`.  
  
## <a name="see-also"></a>Voir aussi
- [Éléments fondamentaux de l’héritage](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
