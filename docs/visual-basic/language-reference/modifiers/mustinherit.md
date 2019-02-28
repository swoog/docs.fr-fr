---
title: MustInherit (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- MustInherit
- vb.MustInherit
helpviewer_keywords:
- classes [Visual Basic], abstract
- MustInherit classes [Visual Basic], MustInherit keyword
- abstract classes [Visual Basic], MustInherit class
- MustInherit keyword [Visual Basic]
ms.assetid: b8f05185-90e3-4dd7-adc2-90d852fab5b4
ms.openlocfilehash: 124262695f9333ce31c4097662688e0fe30f300d
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56969529"
---
# <a name="mustinherit-visual-basic"></a>MustInherit (Visual Basic)
Spécifie qu’une classe peut être utilisée uniquement comme classe de base et que vous ne pouvez pas créer un objet directement à partir de celui-ci.  
  
## <a name="remarks"></a>Notes  
 L’objectif d’un *classe de base* (également appelé un *classe abstraite*) consiste à définir des fonctionnalités communes à toutes les classes dérivées à partir de celui-ci. Cela évite les classes dérivées de devoir redéfinir les éléments communs. Dans certains cas, cette fonctionnalité commune n’est pas suffisamment complète pour rendre un objet utilisable, et chaque classe dérivée définit la fonctionnalité manquante. Dans ce cas, vous souhaitez le code utilisé pour créer des objets uniquement à partir de classes dérivées. Vous utilisez `MustInherit` sur la classe de base à appliquer cette recommandation.  
  
 Une autre utilisation d’un `MustInherit` classe consiste à restreindre une variable à un jeu de classes connexes. Vous pouvez définir une classe de base et dérivez toutes ces classes connexes à partir de celui-ci. La classe de base est inutile de fournir une fonctionnalité commune à toutes les classes dérivées, mais il peut servir de filtre pour assigner des valeurs aux variables. Si votre code de consommation déclare une variable comme classe de base, Visual Basic vous permet à affecter uniquement un objet à partir d’une des classes dérivées à cette variable.  
  
 Le .NET Framework définit plusieurs `MustInherit` classes, parmi les <xref:System.Array>, <xref:System.Enum>, et <xref:System.ValueType>. <xref:System.ValueType> est un exemple d’une classe de base qui restreint une variable. Tous les types valeur dérivent <xref:System.ValueType>. Si vous déclarez une variable en tant que <xref:System.ValueType>, vous pouvez affecter uniquement les types de valeur à cette variable.  
  
## <a name="rules"></a>Règles  
  
-   **Contexte de déclaration.** Vous pouvez utiliser `MustInherit` uniquement dans un `Class` instruction.  
  
-   **Modificateurs combinés.** Vous ne pouvez pas spécifier `MustInherit` avec `NotInheritable` dans la même déclaration.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre l’héritage et la substitution forcés. La classe de base `shape` définit une variable `acrossLine`. Les classes `circle` et `square` dérivent `shape`. Ils héritent de la définition de `acrossLine`, mais elles doivent définir la fonction `area` parce que ce calcul est différent pour chaque type de forme.  
  
 [!code-vb[VbVbalrKeywords#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class1.vb#2)]  
  
 Vous pouvez déclarer `shape1` et `shape2` soit de type `shape`. Toutefois, vous ne pouvez pas créer un objet à partir de `shape` , car il ne dispose pas de la fonctionnalité de la fonction `area` et est marquée comme `MustInherit`.  
  
 Car elles sont déclarées comme `shape`, les variables `shape1` et `shape2` sont limités aux objets à partir de classes dérivées `circle` et `square`. Visual Basic ne permet pas d’attribuer n’importe quel autre objet à ces variables, qui vous offre un niveau élevé de sécurité de type.  
  
## <a name="usage"></a>Utilisation  
 Le `MustInherit` modificateur peut être utilisé dans ce contexte :  
  
 [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)  
  
## <a name="see-also"></a>Voir aussi
- [Inherits (instruction)](../../../visual-basic/language-reference/statements/inherits-statement.md)
- [NotInheritable](../../../visual-basic/language-reference/modifiers/notinheritable.md)
- [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
- [Éléments fondamentaux de l’héritage](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)
