---
title: 'Comment : personnaliser les flux avec le fournisseur de réflexion (services de données WCF)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, customizing
- WCF Data Services, customizing feeds
ms.assetid: 00c23dcf-9bb8-459a-a012-6c4d9bcad7e9
ms.openlocfilehash: 984a4aac43689be0ec80e7f6c289e8d5229e9e1b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33358006"
---
# <a name="how-to-customize-feeds-with-the-reflection-provider-wcf-data-services"></a>Comment : personnaliser les flux avec le fournisseur de réflexion (services de données WCF)
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] vous permet de personnaliser la sérialisation Atom dans une réponse du service de données pour pouvoir mapper les propriétés d'une entité aux éléments inutilisés définis dans le protocole AtomPub. Cette rubrique indique comment définir des attributs de mappage pour les types d'entité dans un modèle de données défini à l'aide du fournisseur de réflexion. Pour plus d’informations, consultez [personnalisation de flux](../../../../docs/framework/data/wcf/feed-customization-wcf-data-services.md).  
  
 Le modèle de données pour cet exemple est défini dans la rubrique [Comment : créer un Service de données à l’aide du fournisseur de réflexion](../../../../docs/framework/data/wcf/create-a-data-service-using-rp-wcf-data-services.md)  
  
## <a name="example"></a>Exemple  
 Dans l'exemple suivant, les deux propriétés du type `Order` sont mappées aux éléments Atom existants. La propriété `Product` du type `Item` est mappée à un attribut de flux personnalisé dans un espace de noms séparé.  
  
 [!code-csharp[Astoria Custom Feeds#CustomIQueryableFeeds](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria custom feeds/cs/orderitems.svc.cs#customiqueryablefeeds)]
 [!code-vb[Astoria Custom Feeds#CustomIQueryableFeeds](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria custom feeds/vb/orderitems.svc.vb#customiqueryablefeeds)]  
  
## <a name="example"></a>Exemple  
 L'exemple précédent retourne le résultat suivant pour l'URI `http://myservice/OrderItems.svc/Orders(0)?$expand=Items`.  
  
 [!code-xml[Astoria Custom Feeds#IQueryableFeedResultInline](../../../../samples/snippets/xml/VS_Snippets_Misc/astoria custom feeds/xml/iqueryablefeedresultinline.xml#iqueryablefeedresultinline)]  
  
## <a name="see-also"></a>Voir aussi  
 [Fournisseur de réflexion](../../../../docs/framework/data/wcf/reflection-provider-wcf-data-services.md)
