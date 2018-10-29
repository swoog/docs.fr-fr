---
title: Fin d'instruction attendue
ms.date: 07/20/2015
f1_keywords:
- bc30205
- vbc30205
helpviewer_keywords:
- BC30205
ms.assetid: 53c7f825-a737-4b76-a1fa-f67745b8bd40
ms.openlocfilehash: 8df756009ebe3a0613ec47018d938151829214df
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50198261"
---
# <a name="end-of-statement-expected"></a>Fin d'instruction attendue
L’instruction est syntaxiquement complète, mais un élément de programmation supplémentaire suit l’élément qui termine l’instruction. Un terminateur de ligne est nécessaire à la fin de chaque instruction.
  
 Un terminateur de ligne divise les caractères d’un fichier source Visual Basic en lignes. Exemples d’indicateurs de fin de ligne sont le Unicode chariot retour (& HD), le Unicode saut de ligne (& haute disponibilité), et Unicode retour chariot suivi du caractère de saut de ligne Unicode. Pour plus d’informations sur les indicateurs de fin de ligne, consultez le [spécification du langage Visual Basic](~/_vblang/spec/lexical-grammar.md#line-terminators).
  
 **ID d’erreur :** BC30205
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur
  
1.  Vérifiez si deux instructions différentes ont été placées par inadvertance sur la même ligne.
  
2.  Insérer un terminateur de ligne après l’élément qui se termine l’instruction.
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique : diviser et combiner des instructions dans le code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)  
 [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
