---
title: La variable de portée '<variable>' masque une variable dans un bloc englobant, une variable de portée précédemment définie ou une variable déclarée implicitement dans une expression de requête
ms.date: 07/20/2015
f1_keywords:
- bc36633
- vbc36633
helpviewer_keywords:
- BC36633
ms.assetid: 5d5470e4-3de5-49c2-8831-1087625f4a77
ms.openlocfilehash: e31f728de228bea743f6c7b5cbfef3cd73367262
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61971626"
---
# <a name="range-variable-variable-hides-a-variable-in-an-enclosing-block-a-previously-defined-range-variable-or-an-implicitly-declared-variable-in-a-query-expression"></a>Variable de portée \<variable > masque une variable dans un bloc englobant, une variable de portée précédemment définie ou une variable déclarée implicitement dans une expression de requête
Un nom de variable de plage spécifié dans un `Select`, `From`, `Aggregate`, ou `Let` clause duplique le nom d’une variable de portée spécifié précédemment dans la requête ou le nom d’une variable qui est déclaré implicitement par la requête, comme un nom de champ ou le nom d’une fonction d’agrégation.  
  
 **ID d’erreur :** BC36633  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Assurez-vous que toutes les variables de plage dans une étendue de requête particulière ont des noms uniques. Vous pouvez placer une requête entre parenthèses pour garantir que les requêtes imbriquées ont une étendue unique.  
  
## <a name="see-also"></a>Voir aussi

- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Let (clause)](../../../visual-basic/language-reference/queries/let-clause.md)
- [Aggregate (clause)](../../../visual-basic/language-reference/queries/aggregate-clause.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
