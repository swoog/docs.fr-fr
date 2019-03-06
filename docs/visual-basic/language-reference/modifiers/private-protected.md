---
title: Private protégé (Visual Basic)
ms.date: 05/10/2018
helpviewer_keywords:
- Private Protected keyword [Visual Basic]
- Private Protected keyword [Visual Basic], syntax
ms.openlocfilehash: fea43558ac0fe8181f2786b69f2621346d446b2e
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57376388"
---
# <a name="private-protected-visual-basic"></a>Private protégé (Visual Basic)

La combinaison de mots clés `Private Protected` est un modificateur d’accès de membre. Un `Private Protected` membre est accessible par tous les membres de sa classe conteneur, ainsi que par les types dérivés de la classe conteneur, mais uniquement si elles sont trouvent dans son assembly conteneur.

Vous pouvez spécifier `Private Protected` uniquement sur les membres de classes ; vous ne pouvez pas appliquer `Private Protected` aux membres d’une structure, car les structures ne peuvent pas être héritées.

Le `Private Protected` modificateur d’accès est pris en charge par Visual Basic 15.5 et versions ultérieures. Pour l’utiliser, vous pouvez ajouter l’élément suivant à votre projet Visual Basic (\*.vbproj) fichier. Comme tant que Visual Basic 15.5 ou version ultérieure est installé sur votre système, il vous permet de tirer parti de toutes les fonctionnalités de langage pris en charge par la dernière version du compilateur Visual Basic :

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

Pour plus d’informations, consultez [définition de la version de langage Visual Basic](../../language-reference/configure-language-version.md).

> [!NOTE]
> Dans Visual Studio, en sélectionnant la touche F1 sur `private protected` fournit une aide pour soit [privé](private.md) ou [protégé](protected.md). L’IDE choisit le jeton unique sous le curseur plutôt que le mot composé.

## <a name="rules"></a>Règles

- **Contexte de déclaration.** Vous pouvez utiliser `Private Protected` uniquement au niveau de la classe. Cela signifie que le contexte de déclaration pour un `Protected` élément doit être une classe et ne peut pas être une fichier source, un espace de noms, un module, une structure ou une procédure.

## <a name="behavior"></a>Comportement

- **Niveau d’accès.** Tout le code dans une classe peut accéder à ses éléments. Code dans toute classe qui dérive d’une classe de base et est contenue dans le même assembly peut accéder à tous les `Private Protected` éléments de la classe de base. Toutefois, le code dans toute classe qui dérive d’une classe de base et est contenue dans un autre assembly ne peut pas accéder à la classe de base `Private Protected` éléments.

- **Modificateurs d’accès.** Les mots clés qui spécifient le niveau d’accès sont appelés *modificateurs d’accès*. Pour obtenir une comparaison des modificateurs d’accès, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).

Le modificateur `Private Protected` peut être utilisé dans les contextes suivants :

- [Class, instruction](../../../visual-basic/language-reference/statements/class-statement.md) d’une classe imbriquée

- [Const (instruction)](../../../visual-basic/language-reference/statements/const-statement.md)

- [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)

- [Delegate, instruction](../../../visual-basic/language-reference/statements/delegate-statement.md) d’un délégué imbriqué dans une classe

- [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)

- [Enum, instruction](../../../visual-basic/language-reference/statements/enum-statement.md) d’une énumération imbriquée dans une classe

- [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)

- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)

- [Interface, instruction](../../../visual-basic/language-reference/statements/interface-statement.md) d’une interface imbriquée dans une classe

- [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)

- [Structure instruction](../../../visual-basic/language-reference/statements/structure-statement.md) d’une structure imbriquée dans une classe

- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)

## <a name="see-also"></a>Voir aussi

- [Public](../../../visual-basic/language-reference/modifiers/public.md)
- [Protected](../../../visual-basic/language-reference/modifiers/protected.md)
- [Friend](friend.md)
- [Private](../../../visual-basic/language-reference/modifiers/private.md)
- [Protected Friend](./protected-friend.md)
- [Niveaux d’accès dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [Procédures](../../../visual-basic/programming-guide/language-features/procedures/index.md)
- [Structures](../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Objets et classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
