---
title: Exposition de vos données comme service (services de données WCF)
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, configuring
- getting started, WCF Data Services
- WCF Data Services, getting started
ms.assetid: df0bbcee-f66f-4a88-abb4-4e73c8b9c908
ms.openlocfilehash: ba316aeda0a0a7e80af8e37a6a62e88652b9635b
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43463050"
---
# <a name="expose-your-data-as-a-service-wcf-data-services"></a>Exposer vos données en tant que Service (WCF Data Services)

WCF Data Services s’intègre à Visual Studio pour vous permettre de définir plus facilement des services permettant d’exposer vos données en tant que [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] flux. Création d’un service de données qui expose un flux OData implique les étapes fondamentales suivantes :

1.  **Définir le modèle de données.** WCF Data Services prend en charge en mode natif les modèles de données qui sont basées sur le [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md). Pour plus d’informations, consultez [Comment : créer un Service de données en utilisant une Source de données ADO.NET Entity Framework](../../../../docs/framework/data/wcf/create-a-data-service-using-an-adonet-ef-data-wcf.md).

     WCF Data Services prend également en charge les modèles de données qui sont basées sur des objets common language runtime (CLR) qui retournent une instance de la <xref:System.Linq.IQueryable%601> interface. Vous pouvez ainsi déployer des services de données basés sur les listes, les tableaux et les collections du .NET Framework. Pour permettre les opérations de création, lecture, mise à jour et suppression sur ces structures de données, vous devez également implémenter l'interface <xref:System.Data.Services.IUpdatable>. Pour plus d’informations, consultez [Comment : créer un Service de données à l’aide du fournisseur de réflexion](../../../../docs/framework/data/wcf/create-a-data-service-using-rp-wcf-data-services.md).

     Pour des scénarios plus avancés, WCF Data Services inclut un ensemble de fournisseurs qui vous permettent de définir un modèle de données basé sur les types de données de la liaison tardive. Pour plus d’informations, consultez [fournisseurs de services de données personnalisés](../../../../docs/framework/data/wcf/custom-data-service-providers-wcf-data-services.md).

2.  **Créez le service de données.** Le service de données le plus basique expose une classe qui hérite de la classe <xref:System.Data.Services.DataService%601> , avec un type `T` qui est le nom qualifié par l'espace de noms du conteneur d'entités. Pour plus d'informations, consultez [Defining WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md).

3.  **Configurer le service de données.** Par défaut, WCF Data Services désactive l’accès aux ressources qui sont exposées par un conteneur d’entités. Le <xref:System.Data.Services.DataServiceConfiguration> interface vous permet de configurer l’accès aux ressources et opérations de service, spécifiez la version prise en charge d’OData et définir d’autres comportements de service à l’échelle, telles que le traitement par lot des comportements ou le nombre maximal d’entités qui peuvent être retournées dans une seule réponse. Pour plus d’informations, consultez [configuration du Service de données](../../../../docs/framework/data/wcf/configuring-the-data-service-wcf-data-services.md).

Pour obtenir un exemple montrant comment créer un service de données simple qui repose sur la base de données Northwind, consultez [Quickstart](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).

## <a name="see-also"></a>Voir aussi

- [Prise en main](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md)
- [Vue d’ensemble](../../../../docs/framework/data/wcf/wcf-data-services-overview.md)