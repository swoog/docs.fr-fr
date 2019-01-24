---
title: '|| (OR) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 8e649648-eb9a-4380-9d74-36e62260628c
ms.openlocfilehash: 4d0bed2fb000e96e9fd0ceac6ea90e19b8fa7514
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54554853"
---
# <a name="-or-entity-sql"></a>|| (OR) (Entity SQL)
Combine deux expressions `Boolean` .  
  
## <a name="syntax"></a>Syntaxe  
  
```  
boolean_expression OR boolean_expression  
or   
boolean_expression || boolean_expression  
```  
  
## <a name="arguments"></a>Arguments  
 `boolean_expression`  
 Toute expression valide qui retourne une valeur `Boolean`.  
  
## <a name="return-value"></a>Valeur de retour  
 `true` si l'une des conditions a la valeur `true`; sinon, `false`.  
  
## <a name="remarks"></a>Notes  
 OR est un opérateur logique [!INCLUDE[esql](../../../../../../includes/esql-md.md)] . Il est utilisé pour combiner deux conditions. Lorsque vous utilisez plusieurs opérateurs logiques dans une instruction, les opérateurs OR sont évalués après les opérateurs AND. L'utilisation de parenthèses permet toutefois de modifier l'ordre de traitement.  
  
 Les doubles barres verticales (&#124;&#124;) ont les mêmes fonctionnalités que l’opérateur OR.  
  
 Le tableau ci-dessous indique les valeurs d'entrée et les types de retour possibles.  
  
||`TRUE`|`FALSE`|`NULL`|  
|-|------------|-------------|------------|  
|`TRUE`|true|TRUE|TRUE|  
|`FALSE`|TRUE|FALSE|NULL|  
|`NULL`|TRUE|NULL|NULL|  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'opérateur OR pour combiner deux expressions `Boolean` . Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1.  Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2.  Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#OR](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#or)]  
  
## <a name="see-also"></a>Voir aussi
- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
