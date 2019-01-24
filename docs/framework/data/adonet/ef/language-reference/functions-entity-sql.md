---
title: Fonctions (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 52b3d776-5acc-4f69-b614-5a43ce56ef9f
ms.openlocfilehash: 88029f22cc22594d26a05ad66051378a75a6e753
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54715593"
---
# <a name="functions-entity-sql"></a>Fonctions (Entity SQL)
Entity SQL prend en charge les fonctions définies par l'utilisateur, les fonctions canoniques et les fonctions spécifiques au fournisseur. Les fonctions définies par l'utilisateur sont spécifiées dans le modèle conceptuel ou inline dans la requête. Pour plus d’informations, consultez [les fonctions définies par l’utilisateur](../../../../../../docs/framework/data/adonet/ef/language-reference/user-defined-functions-entity-sql.md).  
  
 Les fonctions canoniques sont prédéfinies dans Entity Framework et doivent être prises en charge par les fournisseurs de données. Les commandes Entity SQL échouent si un utilisateur appelle une fonction qui n'est pas prise en charge par un fournisseur. Par conséquent, les fonctions canoniques sont généralement recommandées par rapport aux fonctions spécifiques au magasin, qui se trouvent dans un espace de noms spécifique au fournisseur. Pour plus d’informations, consultez [fonctions canoniques](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md).  
  
 Le fournisseur managé Client Microsoft SQL fournit un jeu de fonctions spécifiques au fournisseur. Pour plus d’informations, consultez [fonctions SqlClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).  
  
## <a name="in-this-section"></a>Dans cette section  
 [Fonctions définies par l’utilisateur](../../../../../../docs/framework/data/adonet/ef/language-reference/user-defined-functions-entity-sql.md)  
  
 [Résolution de surcharge des fonctions](../../../../../../docs/framework/data/adonet/ef/language-reference/function-overload-resolution-entity-sql.md)  
  
 [Fonctions d’agrégation](../../../../../../docs/framework/data/adonet/ef/aggregate-functions-sqlclient-for-entity-framework.md)  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
