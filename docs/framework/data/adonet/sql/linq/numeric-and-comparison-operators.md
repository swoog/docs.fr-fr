---
title: Opérateurs de comparaison et opérateurs numériques
ms.date: 03/30/2017
ms.assetid: 25b4a26a-06f2-4f80-87a9-76705ed46197
ms.openlocfilehash: 9b31fd2d819afbb1e589ad74f23ec139830c68b8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212165"
---
# <a name="numeric-and-comparison-operators"></a>Opérateurs de comparaison et opérateurs numériques
Les opérateurs arithmétiques et de comparaison fonctionnent conformément aux attentes dans le Common Language Runtime (CLR), à l'exception des points suivants :  
  
-   SQL ne prend pas en charge l'opérateur modulo sur les nombres à virgule flottante.  
  
-   SQL ne prend pas en charge l'arithmétique non contrôlée.  
  
-   Les opérateurs d'incrémentation et de décrémentation ne sont pas pris en charge car ils présentent des effets secondaires lorsqu'ils sont utilisés dans des expressions qui ne peuvent pas être répliquées dans SQL.  
  
## <a name="supported-operators"></a>Opérateurs pris en charge  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] prend en charge les opérateurs suivants.  
  
-   Opérateurs arithmétiques de base :  
  
    -   `+`  
  
    -   `-` (soustraction)  
  
    -   `*`  
  
    -   `/`  
  
    -   Division d'entier Visual Basic (`\`)  
  
    -   `%` (`Mod` Visual Basic)  
  
    -   `<<`  
  
    -   `>>`  
  
    -   `-` (négation unaire)  
  
-   Opérateurs de comparaison de base :  
  
    -   `=` Visual Basic et `==` C#  
  
    -   `<>` Visual Basic et `!=` C#  
  
    -   Visual Basic `Is/IsNot`  
  
    -   `<`  
  
    -   `<=`  
  
    -   `>`  
  
    -   `>=`  
  
## <a name="see-also"></a>Voir aussi

- [Fonctions et types de données](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
- [Opérateurs C#](../../../../../../docs/csharp/language-reference/operators/index.md)
- [Opérateurs](../../../../../visual-basic/language-reference/operators/index.md)
