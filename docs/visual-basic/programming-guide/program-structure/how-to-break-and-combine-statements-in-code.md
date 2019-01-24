---
title: 'Procédure : Diviser et combiner des instructions dans le Code (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb._
helpviewer_keywords:
- colons (:)
- line continuation
- _ line-continuation character
- ': line separator character'
- Visual Basic code, line breaks in
- Visual Basic code, line breaks
- Visual Basic code, line continuation
- long lines of code
- line terminator
- line-continuation sequence
- underscores [Visual Basic], in code
- statements [Visual Basic], line continuation in
- line breaks [Visual Basic], in code
- line-continuation character [Visual Basic]
- Visual Basic code, line continuation in
- statements [Visual Basic], line breaks in
ms.assetid: dea01dad-a8ac-484a-bb3a-8c45a1b1eccc
ms.openlocfilehash: b19c36018a0938b9b6546e5baefbbc3de1e5dd30
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54619913"
---
# <a name="how-to-break-and-combine-statements-in-code-visual-basic"></a>Procédure : Diviser et combiner des instructions dans le Code (Visual Basic)
Lorsque vous écrivez votre code, vous pouvez parfois créer de longues instructions qui imposent un défilement horizontal dans l’éditeur de Code. Bien que cela n’affecte pas la façon votre code s’exécute, elle rend difficile pour vous ou quelqu'un d’autre lire le code tel qu’il apparaît sur le moniteur. Dans ce cas, vous devez envisager de diviser l’instruction long unique en plusieurs lignes.  
  
### <a name="to-break-a-single-statement-into-multiple-lines"></a>Pour diviser une instruction unique en plusieurs lignes  
  
-   Utiliser le caractère de continuation de ligne, qui est un trait de soulignement (`_`), au point auquel vous souhaitez que la saut de ligne. Le trait de soulignement doit être immédiatement précédé d’un espace et immédiatement suivi d’un terminateur de ligne (retour chariot).  
  
    > [!NOTE]
    >  Dans certains cas, si vous omettez le caractère de continuation de ligne, le compilateur Visual Basic implicitement continue l’instruction sur la ligne de code suivante. Pour obtenir la liste d’éléments de syntaxe pour laquelle vous pouvez omettre le caractère de continuation de ligne, consultez « Continuation de ligne implicite » dans [instructions](../../../visual-basic/programming-guide/language-features/statements.md).  
  
     Dans l’exemple suivant, l’instruction est divisée en quatre lignes avec des caractères de continuation de ligne terminant toutes les mais la dernière ligne.  
  
     [!code-vb[VbVbcnConventions#20](../../../visual-basic/programming-guide/language-features/codesnippet/VisualBasic/how-to-break-and-combine-statements-in-code_1.vb)]  
  
     À l’aide de cette séquence rend votre code plus facile à lire, à la fois en ligne et quand imprimé.  
  
     Le caractère de continuation de ligne doit être le dernier caractère d’une ligne. Vous ne pouvez pas faire suivre avec un autre élément sur la même ligne.  
  
     Il existe des restrictions quant à l’endroit où vous pouvez utiliser le caractère de continuation de ligne ; par exemple, vous ne pouvez pas l’utiliser au milieu d’un nom d’argument. Vous pouvez interrompre une liste d’arguments avec le caractère de continuation de ligne, mais les noms des arguments individuels doivent rester intactes.  
  
     Vous ne pouvez pas continuer un commentaire à l’aide d’un caractère de continuation de ligne. Le compilateur n’examine les caractères dans un commentaire pour une signification spéciale. Pour un commentaire de plusieurs lignes, répétez le symbole de commentaire (`'`) sur chaque ligne.  
  
 Bien que la méthode recommandée consiste à placer chaque instruction sur une ligne distincte, Visual Basic vous permet également de placer plusieurs instructions sur la même ligne.  
  
### <a name="to-place-multiple-statements-on-the-same-line"></a>Placer plusieurs instructions sur la même ligne  
  
-   Séparez les instructions par un signe deux-points (`:`), comme dans l’exemple suivant.  
  
     [!code-vb[VbVbcnConventions#10](../../../visual-basic/programming-guide/language-features/codesnippet/VisualBasic/how-to-break-and-combine-statements-in-code_2.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
