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
ms.locfileid: "33599172"
---
# <a name="alias-clause-visual-basic"></a><span data-ttu-id="1f9d5-102">Alias, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1f9d5-102">Alias Clause (Visual Basic)</span></span>
<span data-ttu-id="1f9d5-103">Indique qu’une procédure externe a un autre nom dans sa DLL.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-103">Indicates that an external procedure has another name in its DLL.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1f9d5-104">Notes</span><span class="sxs-lookup"><span data-stu-id="1f9d5-104">Remarks</span></span>  
 <span data-ttu-id="1f9d5-105">Le `Alias` mot clé peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="1f9d5-105">The `Alias` keyword can be used in this context:</span></span>  
  
 [<span data-ttu-id="1f9d5-106">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="1f9d5-106">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 <span data-ttu-id="1f9d5-107">Dans l’exemple suivant, la `Alias` est utilisé pour fournir le nom de la fonction dans advapi32.dll, `GetUserNameA`, qui `getUserName` est utilisé à la place de dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-107">In the following example, the `Alias` keyword is used to provide the name of the function in advapi32.dll, `GetUserNameA`, that `getUserName` is used in place of in this example.</span></span> <span data-ttu-id="1f9d5-108">Fonction `getUserName` est appelée dans un sub `getUser`, qui affiche le nom de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-108">Function `getUserName` is called in sub `getUser`, which displays the name of the current user.</span></span>  
  
 [!code-vb[VbVbalrStatements#15](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/alias-clause_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="1f9d5-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f9d5-109">See Also</span></span>  
 [<span data-ttu-id="1f9d5-110">Mots clés</span><span class="sxs-lookup"><span data-stu-id="1f9d5-110">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
