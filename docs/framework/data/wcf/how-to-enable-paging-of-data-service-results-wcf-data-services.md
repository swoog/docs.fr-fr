---
title: 'Procédure : Activer la pagination des résultats du Service de données (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- paging output [WCF Data Services]
ms.assetid: 9a316cbd-9612-4482-a541-a10bc78b2635
ms.openlocfilehash: 77dbeba89b352fa470ab0523a830db9175a1a21a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59122900"
---
# <a name="how-to-enable-paging-of-data-service-results-wcf-data-services"></a>Procédure : Activer la pagination des résultats du Service de données (WCF Data Services)
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] vous permet de limiter le nombre d’entités retournées par une requête de service de données. Les limites de page sont définies dans la méthode appelée lorsque le service est initialisé et peuvent être définies séparément pour chaque jeu d'entités.  
  
 Lorsque la pagination est activée, la dernière entrée dans le flux contient un lien vers la page suivante de données. Pour plus d’informations, consultez [configuration du Service de données](../../../../docs/framework/data/wcf/configuring-the-data-service-wcf-data-services.md).  
  
 Cette rubrique indique comment modifier un service de données pour permettre la pagination de `Customers` retournés et de jeux d'entités `Orders`. L'exemple de cette rubrique utilise l'exemple du service de données Northwind. Ce service est créé lorsque vous effectuez la [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).  
  
### <a name="how-to-enable-paging-of-returned-customers-and-orders-entity-sets"></a>Comment permettre la pagination de clients retournés et de jeux d'entités de commandes  
  
-   Dans le code du service de données, remplacez le code d'espace réservé dans la fonction `InitializeService` par le code suivant :  
  
     [!code-csharp[Astoria Northwind Service#DataServiceConfigPaging](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind service/cs/northwind.svc.cs#dataserviceconfigpaging)]
     [!code-vb[Astoria Northwind Service#DataServiceConfigPaging](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind service/vb/northwind.svc.vb#dataserviceconfigpaging)]  
  
## <a name="see-also"></a>Voir aussi

- [Chargement de contenu différé](../../../../docs/framework/data/wcf/loading-deferred-content-wcf-data-services.md)
- [Procédure : Charger des résultats paginés](../../../../docs/framework/data/wcf/how-to-load-paged-results-wcf-data-services.md)
