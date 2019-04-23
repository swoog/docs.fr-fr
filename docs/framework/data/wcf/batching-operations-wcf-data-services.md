---
title: Opérations de traitement par lots (services de données WCF)
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, client library
ms.assetid: 962a49d1-cc11-4b96-bc7d-071dd6607d6c
ms.openlocfilehash: a9f74f025af6dfc5737ea9f4971f68c5ad913e8b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59133599"
---
# <a name="batching-operations-wcf-data-services"></a>Opérations de traitement par lots (services de données WCF)
Le [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] prend en charge traitement par lots des demandes à un [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)]-en fonction de service. Pour plus d’informations, consultez [OData : Traitement par lots](https://go.microsoft.com/fwlink/?LinkId=186075). Dans [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)], chaque opération qui utilise le <xref:System.Data.Services.Client.DataServiceContext>, telles que l’exécution d’une requête ou de l’enregistrement des modifications, entraîne une demande séparée envoyées au service de données. Pour maintenir une étendue logique pour les jeux d'opérations, vous pouvez définir explicitement des lots opérationnels. Cela garantit que toutes les opérations dans le lot sont envoyées au service de données dans une requête HTTP unique permet au serveur traiter les opérations de manière atomique et réduit le nombre d’allers-retours au service de données.  
  
## <a name="batching-query-operations"></a>Opérations de traitement par lot des requêtes  
 Pour exécuter plusieurs requêtes dans un lot unique, vous devez créer chaque requête dans le lot comme une instance distincte de la classe <xref:System.Data.Services.Client.DataServiceRequest%601>. Lorsque vous créez une requête d'interrogation de cette manière, la requête elle-même est définie comme un URI, et elle suit les règles pour l'adressage de ressources. Pour plus d’informations, consultez [accès aux ressources de Service de données](../../../../docs/framework/data/wcf/accessing-data-service-resources-wcf-data-services.md). Les requêtes d'interrogation par lot sont envoyées au service de données lorsque la méthode <xref:System.Data.Services.Client.DataServiceContext.ExecuteBatch%2A> est appelée qui contient les objets de requête d'interrogation. Cette méthode retourne un objet <xref:System.Data.Services.Client.DataServiceResponse> qui est une collection d’objets <xref:System.Data.Services.Client.QueryOperationResponse%601> qui représentent des réponses aux requêtes individuelles dans le lot, chacune contenant une collection d’objets retournés par la requête ou des informations d’erreur. Lorsqu'une opération de requête unique dans le lot échoue, les informations d'erreur sont retournées dans l'objet <xref:System.Data.Services.Client.QueryOperationResponse%601> pour l'opération qui a échoué et les opérations restantes sont exécutées. Pour plus d'informations, voir [Procédure : Exécuter des requêtes dans un lot](../../../../docs/framework/data/wcf/how-to-execute-queries-in-a-batch-wcf-data-services.md).  
  
 Les requêtes par lot peuvent également être exécutées de façon asynchrone. Pour plus d’informations, consultez [opérations asynchrones](../../../../docs/framework/data/wcf/asynchronous-operations-wcf-data-services.md).  
  
## <a name="batching-the-savechanges-operation"></a>Traitement par lot de l'opération SaveChanges  
 Lorsque vous appelez le <xref:System.Data.Services.Client.DataServiceContext.SaveChanges%2A> (méthode), toutes les modifications que le contexte de pistes sont traduites en opérations basées sur REST qui sont envoyées en tant que demande le [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] service. Par défaut, ces modifications ne sont pas envoyées dans un message de demande unique. Pour exiger que toutes les modifications soient envoyées dans une demande unique, vous devez appeler la <xref:System.Data.Services.Client.DataServiceContext.SaveChanges%28System.Data.Services.Client.SaveChangesOptions%29> (méthode) et inclure une valeur de <xref:System.Data.Services.Client.SaveChangesOptions.Batch> dans le <xref:System.Data.Services.Client.SaveChangesOptions> énumération que vous fournissez à la méthode.  
  
 Vous pouvez également enregistrer de façon asynchrone les modifications par lot. Pour plus d’informations, consultez [opérations asynchrones](../../../../docs/framework/data/wcf/asynchronous-operations-wcf-data-services.md).  
  
## <a name="see-also"></a>Voir aussi

- [Bibliothèque cliente WCF Data Services](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
