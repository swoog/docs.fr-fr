---
title: Alias, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Alias
helpviewer_keywords:
- Alias keyword [Visual Basic]
ms.assetid: 58c06b11-465d-4d87-906a-73200a3d7f19
ms.openlocfilehash: 9cf97402d0b0a6cd16dd75a970c1d29a2fcc30a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498568"
---
# <a name="alias-clause-visual-basic"></a>Alias, clause (Visual Basic)
Indique qu’une procédure externe possède un autre nom dans sa DLL.  
  
## <a name="remarks"></a>Notes  
 Le `Alias` mot clé peut être utilisé dans ce contexte :  
  
 [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 Dans l’exemple suivant, le `Alias` mot clé est utilisé pour fournir le nom de la fonction dans advapi32.dll, `GetUserNameA`, qui `getUserName` est utilisé à la place de dans cet exemple. Fonction `getUserName` est appelée dans un sub `getUser`, qui affiche le nom de l’utilisateur actuel.  
  
 [!code-vb[VbVbalrStatements#15](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/alias-clause_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
