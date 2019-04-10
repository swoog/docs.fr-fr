---
title: IN (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 51662950-ee01-4857-b7b9-311dd8515966
ms.openlocfilehash: f4fa8cbc07513321e59b93503b59af172c0a6f05
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59211320"
---
# <a name="in-entity-sql"></a>IN (Entity SQL)
Détermine si une valeur correspond à une valeur incluse dans une collection.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
value [ NOT ] IN expression  
```  
  
## <a name="arguments"></a>Arguments  
 `value`  
 Toute expression valide qui retourne la valeur dont rechercher une correspondance.  
  
 [ NOT ]  
 Spécifie que la valeur du résultat `Boolean` de IN est inversée.  
  
 `expression`  
 Toute expression valide qui retourne la collection dans laquelle rechercher une correspondance. Toutes les expressions doivent être du même type que le `value`ou d'un type de base commun ou dérivé de celui-ci.  
  
## <a name="return-value"></a>Valeur de retour  
 `true` Si la valeur est trouvée dans la collection ; null si la valeur est null ou la collection est null. Sinon, `false`. L'utilisation de NOT IN inverse les résultats de IN.  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'opérateur IN pour déterminer si une valeur correspond à une valeur contenue dans une collection. Cette requête est basée sur le modèle de vente AdventureWorks Sales Model. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1.  Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2.  Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :  
  
 [!code-csharp[DP EntityServices Concepts 2#IN](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#in)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
