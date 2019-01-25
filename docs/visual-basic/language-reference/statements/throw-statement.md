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
ms.openlocfilehash: 9af1436af950346eef572c34b9d42da3e8c8cf24
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671159"
---
# <a name="throw-statement-visual-basic"></a>Throw, instruction (Visual Basic)
Lève une exception dans une procédure.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Throw [ expression ]  
```  
  
## <a name="part"></a>Élément  
 `expression`  
 Fournit des informations relatives à l’exception levée. Facultatif quand elles se trouvent dans un `Catch` instruction, sinon requise.  
  
## <a name="remarks"></a>Notes  
 Le `Throw` instruction lève une exception que vous pouvez gérer avec le code de gestion des exceptions structurée (`Try`... `Catch`... `Finally`) ou le code de gestion des exceptions structurée (`On Error GoTo`). Vous pouvez utiliser la `Throw` instruction pour intercepter les erreurs dans votre code, car Visual Basic remonte la pile des appels jusqu'à ce qu’il trouve le code de gestion des exceptions approprié.  
  
 Un `Throw` instruction sans expression ne peut être utilisée que dans un `Catch` instruction, dans lequel l’instruction case lève à nouveau l’exception qui est gérée par le `Catch` instruction.  
  
 Le `Throw` instruction réinitialise la pile des appels pour le `expression` exception. Si `expression` n’est pas fourni, la pile des appels reste inchangé. Vous pouvez accéder à la pile des appels pour l’exception via la <xref:System.Exception.StackTrace%2A> propriété.  
  
## <a name="example"></a>Exemple  
 Le code suivant utilise la `Throw` instruction pour lever une exception :  
  
 [!code-vb[VbVbalrStatements#84](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/throw-statement_1.vb)]  
  
## <a name="requirements"></a>Spécifications  
 **Espace de noms :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)  
  
 **Module :** `Interaction`  
  
 **Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)  
  
## <a name="see-also"></a>Voir aussi
- [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [On Error (instruction)](../../../visual-basic/language-reference/statements/on-error-statement.md)
