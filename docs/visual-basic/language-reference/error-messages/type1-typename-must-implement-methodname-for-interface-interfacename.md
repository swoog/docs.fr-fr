---
title: '&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;methodname&gt; &#39; pour l’interface &#39; &lt;nom_interface&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: daeeab853f6a7f582542fa15ffc09ce749731d6f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33594381"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmethodnamegt39-for-interface-39ltinterfacenamegt39"></a>&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;methodname&gt; &#39; pour l’interface &#39; &lt;nom_interface&gt;&#39;
Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure définie par l’interface. Chaque membre de l’interface doit être implémentée.  
  
 **ID d’erreur :** BC30149  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déclarez une procédure avec le même nom et la même signature que ceux définis dans l’interface. Veillez à inclure au moins les `End Function` ou `End Sub` instruction.  
  
2.  Ajouter un `Implements` clause à la fin de la `Function` ou `Sub` instruction. Par exemple :  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [Implements (instruction)](../../../visual-basic/language-reference/statements/implements-statement.md)  
 [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
