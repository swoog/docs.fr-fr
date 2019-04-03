---
title: Private (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Private
helpviewer_keywords:
- Private keyword [Visual Basic]
- Private keyword [Visual Basic], syntax
ms.assetid: aba74a2e-5824-4613-bf63-b9ec7787f4e6
ms.openlocfilehash: d6e28e5e87c3a88e4db3fc81177894683dbb0908
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58819474"
---
# <a name="private-visual-basic"></a>Private (Visual Basic)
Spécifie qu’un ou plusieurs éléments de programmation déclarés sont accessibles uniquement à partir de leur contexte de déclaration, y compris à partir des types contenus.  
  
## <a name="remarks"></a>Notes  
 Si un élément de programmation représente des fonctionnalités exclusives ou contient des données confidentielles, vous souhaitez généralement limiter son accès aussi strictement que possible. Vous obtenez une limitation maximale en autorisant uniquement le module, classe ou structure qui le définit pour y accéder. Pour limiter l’accès à un élément de cette façon, vous pouvez le déclarer avec `Private`.  

> [!NOTE]
> Vous pouvez également utiliser le [Private Protected](private-protected.md) modificateur d’accès, ce qui rend un membre accessible à partir de cette classe et à partir de classes dérivées situées dans son assembly conteneur.

## <a name="rules"></a>Règles  

-   **Contexte de déclaration.** Vous pouvez utiliser `Private` seulement au niveau du module. Cela signifie que le contexte de déclaration pour un `Private` élément doit être un module, une classe ou une structure et ne peut pas être un fichier source, un espace de noms, une interface ou une procédure.  
  
## <a name="behavior"></a>Comportement  
  
-   **Niveau d’accès.** Tout le code dans un contexte de déclaration peut accéder à ses `Private` éléments. Cela inclut le code au sein d’un type de relation contenant-contenu, comme une classe imbriquée ou une expression d’assignation dans une énumération. Aucun code en dehors du contexte de déclaration ne peut accéder à ses `Private` éléments.  
  
-   **Modificateurs d’accès.** Les mots clés qui spécifient le niveau d’accès sont appelés *modificateurs d’accès*. Pour obtenir une comparaison des modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
 Le modificateur `Private` peut être utilisé dans les contextes suivants :  
  
 [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)  
  
 [Const (instruction)](../../../visual-basic/language-reference/statements/const-statement.md)  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Delegate (instruction)](../../../visual-basic/language-reference/statements/delegate-statement.md)  
  
 [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [Enum (instruction)](../../../visual-basic/language-reference/statements/enum-statement.md)  
  
 [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Interface (instruction)](../../../visual-basic/language-reference/statements/interface-statement.md)  
  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)  
  
 [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a>Voir aussi

- [Public](../../../visual-basic/language-reference/modifiers/public.md)
- [Protected](../../../visual-basic/language-reference/modifiers/protected.md)
- [Friend](../../../visual-basic/language-reference/modifiers/friend.md)
- [Private Protected](./private-protected.md)
- [Protected Friend](./protected-friend.md)[Access levels dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [Structures](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Objets et classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
