---
title: Resume, instruction
ms.date: 07/20/2015
f1_keywords:
- vb.Resume
- vb.ResumeNext
helpviewer_keywords:
- Next statement [Visual Basic], Resume
- Resume Next statement [Visual Basic]
- execution [Visual Basic], resuming
- run-time errors [Visual Basic], resuming after
- Resume statement [Visual Basic], syntax
- errors [Visual Basic], resuming after
- Error statement [Visual Basic], and Resume statement
- execution
- Resume statement [Visual Basic]
ms.assetid: e24d058b-1a5c-4274-acb9-7d295d3ea537
ms.openlocfilehash: 1d03f631893be51529f29af824de0d684bf43804
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33603780"
---
# <a name="resume-statement"></a>Resume, instruction
Reprend l’exécution après qu’une routine de gestion des erreurs est terminée.  
  
 Nous vous suggérons d’utiliser la gestion structurée des exceptions dans votre code autant que possible, au lieu d’utiliser la gestion des exceptions structurées et `On Error` et `Resume` instructions. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Resume [ Next | line ]  
```  
  
## <a name="parts"></a>Composants  
 `Resume`  
 Obligatoire. Si l’erreur s’est produite dans la même procédure que le Gestionnaire d’erreurs, l’exécution se poursuit avec l’instruction qui a provoqué l’erreur. Si l’erreur s’est produite dans une procédure appelée, l’exécution reprend à l’instruction qui a appelé la procédure contenant la routine de gestion des erreurs.  
  
 `Next`  
 Facultatif. Si l’erreur s’est produite dans la même procédure que le Gestionnaire d’erreurs, l’exécution se poursuit avec l’instruction qui suit immédiatement l’instruction ayant provoqué l’erreur. Si l’erreur s’est produite dans une procédure appelée, l’exécution se poursuit avec l’instruction qui suit l’instruction qui a appelé la procédure contenant la routine de gestion des erreurs (ou `On Error Resume Next` instruction).  
  
 `line`  
 Facultatif. L’exécution se poursuit à la ligne spécifiée dans le champ obligatoire `line` argument. Le `line` argument est une étiquette de ligne ou un numéro de ligne et doit se trouver dans la même procédure que le Gestionnaire d’erreurs.  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Nous vous recommandons d’utiliser Gestion structurée des exceptions dans votre code autant que possible, au lieu d’utiliser la gestion des exceptions structurées et `On Error` et `Resume` instructions. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
 Si vous utilisez un `Resume` instruction n’importe où autre que dans une routine de gestion des erreurs, une erreur se produit.  
  
 Le `Resume` instruction ne peut pas être utilisée dans une procédure qui contient un `Try...Catch...Finally` instruction.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise la `Resume` instruction pour terminer la gestion des erreurs dans une procédure, puis reprend l’exécution avec l’instruction qui a provoqué l’erreur. L’erreur numéro 55 est générée pour illustrer l’utilisation de la `Resume` instruction.  
  
 [!code-vb[VbVbalrErrorHandling#16](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/resume-statement_1.vb)]  
  
## <a name="requirements"></a>Spécifications  
 **Namespace :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)  
  
 **Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)  
  
## <a name="see-also"></a>Voir aussi  
 [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
 [Error (instruction)](../../../visual-basic/language-reference/statements/error-statement.md)  
 [On Error (instruction)](../../../visual-basic/language-reference/statements/on-error-statement.md)
