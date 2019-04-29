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
ms.openlocfilehash: 10f67c02d25ec275d1c3e98197d51c25aa250c19
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61955504"
---
# <a name="visual-basic-limitations"></a>Restrictions liées à Visual Basic
Les versions antérieures de Visual Basic imposaient des limites dans le code, tel que la longueur des noms de variables, le nombre de variables autorisé dans les modules et la taille du module. Dans Visual Basic .NET, ces restrictions ont été moins stricte, ce qui vous donne une plus grande liberté d’écriture et d’organisation de votre code.  
  
 Les limites physiques dépendent de plus de mémoire d’exécution que sur les considérations relatives à la compilation. Si vous utilisez des pratiques de programmation prudentes et divisez des applications volumineuses en plusieurs classes et les modules, il est très peu de chance de rencontrer une limitation de Visual Basic interne.  
  
 Voici quelques limitations que vous pouvez rencontrer dans les cas extrêmes :  
  
- **Longueur du nom.** Il est un nombre maximal de caractères pour le nom de chaque élément de programmation déclaré. Cette limite s’applique à une chaîne de qualification entière si le nom de l’élément est qualifié. Consultez [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
- **Longueur de ligne.** Il existe un maximum de 65 535 caractères dans une ligne de code source physique. La ligne de code source logique peut être plus longue si vous utilisez des caractères de continuation de ligne. Voir [Guide pratique pour Diviser et combiner des instructions dans le Code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md).  
  
- **Dimensions du tableau.** Il est un nombre maximal de dimensions, que vous pouvez déclarer un tableau. Cela limite le nombre d’index que vous pouvez utiliser pour spécifier un élément de tableau. Consultez [Array Dimensions in Visual Basic](../../../visual-basic/programming-guide/language-features/arrays/array-dimensions.md).  
  
- **Longueur de chaîne.** Il est un nombre maximal de caractères Unicode que vous pouvez stocker dans une chaîne unique. Consultez [Type de données chaîne](../../../visual-basic/language-reference/data-types/string-data-type.md).  
  
- **Longueur de chaîne d’environnement.** Il existe un maximum de 32 768 caractères pour n’importe quelle chaîne d’environnement utilisée comme un argument de ligne de commande. Il s’agit d’une limitation sur toutes les plateformes.  
  
## <a name="see-also"></a>Voir aussi

- [Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [Conventions d’affectation de noms de Visual Basic](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
