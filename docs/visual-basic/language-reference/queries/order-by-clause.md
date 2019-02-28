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
ms.openlocfilehash: 1d9055796687f828cc173a78feb9918cbf70bbd8
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56976367"
---
# <a name="order-by-clause-visual-basic"></a>Order By, clause (Visual Basic)
Spécifie l’ordre de tri pour un résultat de requête.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Order By orderExp1 [ Ascending | Descending ] [, orderExp2 [...] ]  
```  
  
## <a name="parts"></a>Composants  
 `orderExp1`  
 Obligatoire. Un ou plusieurs champs à partir du résultat de requête en cours qui identifient de manière de classer les valeurs retournées. Les noms de champs doivent être séparés par des virgules (,). Vous pouvez identifier chaque champ comme étant trié dans l’ordre croissant ou décroissant à l’aide de la `Ascending` ou `Descending` mots clés. Si aucun `Ascending` ou `Descending` mot clé est spécifié, l’ordre de tri par défaut est croissant. Les champs d’ordre de tri prévalent de gauche à droite.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser le `Order By` clause pour trier les résultats d’une requête. Le `Order By` clause peut trier seulement un résultat basé sur la variable de portée pour la portée actuelle. Par exemple, le `Select` clause introduit une nouvelle étendue dans une expression de requête avec de nouvelles variables d’itération pour cette portée. Plage des variables définies avant une `Select` clause dans une requête ne sont pas disponibles après la `Select` clause. Par conséquent, si vous souhaitez classer vos résultats par un champ qui n’est pas disponible dans le `Select` clause, vous devez placer le `Order By` clause avant le `Select` clause. Un exemple de lorsque vous seriez obligé de le faire est lorsque vous souhaitez trier votre requête par champs qui ne sont pas retournées dans le cadre du résultat.  
  
 Ordre croissant ou décroissant pour un champ est déterminé par l’implémentation de la <xref:System.IComparable> interface pour le type de données du champ. Si le type de données n’implémente pas le <xref:System.IComparable> interface, l’ordre de tri est ignoré.  
  
## <a name="example"></a>Exemple  
 La requête suivante expression utilise un `From` clause pour déclarer une variable de portée `book` pour le `books` collection. Le `Order By` clause trie les résultats de la requête par prix croissant (valeur par défaut). La documentation avec le même prix est triée par titre dans l’ordre croissant. Le `Select` clause sélectionne le `Title` et `Price` propriétés que les valeurs retournées par la requête.  
  
 [!code-vb[VbSimpleQuerySamples#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#24)]  
  
## <a name="example"></a>Exemple  
 La requête suivante expression utilise le `Order By` clause pour trier le résultat de la requête par prix dans l’ordre décroissant. La documentation avec le même prix est triée par titre dans l’ordre croissant.  
  
 [!code-vb[VbSimpleQuerySamples#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#25)]  
  
## <a name="example"></a>Exemple  
 La requête suivante expression utilise un `Select` clause pour sélectionner le titre du livre, prix, date de publication et l’auteur. Il remplit ensuite le `Title`, `Price`, `PublishDate`, et `Author` champs de la variable de portée de la nouvelle étendue. Le `Order By` clause trie la nouvelle variable de portée de nom de l’auteur, titre de livre et ensuite le prix. Chaque colonne est triée dans l’ordre par défaut (croissant).  
  
 [!code-vb[VbSimpleQuerySamples#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#26)]  
  
## <a name="see-also"></a>Voir aussi
- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [Select (clause)](../../../visual-basic/language-reference/queries/select-clause.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
