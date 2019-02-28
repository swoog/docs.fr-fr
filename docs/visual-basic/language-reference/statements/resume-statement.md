---
title: Resume, instruction (Visual Basic)
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
ms.openlocfilehash: fcb50a9c7e36bab046be25d7f82f91cfe0f9be8e
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56966916"
---
# <a name="resume-statement"></a>Resume, instruction
Reprend l’exécution une fois une routine de gestion des erreurs est terminée.  
  
 Nous vous suggérons d’utiliser Gestion structurée des exceptions dans votre code autant que possible, plutôt que d’à l’aide de la gestion non structurée et `On Error` et `Resume` instructions. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Resume [ Next | line ]  
```  
  
## <a name="parts"></a>Composants  
 `Resume`  
 Obligatoire. Si l’erreur s’est produite dans la même procédure que le Gestionnaire d’erreurs, l’exécution reprend avec l’instruction qui a provoqué l’erreur. Si l’erreur s’est produite dans une procédure appelée, l’exécution reprend à l’instruction qui a appelé la procédure contenant la routine de gestion des erreurs.  
  
 `Next`  
 Facultatif. Si l’erreur s’est produite dans la même procédure que le Gestionnaire d’erreurs, l’exécution reprend avec l’instruction qui suit immédiatement l’instruction ayant provoqué l’erreur. Si l’erreur s’est produite dans une procédure appelée, l’exécution se poursuit avec l’instruction qui suit immédiatement l’instruction qui a appelé la procédure contenant la routine de gestion des erreurs (ou `On Error Resume Next` instruction).  
  
 `line`  
 Facultatif. L’exécution reprend à la ligne spécifiée dans le champ obligatoire `line` argument. Le `line` argument est une étiquette de ligne ou un numéro de ligne et doit se trouver dans la même procédure que le Gestionnaire d’erreurs.  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Nous vous recommandons d’utiliser Gestion structurée des exceptions dans votre code autant que possible, plutôt que d’à l’aide de la gestion non structurée et `On Error` et `Resume` instructions. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
 Si vous utilisez un `Resume` instruction n’importe où autre que dans une routine de gestion des erreurs, une erreur se produit.  
  
 Le `Resume` instruction ne peut pas être utilisée dans une procédure qui contient un `Try...Catch...Finally` instruction.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise la `Resume` instruction à la fin dans une procédure de gestion des erreurs et de reprendre l’exécution avec l’instruction qui a provoqué l’erreur. Erreur numéro 55 est générée pour illustrer l’utilisation de la `Resume` instruction.  
  
 [!code-vb[VbVbalrErrorHandling#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrErrorHandling/VB/Class1.vb#16)]  
  
## <a name="requirements"></a>Spécifications  
 **Espace de noms :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)  
  
 **Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)  
  
## <a name="see-also"></a>Voir aussi
- [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [Error (instruction)](../../../visual-basic/language-reference/statements/error-statement.md)
- [On Error (instruction)](../../../visual-basic/language-reference/statements/on-error-statement.md)
