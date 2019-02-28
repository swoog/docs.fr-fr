---
title: Select, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QuerySelect
helpviewer_keywords:
- Select statement [Visual Basic]
- Select clause [Visual Basic]
- queries [Visual Basic], Select
ms.assetid: 27a3f61c-5960-4692-9b91-4d0c4b6178fe
ms.openlocfilehash: 591fa664c56383cf8a7b3492e524a9738e065f8a
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56979604"
---
# <a name="select-clause-visual-basic"></a>Select, clause (Visual Basic)
Définit le résultat d’une requête.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Select [ var1 = ] fieldName1 [, [ var2 = ] fieldName2 [...] ]  
```  
  
## <a name="parts"></a>Composants  
 `var1`  
 Facultatif. Un alias qui peut être utilisé pour référencer les résultats de l’expression de colonne.  
  
 `fieldName1`  
 Obligatoire. Le nom du champ à retourner dans le résultat de requête.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser le `Select` clause pour définir les résultats à retourner à partir d’une requête. Cela vous permet de définir les membres d’un nouveau type anonyme qui est créé par une requête ou de cibler les membres d’un type nommé qui est retourné par une requête. Le `Select` clause n’est pas obligatoire pour une requête. Si aucun `Select` clause est spécifiée, la requête retournera un type basé sur tous les membres des variables de plage identifiées pour l’étendue actuelle. Pour plus d’informations, consultez [Types anonymes](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md). Lorsqu’une requête crée un type nommé, elle retournera un résultat de type <xref:System.Collections.Generic.IEnumerable%601> où `T` est le type créé.  
  
 Le `Select` clause peut faire référence à toutes les variables dans la portée actuelle. Cela inclut des variables de portée identifiées dans le `From` clause (ou `From` clauses). Il inclut également toutes les nouvelles variables créées avec un alias par le `Aggregate`, `Let`, `Group By`, ou `Group Join` clauses ou variables à partir d’une précédente `Select` clause dans l’expression de requête. Le `Select` clause peut également inclure des valeurs statiques. Par exemple, l’exemple de code suivant montre une expression de requête dans lequel le `Select` clause définit le résultat de requête comme un nouveau type anonyme avec quatre membres : `ProductName`, `Price`, `Discount`, et `DiscountedPrice`. Le `ProductName` et `Price` les valeurs de membre sont extraites de la variable de portée du produit qui est définie dans le `From` clause. Le `DiscountedPrice` valeur de membre est calculée dans le `Let` clause. Le `Discount` membre est une valeur statique.  
  
 [!code-vb[VbSimpleQuerySamples#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#27)]  
  
 Le `Select` clause introduit un nouvel ensemble de variables de portée pour les clauses de requête suivantes, et les variables de portée précédente ne sont plus dans la portée. La dernière `Select` clause dans une expression de requête détermine la valeur de retour de la requête. Par exemple, la requête suivante retourne la société nom et l’ordre des ID pour chaque commande client dont le total est supérieure à 500. La première `Select` clause identifie les variables de plage pour le `Where` clause et la seconde `Select` clause. La seconde `Select` clause identifie les valeurs retournées par la requête sous un nouveau type anonyme.  
  
 [!code-vb[VbSimpleQuerySamples#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#28)]  
  
 Si le `Select` clause identifie un élément unique à retourner, l’expression de requête retourne une collection du type de cet élément unique. Si le `Select` clause identifie plusieurs éléments à retourner, l’expression de requête retourne une collection d’un nouveau type anonyme, en fonction des éléments sélectionnés. Par exemple, les deux requêtes suivantes retournent des collections de deux types différents selon le `Select` clause. La première requête retourne une collection de noms de société sous forme de chaînes. La deuxième requête retourne une collection de `Customer` objets remplie avec les noms de société et les informations d’adresse.  
  
 [!code-vb[VbSimpleQuerySamples#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#29)]  
  
## <a name="example"></a>Exemple  
 La requête suivante expression utilise un `From` clause pour déclarer une variable de portée `cust` pour le `customers` collection. Le `Select` clause sélectionne le nom du client et la valeur d’ID et remplit la `CompanyName` et `CustomerID` colonnes de la nouvelle variable de plage. Le `For Each` instruction effectue une itération sur chaque objet retourné et affiche le `CompanyName` et `CustomerID` colonnes pour chaque enregistrement.  
  
 [!code-vb[VbSimpleQuerySamples#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#30)]  
  
## <a name="see-also"></a>Voir aussi
- [Introduction à LINQ en Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Requêtes](../../../visual-basic/language-reference/queries/index.md)
- [From (clause)](../../../visual-basic/language-reference/queries/from-clause.md)
- [Where (clause)](../../../visual-basic/language-reference/queries/where-clause.md)
- [Order By (clause)](../../../visual-basic/language-reference/queries/order-by-clause.md)
- [Types anonymes](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
