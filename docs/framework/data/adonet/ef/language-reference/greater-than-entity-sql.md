---
title: '> (Supérieur à) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 4cea865c-677c-4b06-99a1-010f2ae2394a
ms.openlocfilehash: e1d13fa863eb79982d239f4e2dc298f7fcd1346f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61879487"
---
# <a name="-greater-than-entity-sql"></a>> (Supérieur à) (Entity SQL)
Compare deux expressions pour déterminer si la valeur de l'expression de gauche est supérieure à celle de l'expression de droite.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
expression > expression  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Toute expression valide. Les deux expressions doivent posséder des types de données implicitement convertibles.  
  
## <a name="result-types"></a>Types de résultats  
 `true` si la valeur de l'expression de gauche est supérieure à celle de l'expression de droite ; sinon, `false`.  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'opérateur de comparaison > pour comparer deux expressions afin de déterminer si la valeur de l'expression de gauche est supérieure à celle de l'expression de droite. Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1. Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2. Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#GREATER](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#greater)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
