---
title: Protected Friend (Visual Basic)
ms.date: 05/10/2018
helpviewer_keywords:
- Protected Friend keyword [Visual Basic]
- Protected Friend keyword [Visual Basic], syntax
ms.openlocfilehash: b72cbee0394043620e792d1c014bfe55121e175e
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/18/2018
ms.locfileid: "34306540"
---
# <a name="protected-friend-visual-basic"></a>Protected Friend (Visual Basic)

La combinaison de mots clés `Protected Friend` est un modificateur d’accès de membre. Il confère à la fois [Friend](friend.md) accès et [protégé](protected.md) accès aux éléments déclarés, afin qu’ils soient accessibles à partir de n’importe où dans le même assembly, de leur propre classe et de classes dérivées. Vous pouvez spécifier `Protected Friend` uniquement sur les membres de classes ; vous ne pouvez pas appliquer `Protected Friend` aux membres d’une structure, car les structures ne peuvent pas être héritées.

> [!NOTE]
> Dans Visual Studio, en sélectionnant la touche F1 sur `protected friend` fournit une aide pour soit [protégé](protected.md) ou [friend](friend.md). L’IDE choisit le jeton unique sous le curseur plutôt que le mot composé.

## <a name="rules"></a>Règles

- **Contexte de déclaration.** Vous pouvez utiliser `Protected Friend` uniquement au niveau de la classe. Cela signifie que le contexte de déclaration pour un `Protected` élément doit être une classe et ne peut pas être un fichier source, espace de noms, interface, un module, structure ou procédure. 


## <a name="see-also"></a>Voir aussi

[Public](../../../visual-basic/language-reference/modifiers/public.md)  
[Protected](../../../visual-basic/language-reference/modifiers/protected.md)  
[Friend](friend.md)   
[Private](../../../visual-basic/language-reference/modifiers/private.md)  
[Protégé privé](./private-protected.md)   
[Niveaux d’accès dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)  
[Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)  
[Structures](../../../visual-basic/programming-guide/language-features/data-types/structures.md)  
[Objets et classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
