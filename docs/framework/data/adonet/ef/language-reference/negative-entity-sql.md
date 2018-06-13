---
title: '- (Négatif) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 208e54ef-4741-4ec5-89d6-6ff700863cb0
ms.openlocfilehash: 5d1726be6a4a59891646d05b344f59962d548c75
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32765150"
---
# <a name="--negative-entity-sql"></a>- (négatif) (Entity SQL)
Retourne la forme négative de la valeur d'une expression numérique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
- expression  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Toute expression valide de l'un des types de données numériques.  
  
## <a name="result-types"></a>Types de résultats  
 Type de données de l' `expression`.  
  
## <a name="remarks"></a>Notes  
 Si l' `expression` est un type non signé, le type du résultat sera le type signé le plus proche du type de l' `expression`. Par exemple, si l' `expression` est de type Byte, une valeur de type Int16 sera retournée.  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'opérateur arithmétique - pour retourner la forme négative de la valeur d'une expression numérique. Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1.  Suivez la procédure indiquée dans [Guide pratique pour exécuter une requête qui retourne les résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2.  Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#NEGATIVE](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#negative)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
