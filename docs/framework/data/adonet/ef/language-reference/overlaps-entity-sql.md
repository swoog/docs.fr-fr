---
title: OVERLAPS (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 41743e89-79cb-4d7b-8a27-355b45024b61
ms.openlocfilehash: 74399c4c5701fcf039666ef3de19de2cf9a6b50e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59104199"
---
# <a name="overlaps-entity-sql"></a>OVERLAPS (Entity SQL)
Détermine si deux collections ont des éléments en commun.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
expression OVERLAPS expression  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Toute expression de requête valide qui retourne une collection à comparer avec la collection retournée par une autre expression de requête. Toutes les expressions doivent être du même type que le `expression`ou d'un type de base commun ou dérivé de celui-ci.  
  
## <a name="return-value"></a>Valeur de retour  
 `true` Si les deux collections ont des éléments en commun ; Sinon, `false`.  
  
## <a name="remarks"></a>Notes  
 OVERLAPS est fonctionnellement équivalent à ce qui suit :  
  
 `EXISTS ( expression INTERSECT expression )`  
  
 OVERLAPS est l'un des opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] . Tous les opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont évalués de gauche à droite. Pour plus d’informations de priorité pour le [!INCLUDE[esql](../../../../../../includes/esql-md.md)] opérateurs de jeu, consultez [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md).  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'opérateur OVERLAPS pour déterminer si deux collections ont une valeur commune. Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1.  Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2.  Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#OVERLAPS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#overlaps)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
