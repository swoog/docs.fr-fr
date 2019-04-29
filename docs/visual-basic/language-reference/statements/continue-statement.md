---
title: Continue, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.continue
helpviewer_keywords:
- Continue statement [Visual Basic]
- loops, transferring to next iteration
ms.assetid: 3ad00103-358b-4af3-a3a8-1b9ea0e995d3
ms.openlocfilehash: 5523be69f2901851c86f6c0263548e3577507ff9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638244"
---
# <a name="continue-statement-visual-basic"></a>Continue, instruction (Visual Basic)
Transfère le contrôle immédiatement à l’itération suivante d’une boucle.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Continue { Do | For | While }  
```  
  
## <a name="remarks"></a>Notes  
 Vous pouvez transférer à partir d’à l’intérieur d’un `Do`, `For`, ou `While` boucle à l’itération suivante de cette boucle. Le contrôle passe immédiatement pour le test de condition de boucle, qui équivaut à transférer à la `For` ou `While` instruction, ou vers le `Do` ou `Loop` instruction qui contient le `Until` ou `While` clause.  
  
 Vous pouvez utiliser `Continue` à n’importe quel emplacement dans la boucle qui autorise les transferts. Les règles autorisant le transfert de contrôle sont identiques à celles de la [instruction GoTo](../../../visual-basic/language-reference/statements/goto-statement.md).  
  
 Par exemple, si une boucle est entièrement contenue dans un `Try` bloc, un `Catch` bloc, ou un `Finally` bloc, vous pouvez utiliser `Continue` pour transférer en dehors de la boucle. If, d’autre part, le `Try`... `End Try` structure est contenue dans la boucle, vous ne pouvez pas utiliser `Continue` pour transférer le contrôle hors de la `Finally` bloc et vous pouvez l’utiliser pour transférer d’un `Try` ou `Catch` bloquer uniquement si vous transférez complètement hors le `Try`... `End Try` structure.  
  
 Si vous avez des boucles imbriquées du même type, par exemple un `Do` boucle dans une autre `Do` boucle, une `Continue Do` instruction passe à l’itération suivante de la plus intérieure `Do` boucle qui le contient. Vous ne pouvez pas utiliser `Continue` pour passer à l’itération suivante d’une boucle conteneur du même type.  
  
 Si vous avez des boucles imbriquées de types différents, par exemple un `Do` mises en boucle dans un `For` boucle, vous pouvez passer à l’itération suivante d’une boucle à l’aide `Continue Do` ou `Continue For`.  
  
## <a name="example"></a>Exemple  
 Le code suivant exemple utilise le `Continue While` instruction pour passer à la colonne suivante d’un tableau si un diviseur est égale à zéro. Le `Continue While` se trouve dans un `For` boucle. Il transfère à la `While col < lastcol` instruction, qui est l’itération suivante de la plus intérieure `While` boucle qui contient le `For` boucle.  
  
 [!code-vb[VbVbalrStatements#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#14)]  
  
## <a name="see-also"></a>Voir aussi

- [Do...Loop (instruction)](../../../visual-basic/language-reference/statements/do-loop-statement.md)
- [For...Next (instruction)](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [While...End While (instruction)](../../../visual-basic/language-reference/statements/while-end-while-statement.md)
- [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
