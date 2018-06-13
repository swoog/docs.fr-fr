---
title: Order By, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryOrderBy
- vb.QueryAscending
- vb.QueryDescending
helpviewer_keywords:
- queries [Visual Basic], Order By
- Order By clause [Visual Basic]
- Order By statement [Visual Basic]
ms.assetid: fa911282-6b81-44c7-acfa-46b5bb93df75
ms.openlocfilehash: 7c60156ee81618530b42d5f61dbcac6f59c4f675
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33604118"
---
# <a name="order-by-clause-visual-basic"></a>Order By, clause (Visual Basic)
Spécifie l’ordre de tri pour un résultat de requête.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Order By orderExp1 [ Ascending | Descending ] [, orderExp2 [...] ]  
```  
  
## <a name="parts"></a>Composants  
 `orderExp1`  
 Obligatoire. Un ou plusieurs champs à partir du résultat de la requête qui identifient l’ordre des valeurs renvoyées. Les noms de champ doivent être séparés par des virgules (,). Vous pouvez identifier chaque champ de tri dans l’ordre croissant ou décroissant à l’aide de la `Ascending` ou `Descending` mots clés. Si aucun `Ascending` ou `Descending` mot clé est spécifié, l’ordre de tri par défaut est croissant. Les champs d’ordre de tri prévalent de gauche à droite.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser la `Order By` clause pour trier les résultats d’une requête. Le `Order By` clause peut trier seulement un résultat basé sur la variable de portée de l’étendue actuelle. Par exemple, le `Select` clause introduit une nouvelle portée dans une expression de requête avec de nouvelles variables d’itération pour cette étendue. Les variables définies avant de plage un `Select` clause dans une requête ne sont pas disponibles après la `Select` clause. Par conséquent, si vous souhaitez classer vos résultats par un champ qui n’est pas disponible dans le `Select` clause, vous devez placer le `Order By` clause avant le `Select` clause. Un exemple de lorsque vous devez pour cela est lorsque vous souhaitez trier votre requête en fonction de champs qui ne sont pas retournés en tant que partie du résultat.  
  
 Ordre croissant ou décroissant pour un champ est déterminé par l’implémentation de la <xref:System.IComparable> interface pour le type de données du champ. Si le type de données n’implémente pas le <xref:System.IComparable> interface, l’ordre de tri est ignoré.  
  
## <a name="example"></a>Exemple  
 La requête suivante expression utilise une `From` clause pour déclarer une variable de portée `book` pour la `books` collection. Le `Order By` clause trie les résultats de la requête par prix croissant (la valeur par défaut). La documentation avec le même prix est triée par titre dans l’ordre croissant. Le `Select` clause sélectionne le `Title` et `Price` propriétés comme valeurs retournées par la requête.  
  
 [!code-vb[VbSimpleQuerySamples#24](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_1.vb)]  
  
## <a name="example"></a>Exemple  
 La requête suivante expression utilise la `Order By` clause pour trier les résultats de la requête par prix dans l’ordre décroissant. La documentation avec le même prix est triée par titre dans l’ordre croissant.  
  
 [!code-vb[VbSimpleQuerySamples#25](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_2.vb)]  
  
## <a name="example"></a>Exemple  
 La requête suivante expression utilise un `Select` clause pour sélectionner le titre du livre, prix, date de publication et l’auteur. Il remplit ensuite le `Title`, `Price`, `PublishDate`, et `Author` champs de la variable de portée de la nouvelle étendue. Le `Order By` clause classe la nouvelle variable de portée par nom de l’auteur, titre de livre, puis par prix. Chaque colonne est triée dans l’ordre par défaut (croissant).  
  
 [!code-vb[VbSimpleQuerySamples#26](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_3.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [Requêtes](../../../visual-basic/language-reference/queries/queries.md)  
 [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)  
 [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
