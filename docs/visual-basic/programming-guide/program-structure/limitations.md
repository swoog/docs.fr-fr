---
title: Restrictions liées à Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- limits
- limitations [Visual Basic]
- limitations
- limits, Visual Basic code
- Visual Basic code, limitations
ms.assetid: cf1646b7-5d24-48c6-9616-bda8a4849d91
ms.openlocfilehash: 57378c3aa18a5cc108c10e8654e55803f3cf9052
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33649927"
---
# <a name="visual-basic-limitations"></a>Restrictions liées à Visual Basic
Les versions antérieures de Visual Basic appliquées des limites dans le code, comme la longueur des noms de variables, le nombre de variables autorisé dans les modules et la taille du module. Dans Visual Basic .NET, ces restrictions ont été allégées, ce qui vous donne une plus grande liberté d’écriture et d’organisation de votre code.  
  
 Les limites physiques sont dépendants plus sur l’exécution de mémoire que sur les considérations relatives à la compilation. Si vous utilisez des pratiques de programmation prudentes et divisez de grandes applications en plusieurs classes et les modules, il est peu de risque de rencontrer une limitation interne de Visual Basic.  
  
 Voici quelques limitations que vous pouvez rencontrer dans les cas extrêmes :  
  
-   **Longueur du nom.** Il existe un nombre maximal de caractères pour le nom de chaque élément de programmation déclaré. Cette valeur maximale s’applique à une chaîne de qualification entière si le nom de l’élément est qualifié. Consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
-   **Longueur de ligne.** Il existe un maximum de 65 535 caractères dans une ligne physique de code source. La ligne de code source logique peut être plus longue si vous utilisez des caractères de continuation de ligne. Consultez [Comment : diviser et combiner des instructions dans le Code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md).  
  
-   **Dimensions du tableau.** Il existe un nombre maximal de dimensions, que vous pouvez déclarer un tableau. Cela limite le nombre d’index que vous pouvez utiliser pour spécifier un élément de tableau. Consultez [en Visual Basic, les Dimensions de tableau](../../../visual-basic/programming-guide/language-features/arrays/array-dimensions.md).  
  
-   **Longueur de chaîne.** Il existe un nombre maximal de caractères Unicode que vous pouvez stocker dans une chaîne unique. Consultez [Type de données chaîne](../../../visual-basic/language-reference/data-types/string-data-type.md).  
  
-   **Longueur de chaîne d’environnement.** Il existe un maximum de 32768 caractères pour toute chaîne d’environnement utilisée comme argument de ligne de commande. Il s’agit d’une limitation sur toutes les plateformes.  
  
## <a name="see-also"></a>Voir aussi  
 [Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)  
 [Conventions d’affectation de noms de Visual Basic](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
