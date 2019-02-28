---
title: Take, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryTake
helpviewer_keywords:
- Take statement [Visual Basic]
- queries [Visual Basic], Take
- Take clause [Visual Basic]
ms.assetid: 77bf87b2-1476-4456-957f-fee922fbad8c
ms.openlocfilehash: 2705b61f4ebc839a9db98f037f303b4df78bbe5f
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56976211"
---
# <a name="take-clause-visual-basic"></a>Take, clause (Visual Basic)
Retourne un nombre spécifié d'éléments contigus à partir du début d'une collection.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Take count  
```  
  
## <a name="parts"></a>Composants  
 `count`  
 Obligatoire. Une valeur ou une expression qui correspond au nombre d’éléments de la séquence à retourner.  
  
## <a name="remarks"></a>Notes  
 Le `Take` clause entraîne une requête inclure un nombre spécifié d’éléments contigus à partir du début d’une liste de résultats. Le nombre d’éléments à inclure est spécifié par le `count` paramètre.  
  
 Vous pouvez utiliser la `Take` clause avec le `Skip` clause pour retourner une plage de données à partir de n’importe quel segment d’une requête. Pour ce faire, passez à l’index du premier élément de la plage à la `Skip` clause et la taille de la plage à la `Take` clause. Dans ce cas, le `Take` clause doit être spécifiée après le `Skip` clause.  
  
 Lorsque vous utilisez le `Take` clause dans une requête, vous devez également vous assurer que les résultats sont retournés dans un ordre qui permettra la `Take` clause pour inclure les résultats prévus. Pour plus d’informations sur le classement des résultats de la requête, consultez [Clause Order By](../../../visual-basic/language-reference/queries/order-by-clause.md).  
  
 Vous pouvez utiliser le `TakeWhile` clause pour spécifier que seuls certains éléments soient retournés, selon une condition fournie.  
  
## <a name="example"></a>Exemple  
 Le code suivant exemple utilise le `Take` clause conjointement avec le `Skip` clause pour retourner des données à partir d’une requête dans les pages. La fonction GetCustomers utilise le `Skip` clause pour ignorer les clients dans la liste jusqu'à ce que le départ fournie valeur d’index et utilise le `Take` clause pour retourner une page de clients à partir de cette valeur d’index.  
  
 [!code-vb[VbSimpleQuerySamples#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Order By (clause)](../../../visual-basic/language-reference/queries/order-by-clause.md)
- [Take While (clause)](../../../visual-basic/language-reference/queries/take-while-clause.md)
- [Skip (clause)](../../../visual-basic/language-reference/queries/skip-clause.md)
