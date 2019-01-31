---
title: <type1> '<typename>' doit implémenter '<methodname>' pour l'interface '<interfacename>'
ms.date: 07/20/2015
f1_keywords:
- vbc30149
- bc30149
helpviewer_keywords:
- BC30149
ms.assetid: 29d1b7f4-dca7-478c-bbe7-c657f342c183
ms.openlocfilehash: c5dd7c6889a3fb5344142ee9914f98e8922d748b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264430"
---
# <a name="type1typename-must-implement-methodname-for-interface-interfacename"></a>\<type1 >'\<nom_type >' doit implémenter '\<nom_méthode >' pour l’interface '\<nom_interface >'
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
