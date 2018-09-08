---
title: "Procédure : activer l'accès au service de données (WCF Data Services)"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF Data Services, configuring
ms.assetid: 3d830bcd-32b4-4f26-9287-d58a071452c6
ms.openlocfilehash: eb9d7cd8e62a73f49fd2b0f2fc2572b01109553b
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44214834"
---
# <a name="how-to-enable-access-to-the-data-service-wcf-data-services"></a>Procédure : activer l'accès au service de données (WCF Data Services)
Dans [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)], vous devez accorder explicitement l'accès aux ressources exposées par un service de données. Cela signifie qu'après avoir créé un service de données, vous devez encore fournir explicitement l'accès à des ressources individuelles comme les jeux d'entités. Cette rubrique montre comment activer la lecture et l’accès en écriture à cinq de l’entité définit dans le service de données Northwind est créé lorsque vous complétez le [quickstart](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md). Puisque l'énumération <xref:System.Data.Services.EntitySetRights> est définie à l'aide de l'objet <xref:System.FlagsAttribute>, vous pouvez utiliser un opérateur OR logique pour spécifier plusieurs autorisations pour un jeu d'entités unique.  
  
> [!NOTE]
>  Tout client qui peut accéder à l'application ASP.NET peut également accéder aux ressources exposées par le service de données. Dans un service de données de production, pour empêcher l'accès non autorisé aux ressources, vous devez également sécuriser l'application elle-même. Pour plus d’informations, consultez [NIB : sécurité ASP.NET](https://msdn.microsoft.com/library/04b37532-18d9-40b4-8e5f-ee09a70b311d).  
  
### <a name="to-enable-access-to-the-data-service"></a>Pour activer l'accès au service de données  
  
-   Dans le code du service de données, remplacez le code d'espace réservé dans la fonction `InitializeService` par le code suivant :  
  
     [!code-csharp[Astoria Quickstart Service#AllReadConfig](../../../../samples/snippets/csharp/VS_Snippets_Misc/astoria quickstart service/cs/northwind.svc.cs#allreadconfig)]
     [!code-vb[Astoria Quickstart Service#AllReadConfig](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/astoria quickstart service/vb/northwind.svc.vb#allreadconfig)]  
  
     Cela permet aux clients de disposer d'un accès en lecture et en écriture aux jeux d'entités `Orders` et `Order_Details` et d'un accès en lecture seule aux jeux d'entités `Customers`.  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour développer un service de données WCF qui fonctionne sur IIS](../../../../docs/framework/data/wcf/how-to-develop-a-wcf-data-service-running-on-iis.md)  
 [Configuration du service de données](../../../../docs/framework/data/wcf/configuring-the-data-service-wcf-data-services.md)
