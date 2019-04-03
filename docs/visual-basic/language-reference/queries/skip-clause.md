---
title: Skip, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QuerySkip
helpviewer_keywords:
- queries [Visual Basic], Skip
- Skip statement [Visual Basic]
- Skip clause [Visual Basic]
ms.assetid: f00eb172-3907-4c43-9745-d8546ab86234
ms.openlocfilehash: db2d79596895505ddaa7778e831082a94c7ad44e
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58821099"
---
# <a name="skip-clause-visual-basic"></a>Skip, clause (Visual Basic)
Ignore un nombre spécifié d’éléments dans une collection, puis retourne les éléments restants.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Skip count  
```  
  
## <a name="parts"></a>Composants  
 `count`  
 Obligatoire. Une valeur ou une expression qui correspond au nombre d’éléments de la séquence à ignorer.  
  
## <a name="remarks"></a>Notes  
 Le `Skip` clause entraîne une requête à ignorer des éléments au début d’une liste de résultats et de retourner les éléments restants. Le nombre d’éléments à ignorer est identifié par le `count` paramètre.  
  
 Vous pouvez utiliser la `Skip` clause avec le `Take` clause pour retourner une plage de données à partir de n’importe quel segment d’une requête. Pour ce faire, passez à l’index du premier élément de la plage à la `Skip` clause et la taille de la plage à la `Take` clause.  
  
 Lorsque vous utilisez le `Skip` clause dans une requête, vous devez également vous assurer que les résultats sont retournés dans un ordre qui permettra la `Skip` clause pour ignorer les résultats prévus. Pour plus d’informations sur le classement des résultats de la requête, consultez [Clause Order By](../../../visual-basic/language-reference/queries/order-by-clause.md).  
  
 Vous pouvez utiliser le `SkipWhile` clause pour spécifier que seuls certains éléments sont ignorés, selon une condition fournie.  
  
## <a name="example"></a>Exemple  
 Le code suivant exemple utilise le `Skip` clause conjointement avec le `Take` clause pour retourner des données à partir d’une requête dans les pages. Le `GetCustomers` fonction utilise le `Skip` clause pour ignorer les clients dans la liste jusqu'à ce que le départ fournie valeur d’index et utilise le `Take` clause pour retourner une page de clients à partir de cette valeur d’index.  
  
 [!code-vb[VbSimpleQuerySamples#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Order By (clause)](../../../visual-basic/language-reference/queries/order-by-clause.md)
- [Skip While (clause)](../../../visual-basic/language-reference/queries/skip-while-clause.md)
- [Take (clause)](../../../visual-basic/language-reference/queries/take-clause.md)
