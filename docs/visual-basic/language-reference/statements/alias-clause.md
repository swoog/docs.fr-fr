---
title: Alias, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Alias
helpviewer_keywords:
- Alias keyword [Visual Basic]
ms.assetid: 58c06b11-465d-4d87-906a-73200a3d7f19
ms.openlocfilehash: 62b34f5860b35104b6a8caa82c359383999dd61b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="alias-clause-visual-basic"></a>Alias, clause (Visual Basic)
Indique qu’une procédure externe a un autre nom dans sa DLL.  
  
## <a name="remarks"></a>Notes  
 Le `Alias` mot clé peut être utilisé dans ce contexte :  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 Dans l’exemple suivant, la `Alias` est utilisé pour fournir le nom de la fonction dans advapi32.dll, `GetUserNameA`, qui `getUserName` est utilisé à la place de dans cet exemple. Fonction `getUserName` est appelée dans un sub `getUser`, qui affiche le nom de l’utilisateur actuel.  
  
 [!code-vb[VbVbalrStatements#15](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/alias-clause_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
