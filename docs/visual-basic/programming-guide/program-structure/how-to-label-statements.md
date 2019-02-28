---
title: 'Procédure : Instructions de l’étiquette (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- colons (:)
- statements [Visual Basic], labels
- ': separator character'
- Visual Basic code, labeling statements
ms.assetid: 38f1ff43-2054-42cb-963b-1998e60c6ed4
ms.openlocfilehash: 2f6f0362fcec170e677d153ad9f936a5c2e55ad7
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56981203"
---
# <a name="how-to-label-statements-visual-basic"></a>Procédure : Instructions de l’étiquette (Visual Basic)
Blocs d’instructions sont constituées de lignes de code délimités par le signe deux-points. Lignes de code, précédé d’une chaîne ou entier identifiant sont dites *intitulée*. Les étiquettes d’instruction sont utilisées pour marquer une ligne de code pour identifier pour une utilisation avec des instructions telles que `On Error Goto`.  
  
 Les étiquettes peuvent être soit des identificateurs Visual Basic valides, telles que celles qui identifient les éléments de programmation, ou les littéraux d’entier. Une étiquette doit apparaître au début d’une ligne de code source et doit être suivie par un signe deux-points, indépendamment de si elle est suivie par une instruction sur la même ligne.  
  
 Le compilateur identifie les étiquettes en vérifiant si le début de la ligne correspond à n’importe quel identificateur déjà défini. Si elle n’est pas le cas, le compilateur suppose que c’est une étiquette.  
  
 Les étiquettes ont leur propre espace de déclaration et n’interfèrent pas avec d’autres identificateurs. Portée d’une étiquette est le corps de la méthode. Déclaration d’étiquette est prioritaire dans une situation ambiguë.  
  
> [!NOTE]
>  Étiquettes peuvent être utilisées uniquement sur des instructions exécutables à l’intérieur de méthodes.  
  
### <a name="to-label-a-line-of-code"></a>Pour étiqueter une ligne de code  
  
-   Placez un identificateur, suivi d’un signe deux-points, au début de la ligne de code source.  
  
     Par exemple, les lignes de code suivantes sont étiquetés avec `Jump` et `120`, respectivement :  
  
     [!code-vb[VbVbalrStatements#708](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#708)]  
  
## <a name="see-also"></a>Voir aussi
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
- [Noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
