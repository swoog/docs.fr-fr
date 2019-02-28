---
title: Byval (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ByVal
- ByVal
helpviewer_keywords:
- ByVal keyword [Visual Basic], contexts
- ByVal keyword [Visual Basic]
ms.assetid: 1eaf4e58-b305-4785-9e3d-e416b9c75598
ms.openlocfilehash: edee47e41ca78175a6fb24ed5eac255c03de0901
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56972562"
---
# <a name="byval-visual-basic"></a>Byval (Visual Basic)
Spécifie qu’un argument est passé de sorte que la procédure ou propriété appelée ne peut pas modifier la valeur d’une variable sous-jacente à l’argument dans le code appelant.  
  
## <a name="remarks"></a>Notes  
 Le modificateur `ByVal` peut être utilisé dans les contextes suivants :  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Operator (instruction)](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre l’utilisation de la `ByVal` mécanisme avec un argument de type de référence de passage de paramètres. Dans l’exemple, l’argument est `c1`, une instance de classe `Class1`. `ByVal` empêche le code dans les procédures de modification de la valeur sous-jacente de l’argument de référence, `c1`, mais ne protège ne pas les champs accessibles et les propriétés de `c1`.  
  
 [!code-vb[VbVbalrKeywords#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class5.vb#10)]  
  
## <a name="see-also"></a>Voir aussi
- [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
- [Passage d’un argument par valeur et par référence](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
