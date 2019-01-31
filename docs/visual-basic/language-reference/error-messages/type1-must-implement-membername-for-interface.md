---
title: <type1> '<typename>' doit implémenter '<membername>' pour l'interface '<interfacename>'
ms.date: 07/20/2015
f1_keywords:
- vbc30154
- bc30154
helpviewer_keywords:
- BC30154
ms.assetid: 259afdfa-3608-4760-adcb-88ec0da5020d
ms.openlocfilehash: de7dd9026e08495941a89be0db11ad4c68d2a748
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264230"
---
# <a name="type1typename-must-implement-membername-for-interface-interfacename"></a>\<type1 >'\<nom_type >' doit implémenter '\<nom_membre >' pour l’interface '\<nom_interface >'
'\<nom_type >' doit implémenter '\<nom_membre >' pour l’interface '\<nom_interface >'. Propriété d’implémentation doit avoir correspondant à 'ReadOnly' / 'WriteOnly' spécificateurs.  
  
 Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure, une propriété ou un événement défini par l’interface. Chaque membre de l’interface doit être implémentée.  
  
 **ID d’erreur :** BC30154  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déclarez un membre avec le même nom et signature tel que défini dans l’interface. Veillez à inclure au moins le `End Function`, `End Sub`, ou `End Property` instruction.  
  
2.  Ajouter un `Implements` clause à la fin de la `Function`, `Sub`, `Property`, ou `Event` instruction. Exemple :  
  
    ```  
    Public Event ItHappened() Implements IBaseInterface.ItHappened  
    ```  
  
3.  Lorsque vous implémentez une propriété, assurez-vous que `ReadOnly` ou `WriteOnly` est utilisé dans la même façon que dans la définition d’interface.  
  
4.  Lorsque vous implémentez une propriété, déclarez `Get` et `Set` procédures, comme il convient.  
  
## <a name="see-also"></a>Voir aussi
- [Implements (instruction)](../../../visual-basic/language-reference/statements/implements-statement.md)
- [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
