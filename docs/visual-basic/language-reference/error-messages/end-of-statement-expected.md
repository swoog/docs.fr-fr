---
title: Fin d'instruction attendue
ms.date: 07/20/2015
f1_keywords:
- bc30205
- vbc30205
helpviewer_keywords:
- BC30205
ms.assetid: 53c7f825-a737-4b76-a1fa-f67745b8bd40
ms.openlocfilehash: 7b91d13cbcb9d211d4ca18c8e48c7494bf6eccc6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33588078"
---
# <a name="end-of-statement-expected"></a>Fin d'instruction attendue
L’instruction est syntaxiquement complète, mais un élément de programmation supplémentaire suit l’élément qui termine l’instruction. Un terminateur de ligne est requis à la fin de chaque instruction.
  
 Un terminateur de ligne divise les caractères d’un fichier source Visual Basic en lignes. Exemples d’indicateurs de fin de ligne sont le Unicode chariot retour (& HD), le Unicode saut de ligne (& HA), et le suivi du caractère de saut de ligne Unicode des caractères de retour chariot Unicode. Pour plus d’informations sur les indicateurs de fin de ligne, consultez la [spécification du langage Visual Basic](../../../visual-basic/reference/language-specification/index.md).
  
 **ID d’erreur :** BC30205
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur
  
1.  Vérifiez si deux instructions différentes ont été placées par inadvertance sur la même ligne.
  
2.  Insérer une marque de fin de ligne après l’élément qui termine l’instruction.
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique : diviser et combiner des instructions dans le code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)  
 [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
