---
title: USING (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 20f58b8f-6070-4456-b7e8-5ff3d6269273
ms.openlocfilehash: 6a5b374bc253cb2deb7a9e1de942c32d8e8bbfcf
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59168023"
---
# <a name="using-entity-sql"></a>USING (Entity SQL)
Spécifie les espaces de noms utilisés dans une expression de requête.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
USING [ alias = ] namespace  
```  
  
## <a name="arguments"></a>Arguments  
 `alias`  
 Spécifie un alias plus court avec lequel qualifier un espace de noms.  
  
 `namespace`  
 Tout espace de noms valide.  
  
## <a name="example"></a>Exemple  
 La requête Entity SQL ci-dessous utilise l'opérateur USING pour spécifier les espaces de noms utilisés dans une expression de requête. Pour compiler et exécuter cette requête, procédez comme suit :  
  
1.  Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne les résultats PrimitiveType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md).  
  
2.  Transmettez à la méthode `ExecutePrimitiveTypeQuery` la requête suivante en tant qu'argument :  
  
```  
using SqlServer; RAND()  
```  
  
## <a name="see-also"></a>Voir aussi

- [Espaces de noms](../../../../../../docs/framework/data/adonet/ef/language-reference/namespaces-entity-sql.md)
- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
