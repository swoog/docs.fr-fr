---
title: Throw, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Throw
helpviewer_keywords:
- structured exception handling, throw statements
- try-catch exception handling, throw statements
- throw statement [Visual Basic], about throw statements
- throwing exceptions, throw statement
- exception handling, throw statement
- On Error statement [Visual Basic], throwing exceptions
- throwing exceptions
- exception handling, unstructured
- throw statement [Visual Basic]
ms.assetid: a6e07406-5c8a-4498-87a2-8339f3651d62
ms.openlocfilehash: cfa53b3585846da25711739fb7af4bde21746b29
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="throw-statement-visual-basic"></a>Throw, instruction (Visual Basic)
Lève une exception dans une procédure.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Throw [ expression ]  
```  
  
## <a name="part"></a>Élément  
 `expression`  
 Fournit des informations relatives à l’exception levée. Facultatif lorsqu’il réside dans un `Catch` instruction, requise dans le cas contraire.  
  
## <a name="remarks"></a>Notes  
 Le `Throw` instruction lève une exception que vous pouvez gérer à l’aide du code de gestion des exceptions structurée (`Try`... `Catch`... `Finally`) ou le code de gestion des exceptions structurée (`On Error GoTo`). Vous pouvez utiliser la `Throw` instruction pour intercepter les erreurs dans votre code, car Visual Basic monte dans la pile des appels jusqu'à ce qu’il trouve le code de gestion des exceptions approprié.  
  
 A `Throw` instruction sans expression peut uniquement être utilisée dans un `Catch` instruction, dans lequel cas l’instruction lève à nouveau l’exception qui est gérée par le `Catch` instruction.  
  
 Le `Throw` instruction rétablit la pile des appels pour le `expression` exception. Si `expression` n’est pas fourni, la pile des appels reste inchangé. Vous pouvez accéder à la pile des appels de l’exception via la <xref:System.Exception.StackTrace%2A> propriété.  
  
## <a name="example"></a>Exemple  
 Le code suivant utilise la `Throw` instruction pour lever une exception :  
  
 [!code-vb[VbVbalrStatements#84](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/throw-statement_1.vb)]  
  
## <a name="requirements"></a>Spécifications  
 **Namespace :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)  
  
 **Module :** `Interaction`  
  
 **Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)  
  
## <a name="see-also"></a>Voir aussi  
 [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
 [On Error (instruction)](../../../visual-basic/language-reference/statements/on-error-statement.md)
