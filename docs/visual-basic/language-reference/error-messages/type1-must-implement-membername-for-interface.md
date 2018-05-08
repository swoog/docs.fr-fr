---
title: '&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;membername&gt; &#39; pour l’interface &#39; &lt;nom_interface&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30154
- bc30154
helpviewer_keywords:
- BC30154
ms.assetid: 259afdfa-3608-4760-adcb-88ec0da5020d
ms.openlocfilehash: 0f93bd137bdc21268cbca139ae739843561350ac
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmembernamegt39-for-interface-39ltinterfacenamegt39"></a>&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;membername&gt; &#39; pour l’interface &#39; &lt;nom_interface&gt;&#39;
'\<nom_type >' doit implémenter '\<nom_membre >' pour l’interface '\<nom_interface >'. Propriété d’implémentation doit avoir correspondant à 'ReadOnly' / 'WriteOnly' spécificateurs.  
  
 Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure, une propriété ou un événement défini par l’interface. Chaque membre de l’interface doit être implémentée.  
  
 **ID d’erreur :** BC30154  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déclarez un membre portant le même nom et la même signature que ceux définis dans l’interface. Veillez à inclure au moins les `End Function`, `End Sub`, ou `End Property` instruction.  
  
2.  Ajouter un `Implements` clause à la fin de la `Function`, `Sub`, `Property`, ou `Event` instruction. Par exemple :  
  
    ```  
    Public Event ItHappened() Implements IBaseInterface.ItHappened  
    ```  
  
3.  Lors de l’implémentation d’une propriété, assurez-vous que `ReadOnly` ou `WriteOnly` est utilisé de la même façon que dans la définition d’interface.  
  
4.  Lors de l’implémentation d’une propriété, déclarez `Get` et `Set` procédures, comme il convient.  
  
## <a name="see-also"></a>Voir aussi  
 [Implements (instruction)](../../../visual-basic/language-reference/statements/implements-statement.md)  
 [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
