---
title: Friend (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Friend
helpviewer_keywords:
- Friend keyword [Visual Basic]
- Friend access modifier
- Friend keyword [Visual Basic], syntax
- Protected Friend keyword combination
- Friend keyword [Visual Basic], and Protected
ms.assetid: b664605e-1c79-4728-b996-aa59c50846bc
ms.openlocfilehash: d906fc8ada19f22059da44acbd76dd07dacd4801
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/17/2018
ms.locfileid: "34234587"
---
# <a name="friend-visual-basic"></a>Friend (Visual Basic)
Spécifie qu’un ou plusieurs éléments de programmation déclarés sont accessibles uniquement à partir de l’assembly qui contient leur déclaration.  
  
## <a name="remarks"></a>Notes  
 Dans de nombreux cas, vous souhaitez que les éléments tels que les classes et les structures à utiliser par la totalité de l’assembly, pas uniquement par le composant qui les déclare de programmation. Toutefois, vous pouvez les rendre accessibles par le code en dehors de l’assembly (par exemple, si l’application est propriétaire). Si vous souhaitez limiter l’accès à un élément de cette façon, vous pouvez la déclarer à l’aide de la `Friend` modificateur.  
  
 Le code dans d’autres classes, structures et les modules qui sont compilés dans le même assembly peut accéder à tous les `Friend` éléments dans cet assembly.  
  
 `Friend` l’accès est souvent le niveau par défaut pour les éléments de programmation d’une application, et `Friend` est l’accès par défaut au niveau d’une interface, un module, une classe ou une structure.  
  
 Vous pouvez utiliser `Friend` uniquement au niveau du module, interface ou espace de noms. Par conséquent, le contexte de déclaration pour un `Friend` élément doit être un fichier source, un espace de noms, une interface, un module, une classe ou une structure ; il ne peut pas être une procédure.  

> [!NOTE]
> Vous pouvez également utiliser le [Protected Friend](protected-friend.md) modificateur d’accès, ce qui rend un membre de classe accessible à partir de cette classe, à partir de classes dérivées et à partir de l’assembly dans lequel la classe est définie. Pour restreindre l’accès à un membre à partir de sa classe et à partir de classes dérivées dans le même assembly, vous utilisez la [protégé privé](private-protected.md) modificateur d’accès.

 Pour obtenir une comparaison de `Friend` et l’autre les modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
> [!NOTE]
>  Vous pouvez spécifier qu’un autre assembly est un assembly friend, ce qui permet d’accéder à tous les types et membres qui sont marqués comme `Friend`. Pour plus d’informations, consultez [Assemblys friend](../../programming-guide/concepts/assemblies-gac/friend-assemblies.md).  
  
## <a name="example"></a>Exemple  
 La classe suivante utilise le `Friend` modificateur pour autoriser d’autres éléments de programmation dans le même assembly pour accéder à certains membres.  
  
 [!code-vb[VbVbalrAccessModifiers#1](../../../visual-basic/language-reference/modifiers/codesnippet/VisualBasic/friend_1.vb)]  
  
## <a name="usage"></a>Utilisation  
 Vous pouvez utiliser la `Friend` modificateur dans les contextes :  
  
 [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)  
  
 [Const (instruction)](../../../visual-basic/language-reference/statements/const-statement.md)  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Delegate (instruction)](../../../visual-basic/language-reference/statements/delegate-statement.md)  
  
 [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)  
  
 [Enum (instruction)](../../../visual-basic/language-reference/statements/enum-statement.md)  
  
 [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Interface (instruction)](../../../visual-basic/language-reference/statements/interface-statement.md)  
  
 [Module (instruction)](../../../visual-basic/language-reference/statements/module-statement.md)  
  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)  
  
 [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute>  
 [Public](../../../visual-basic/language-reference/modifiers/public.md)  
 [Protected](../../../visual-basic/language-reference/modifiers/protected.md)  
 [Private](../../../visual-basic/language-reference/modifiers/private.md)  
 [Protégé privé](./private-protected.md)   
 [Protected Friend](./protected-friend.md)   
 [Niveaux d’accès dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)  
 [Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)  
 [Structures](../../../visual-basic/programming-guide/language-features/data-types/structures.md)  
 [Objets et classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
