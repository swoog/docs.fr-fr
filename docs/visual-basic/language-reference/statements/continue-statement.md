---
title: Continue, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.continue
helpviewer_keywords:
- Continue statement [Visual Basic]
- loops, transferring to next iteration
ms.assetid: 3ad00103-358b-4af3-a3a8-1b9ea0e995d3
ms.openlocfilehash: eb8596c43bf6232eec4bcb844e6202c5de373404
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602721"
---
# <a name="continue-statement-visual-basic"></a>Continue, instruction (Visual Basic)
Transfère le contrôle immédiatement à l’itération suivante d’une boucle.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Continue { Do | For | While }  
```  
  
## <a name="remarks"></a>Notes  
 Vous pouvez transférer à partir d’à l’intérieur d’un `Do`, `For`, ou `While` boucle à l’itération suivante de cette boucle. Contrôle passe immédiatement au test de condition de la boucle, ce qui revient à effectuer un transfert à la `For` ou `While` instruction, ou à la `Do` ou `Loop` instruction qui contient le `Until` ou `While` clause.  
  
 Vous pouvez utiliser `Continue` à n’importe quel emplacement de la boucle qui autorise les transferts. Les règles qui autorisent le transfert de contrôle sont identiques à celles de la [instruction GoTo](../../../visual-basic/language-reference/statements/goto-statement.md).  
  
 Par exemple, si une boucle est entièrement contenue dans un `Try` bloc, un `Catch` bloc, ou un `Finally` bloc, vous pouvez utiliser `Continue` pour transférer hors de la boucle. If, d’autre part, le `Try`... `End Try` structure est contenue dans la boucle, vous ne pouvez pas utiliser `Continue` pour transférer le contrôle de la `Finally` bloc et vous pouvez l’utiliser pour transférer d’un `Try` ou `Catch` bloquer uniquement si vous transférez complètement hors de la `Try`... `End Try` structure.  
  
 Si vous avez des boucles imbriquées du même type, par exemple un `Do` boucle dans une autre `Do` boucle, une `Continue Do` instruction passe à l’itération suivante de la plus profonde `Do` boucle qui le contient. Vous ne pouvez pas utiliser `Continue` pour passer à l’itération suivante d’une boucle conteneur du même type.  
  
 Si vous avez des boucles imbriquées de types différents, par exemple un `Do` mises en boucle dans un `For` boucle, vous pouvez passer à l’itération suivante d’une boucle à l’aide `Continue Do` ou `Continue For`.  
  
## <a name="example"></a>Exemple  
 Le code suivant exemple utilise la `Continue While` instruction pour passer à la colonne suivante d’un tableau si un diviseur est égale à zéro. Le `Continue While` se trouve dans un `For` boucle. Elle transfère vers le `While col < lastcol` instruction, qui est l’itération suivante de la plus profonde `While` boucle qui contient le `For` boucle.  
  
 [!code-vb[VbVbalrStatements#14](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/continue-statement_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Do...Loop (instruction)](../../../visual-basic/language-reference/statements/do-loop-statement.md)  
 [For...Next (instruction)](../../../visual-basic/language-reference/statements/for-next-statement.md)  
 [While...End While (instruction)](../../../visual-basic/language-reference/statements/while-end-while-statement.md)  
 [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
