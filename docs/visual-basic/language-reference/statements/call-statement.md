---
title: Call, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Call
helpviewer_keywords:
- procedures [Visual Basic], Call statement
- Call statement [Visual Basic]
- procedures [Visual Basic], calling
ms.assetid: e5b31571-6867-406f-b8e7-a3f9aae4723a
ms.openlocfilehash: 755443a99a1ad8b0430a76d2dba1ff27472d4c9d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61945065"
---
# <a name="call-statement-visual-basic"></a>Call, instruction (Visual Basic)
Transfère le contrôle à un `Function`, `Sub`, ou de la procédure de la bibliothèque de liens dynamiques (DLL).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
[ Call ] procedureName [ (argumentList) ]  
```  
  
## <a name="parts"></a>Composants  
|||
|---|---|
|`procedureName`|Obligatoire. Nom de la procédure à appeler.|
|`argumentList`|Optionnel. Liste des variables ou expressions représentant les arguments passés à la procédure lorsqu’elle est appelée. Plusieurs arguments sont séparés par des virgules. Si vous incluez `argumentList`, vous devez le placer entre parenthèses.|
|||
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser le `Call` mot clé lorsque vous appelez une procédure. Pour la plupart des appels de procédure, vous n’êtes pas obligé d’utiliser ce mot clé.  
  
 Vous utilisez généralement le `Call` mot clé lorsque l’expression appelée ne commence pas par un identificateur. Utilisation de la `Call` mot clé pour d’autres utilisations n’est pas recommandé.  
  
 Si la procédure retourne une valeur, la `Call` instruction ignore.  
  
## <a name="example"></a>Exemple  
 Le code suivant montre deux exemples où le `Call` mot clé est nécessaire pour appeler une procédure. Dans les deux exemples, l’expression appelée ne commence pas par un identificateur.  
  
 [!code-vb[VbVbalrStatements#97](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#97)]  
  
## <a name="see-also"></a>Voir aussi

- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)
- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
- [Expressions lambda](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
