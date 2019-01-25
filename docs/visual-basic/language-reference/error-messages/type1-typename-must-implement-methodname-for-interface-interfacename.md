---
title: '&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;nom_méthode&gt; &#39; pour interface &#39; &lt;nom_interface&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: ff9ffd50f7f21814d5e4c23fd8df50b12bf746f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642439"
---
# <a name="lttype1gt39lttypenamegt39-must-implement-39ltmethodnamegt39-for-interface-39ltinterfacenamegt39"></a>&lt;type1&gt;&#39;&lt;typename&gt; &#39; doit implémenter &#39; &lt;nom_méthode&gt; &#39; pour interface &#39; &lt;nom_interface&gt;&#39;
Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure définie par l’interface. Chaque membre de l’interface doit être implémentée.  
  
 **ID d’erreur :** BC30149  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déclarez une procédure avec le même nom et signature tel que défini dans l’interface. Veillez à inclure au moins le `End Function` ou `End Sub` instruction.  
  
2.  Ajouter un `Implements` clause à la fin de la `Function` ou `Sub` instruction. Exemple :  
  
    ```  
    Public Sub DoSomething() Implements IBaseInterface.DoSomething  
    ```  
  
## <a name="see-also"></a>Voir aussi
- [Implements (instruction)](../../../visual-basic/language-reference/statements/implements-statement.md)
- [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
