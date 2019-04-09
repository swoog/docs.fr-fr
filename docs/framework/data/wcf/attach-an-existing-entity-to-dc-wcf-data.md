---
title: 'Procédure : Attacher une entité existante au DataServiceContext (WCF Data Services)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, changing data
ms.assetid: e3f2d71d-434c-4e98-91c3-95adae4702b6
ms.openlocfilehash: 6fa8e9d66fa89eb058aafd1e74164097b7f5c3a3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59157850"
---
# <a name="how-to-attach-an-existing-entity-to-the-dataservicecontext-wcf-data-services"></a>Procédure : Attacher une entité existante au DataServiceContext (WCF Data Services)
Lorsqu’une entité existe déjà dans un service de données, le [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] bibliothèque cliente vous permet de joindre un objet qui représente l’entité directement au <xref:System.Data.Services.Client.DataServiceContext> sans exécuter d’abord une requête. Pour plus d’informations, consultez [la mise à jour le Service de données](../../../../docs/framework/data/wcf/updating-the-data-service-wcf-data-services.md).  
  
 L'exemple dans cette rubrique utilise l'exemple de service de données Northwind et des classes de service de données clientes générées automatiquement. Ce service et les classes de données client sont créés lorsque vous complétez le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant montre comment créer un objet `Customer` existant qui contient des modifications à enregistrer dans le service de données. L'objet est joint au contexte et la méthode <xref:System.Data.Services.Client.DataServiceContext.UpdateObject%2A> est appelée pour marquer l'objet joint comme <xref:System.Data.Services.Client.EntityStates.Modified> avant d'appeler la méthode <xref:System.Data.Services.Client.DataServiceContext.SaveChanges%2A>.  
  
 [!code-csharp[Astoria Northwind Client#AttachObject](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria northwind client/cs/source.cs#attachobject)]
 [!code-vb[Astoria Northwind Client#AttachObject](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria northwind client/vb/source.vb#attachobject)]  
  
## <a name="see-also"></a>Voir aussi

- [Bibliothèque client services de données WCF](../../../../docs/framework/data/wcf/wcf-data-services-client-library.md)
