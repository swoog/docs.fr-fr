---
title: <type1>«<typename>'doit implémenter'<membername>'pour l’interface'<interfacename>»
ms.date: 07/20/2015
f1_keywords:
- vbc30154
- bc30154
helpviewer_keywords:
- BC30154
ms.assetid: 259afdfa-3608-4760-adcb-88ec0da5020d
ms.openlocfilehash: 86b0d46e0e27b2fd8d1fccb37f4a3c45e95f5f63
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61792091"
---
# <a name="type1typename-must-implement-membername-for-interface-interfacename"></a>\<type1 >'\<nom_type >' doit implémenter '\<nom_membre >' pour l’interface '\<nom_interface >'
'\<nom_type >' doit implémenter '\<nom_membre >' pour l’interface '\<nom_interface >'. Propriété d’implémentation doit avoir correspondant à 'ReadOnly' / 'WriteOnly' spécificateurs.  
  
 Une classe ou une structure déclare implémenter une interface, mais n’implémente pas une procédure, une propriété ou un événement défini par l’interface. Chaque membre de l’interface doit être implémentée.  
  
 **ID d’erreur :** BC30154  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Déclarez un membre avec le même nom et signature tel que défini dans l’interface. Veillez à inclure au moins le `End Function`, `End Sub`, ou `End Property` instruction.  
  
2. Ajouter un `Implements` clause à la fin de la `Function`, `Sub`, `Property`, ou `Event` instruction. Exemple :  
  
    ```  
    Public Event ItHappened() Implements IBaseInterface.ItHappened  
    ```  
  
3. Lorsque vous implémentez une propriété, assurez-vous que `ReadOnly` ou `WriteOnly` est utilisé dans la même façon que dans la définition d’interface.  
  
4. Lorsque vous implémentez une propriété, déclarez `Get` et `Set` procédures, comme il convient.  
  
## <a name="see-also"></a>Voir aussi

- [Implements (instruction)](../../../visual-basic/language-reference/statements/implements-statement.md)
- [Interfaces](../../../visual-basic/programming-guide/language-features/interfaces/index.md)
