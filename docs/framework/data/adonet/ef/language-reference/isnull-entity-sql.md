---
title: ISNULL (Entity SQL)
ms.date: 03/30/2017
ms.assetid: dc7a0173-3664-4c90-a57b-5cbb0a8ed7ee
ms.openlocfilehash: 894d3ab91623aa4246bf7735fb1b7d04e066825a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59072634"
---
# <a name="isnull-entity-sql"></a>ISNULL (Entity SQL)
Détermine si une expression de requête a la valeur NULL.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
expression IS [ NOT ] NULL  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Toute expression de requête valide. Ne peut pas être une collection, posséder des membres de collection ou être un type d'enregistrement avec des propriétés de type collection.  
  
 NOT  
 Inverse le résultat EDM.Boolean de l'opérateur IS NULL.  
  
## <a name="return-value"></a>Valeur de retour  
 `true` Si `expression` retourne null ; sinon, `false`.  
  
## <a name="remarks"></a>Notes  
 Utilisez `IS NULL` pour déterminer si l'élément d'une jointure externe est NULL :  
  
```  
select c   
      from LOB.Customers as c left outer join LOB.Orders as o   
                              on c.ID = o.CustomerID    
      where o is not null and o.OrderQuantity = @x  
```  
  
 Utilisez `IS NULL` pour déterminer si un membre a une valeur réelle :  
  
```  
select c from LOB.Customer as c where c.DOB is not null  
```  
  
 Le tableau ci-dessous montre le comportement de l'opérateur `IS NULL` sur certains modèles. Toutes les exceptions sont levées côté client avant que le fournisseur soit appelé :  
  
|Motif|Comportement|  
|-------------|--------------|  
|null IS NULL|Retourne `true`.|  
|TREAT (null AS EntityType) IS NULL|Retourne `true`.|  
|TREAT (null AS ComplexType) IS NULL|Génère une erreur.|  
|TREAT (null AS RowType) IS NULL|Génère une erreur.|  
|EntityType IS NULL|Retourne `true` ou la valeur `false`.|  
|ComplexType IS NULL|Génère une erreur.|  
|RowType IS NULL|Génère une erreur.|  
  
## <a name="example"></a>Exemple  
 Ce qui suit [!INCLUDE[esql](../../../../../../includes/esql-md.md)] requête utilise l’opérateur IS NOT NULL pour déterminer si une expression de requête n’est pas null. Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1.  Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2.  Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#ISNULL](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#isnull)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
