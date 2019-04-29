---
title: REM, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.'
- vb.Rem
- Rem
- "'"
helpviewer_keywords:
- REM statement [Visual Basic]
- comments, Visual Basic code
- code comments, Visual Basic
- Visual Basic code, comments
- "' comment marker character [Visual Basic]"
ms.assetid: 34126d7f-e0f9-476d-91e6-b31b398615dc
ms.openlocfilehash: 3c63c5613b40cb2014c77a0a996e3acb2cc304d4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783931"
---
# <a name="rem-statement-visual-basic"></a>REM, instruction (Visual Basic)
Permet d’inclure des notes explicatives dans le code source d’un programme.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
REM comment  
' comment  
```  
  
## <a name="parts"></a>Composants  
 `comment`  
 Optionnel. Le texte des commentaires que vous souhaitez inclure. Un espace est nécessaire entre le `REM` mot clé et `comment`.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez placer un `REM` instruction seule sur une ligne, ou vous pouvez le placer sur une ligne qui suit une autre instruction. La `REM` instruction doit être la dernière instruction sur la ligne. Si elle suit une autre instruction, le `REM` doivent être séparés de cette instruction par un espace.  
  
 Vous pouvez utiliser un guillemet unique (`'`) au lieu de `REM`. Cela est vrai si votre commentaire suit une autre instruction sur la même ligne ou se trouve uniquement sur une ligne.  
  
> [!NOTE]
>  Vous ne pouvez pas continuer une `REM` instruction à l’aide d’une séquence de continuation de ligne (`_`). Une fois un commentaire démarré, le compilateur n’examine pas les caractères pour une signification spéciale. Un commentaire de plusieurs lignes, utilisez un autre `REM` instruction ou un symbole de commentaire (`'`) sur chaque ligne.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre la `REM` instruction, qui est utilisée pour inclure des notes explicatives dans un programme. Il montre également d’utiliser le caractère guillemet simple (`'`) au lieu de `REM`.  
  
 [!code-vb[VbVbalrStatements#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>Voir aussi

- [Commentaires dans le code](../../../visual-basic/programming-guide/program-structure/comments-in-code.md)
- [Guide pratique pour diviser et combiner des instructions dans le code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
