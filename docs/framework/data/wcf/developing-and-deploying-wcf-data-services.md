---
title: Développer et déployer WCF Data Services
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, developing
- WCF Data Services, deploying
- deploying [WCF Data Services
- developing applications [WCF Data Services]
ms.assetid: 6557c0e3-5aea-4f6e-bc14-77ad317a168b
ms.openlocfilehash: 8b709de728726b7695b987c48574d2a70a1bc27e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765672"
---
# <a name="develop-and-deploy-wcf-data-services"></a>Développer et déployer des Services de données WCF

Cette rubrique fournit des informations sur le développement et déploiement de WCF Data Services. Pour des informations générales sur WCF Data Services, consultez [mise en route](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md) et [vue d’ensemble](../../../../docs/framework/data/wcf/wcf-data-services-overview.md).

## <a name="develop-wcf-data-services"></a>Développer des Services de données WCF

Lorsque vous utilisez WCF Data Services pour créer un service de données qui prend en charge la [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)], vous devez effectuer les tâches suivantes au cours du développement :

1. **Définir le modèle de données**

     WCF Data Services prend en charge une variété de fournisseurs de services de données qui vous permettent de définir un modèle de données basé sur les données à partir de diverses sources de données, à partir de bases de données relationnelles aux types de données de la liaison tardive. Pour plus d’informations, consultez [fournisseurs de Services de données](../../../../docs/framework/data/wcf/data-services-providers-wcf-data-services.md).

2. **Créer le service de données**

     Le service de données le plus basique expose une classe qui hérite de la classe <xref:System.Data.Services.DataService%601> , avec un type `T` qui est le nom qualifié par l'espace de noms du conteneur d'entités. Pour plus d'informations, consultez [Defining WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md).

3. **Configurer le service de données**

     Par défaut, WCF Data Services désactive l’accès aux ressources qui sont exposées par un conteneur d’entités. Le <xref:System.Data.Services.DataServiceConfiguration> interface vous permet de configurer l’accès aux ressources et opérations de service, spécifiez la version prise en charge d’OData et définir d’autres comportements de service à l’échelle, telles que le traitement par lot des comportements ou le nombre maximal d’entités qui peuvent être retournées dans un flux de réponse unique. Pour plus d’informations, consultez [configuration du Service de données](../../../../docs/framework/data/wcf/configuring-the-data-service-wcf-data-services.md).

Cette rubrique traite principalement du développement et déploiement de services de données à l’aide de Visual Studio. Pour plus d’informations sur la flexibilité fournie par WCF Data Services pour exposer vos données en tant que flux OData, consultez [Defining WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md).

### <a name="choose-a-development-web-server"></a>Choisissez un serveur Web de développement

Lorsque vous développez un Service de données WCF comme une [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] application ou [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] site Web à l’aide de Visual Studio 2015, vous avez le choix entre plusieurs serveurs Web sur lequel exécuter le service de données pendant le développement. Les serveurs Web suivants s’intègrent avec Visual Studio pour le rendre plus facile à tester et déboguer vos services de données sur l’ordinateur local.

1. **Serveur IIS local**

     Lorsque vous créez un service de données qui est une application [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] ou un site Web [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] exécuté sur Internet Information Services (IIS), nous vous recommandons de développer et tester votre service de données à l'aide d'IIS sur l'ordinateur local. L'exécution du service de données sur IIS facilite le suivi des demandes HTTP pendant le débogage. Elle permet également de prédéfinir les droits requis par IIS pour accéder aux fichiers, aux bases de données et aux autres ressources requises par le service de données. Pour exécuter votre service de données sur IIS, vous devez vous assurer que IIS et Windows Communication Foundation (WCF) sont installés et configurés correctement et accorder l’accès aux comptes d’IIS dans le système de fichiers et les bases de données. Pour plus d'informations, voir [Procédure : Développer un Service de données WCF s’exécutant sur IIS](../../../../docs/framework/data/wcf/how-to-develop-a-wcf-data-service-running-on-iis.md).

    > [!NOTE]
    > Vous devez exécuter Visual Studio avec des droits d’administrateur pour activer l’environnement de développement configurer le serveur IIS local.

2. **Serveur de développement Visual Studio**

     Visual Studio inclut un serveur Web intégré, le serveur de développement Visual Studio, qui est le serveur Web par défaut [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] projets. Ce serveur Web est conçu pour exécuter les projets [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] sur l'ordinateur local pendant le développement. Le [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md) montre comment créer un service de données qui s’exécute dans le serveur de développement Visual Studio.

     Vous devez connaître les limitations suivantes lorsque vous utilisez le serveur de développement Visual Studio pour développer le service de données :

    - Ce serveur est uniquement accessible sur l'ordinateur local.

    - Ce serveur écoute sur `localhost` et sur un port spécifique, non sur le port 80, qui est le port par défaut des messages HTTP. Pour plus d'informations, voir [Serveurs web dans Visual Studio pour les projets web ASP.NET](https://docs.microsoft.com/previous-versions/aspnet/58wxa9w5(v=vs.120)).

    - Ce serveur exécute le service de données dans le contexte de votre compte utilisateur actuel. Par exemple, si vous exécutez en tant qu’administrateur au niveau utilisateur, un service de données en cours d’exécution dans le serveur de développement Visual Studio ont des privilèges d’administrateur. Par conséquent, le service de données pourra accéder à des ressources pour lesquelles il ne possède pas de droits d'accès si déployé sur un serveur IIS.

    - Ce serveur n'inclut pas les fonctionnalités supplémentaires d'IIS, telles que l'authentification.

    - Ce serveur ne peut pas gérer les flux HTTP mémorisé en bloc, qui sont envoyés d’être par défaut par le client WCF Data Services lorsqu’ils accèdent à des données binaires volumineuses à partir du service de données. Pour plus d’informations, consultez [fournisseur de diffusion en continu](../../../../docs/framework/data/wcf/streaming-provider-wcf-data-services.md).

    - Ce serveur a des problèmes avec la période de traitement (`.`) de caractères dans une URL, même si ce caractère est pris en charge par WCF Data Services dans les valeurs de clé.

    > [!TIP]
    > Bien que vous pouvez utiliser le serveur de développement Visual Studio pour tester vos services de données pendant le développement, vous devez les tester à nouveau après le déploiement sur un serveur Web qui exécute IIS.

3. **Environnement de développement Microsoft Azure**

     Windows Azure Tools pour Visual Studio inclut un ensemble intégré d’outils pour développer des services Windows Azure dans Visual Studio. Avec ces outils, vous pouvez développer un service de données pouvant être déployé sur Microsoft Azure, et vous pouvez le tester sur l'ordinateur local avant son déploiement. Utilisez ces outils lorsque vous utilisez Visual Studio pour développer un service de données qui s’exécute sur la plateforme Windows Azure. Vous pouvez télécharger Windows Azure Tools pour Visual Studio à partir de la [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkID=201848). Pour plus d’informations sur le développement d’un service de données qui s’exécute sur Windows Azure, consultez le billet [déploiement d’un OData Service dans Windows Azure](https://go.microsoft.com/fwlink/?LinkId=201847).

### <a name="development-tips"></a>Conseils de développement

Vous devez tenir compte de ce qui suit lorsque vous développez un service de données :

- Définissez les conditions de sécurité de votre service de données si vous planifiez d'utiliser des utilisateurs authentifiés ou un accès restreint pour des utilisateurs spécifiques. Pour plus d'informations, consultez [Securing WCF Data Services](../../../../docs/framework/data/wcf/securing-wcf-data-services.md).

- Un programme d'inspection HTTP peut être très utile pour le débogage d'un service de données, car il vous permet d'inspecter le contenu des messages de demande et de réponse. N'importe quel analyseur de paquets réseau en mesure d'afficher des paquets bruts peut être utilisé pour inspecter des demandes et des réponses HTTP à partir du service de données.

- Lorsque vous déboguez un service de données, vous souhaiterez obtenir plus d’informations sur une erreur du service de données que pendant le fonctionnement normal. Pour obtenir davantage d'informations sur l'erreur à partir du service de données, affectez à la propriété <xref:System.Data.Services.DataServiceConfiguration.UseVerboseErrors%2A> dans <xref:System.Data.Services.DataServiceConfiguration> la valeur `true` et affectez à la propriété <xref:System.ServiceModel.Description.ServiceDebugBehavior.IncludeExceptionDetailInFaults%2A> de l'attribut <xref:System.ServiceModel.Description.ServiceDebugBehavior> sur la classe de service de données la valeur `true`. Pour plus d’informations, consultez le billet [débogage de WCF Data Services](https://go.microsoft.com/fwlink/?LinkId=201868). Vous pouvez également activer le traçage dans WCF pour afficher les exceptions levées dans la couche de messagerie HTTP. Pour plus d'informations, consultez [Configuring Tracing](../../../../docs/framework/wcf/diagnostics/tracing/configuring-tracing.md).

- Un service de données est généralement développé comme un [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] projet d’application, mais vous pouvez également créer votre service de données comme un [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] projet de site Web dans Visual Studio. Pour plus d’informations sur les différences entre les deux types de projets, consultez [projets d’Application Web et projets de Site Web dans Visual Studio](https://docs.microsoft.com/previous-versions/aspnet/dd547590(v=vs.110)).

- Lorsque vous créez un service de données à l’aide de la **ajouter un nouvel élément** boîte de dialogue dans Visual Studio, le service de données est hébergé par [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] dans IIS. Tandis que [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] et IIS sont l'hôte par défaut d'un service de données, d'autres options d'hébergement sont prises en charge. Pour plus d’informations, consultez [qui héberge le Service de données](../../../../docs/framework/data/wcf/hosting-the-data-service-wcf-data-services.md).

## <a name="deploy-wcf-data-services"></a>Déployer des Services de données WCF

WCF Data Service permet de choisir le processus qui héberge le service de données. Vous pouvez utiliser Visual Studio pour déployer un service de données sur les plateformes suivantes :

- **Serveur Web hébergé par IIS**

    Lorsqu'un service de données est développé en tant que projet [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] , il peut être déployé sur un serveur Web IIS à l'aide des processus de déploiement standard [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] .  Visual Studio fournit les technologies de déploiement suivantes pour [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], selon le type de [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] projet qui héberge le service de données que vous déployez.

  - **Technologies de déploiement des applications Web ASP.NET**

    - [Guide pratique pour Créer un Package de déploiement Web dans Visual Studio](https://docs.microsoft.com/previous-versions/aspnet/dd465323(v=vs.110))

    - [Guide pratique pour Déployer un site Web publier le projet à l’aide d’un seul clic dans Visual Studio](https://docs.microsoft.com/previous-versions/aspnet/dd465337(v=vs.110))

  - **Technologies de déploiement des sites Web ASP.NET**

    - [Guide pratique pour Copier des fichiers de Site Web avec l’outil Copier le Site Web](https://docs.microsoft.com/previous-versions/aspnet/c95809c0(v=vs.100))

    - [Guide pratique pour Publier des Sites Web](https://docs.microsoft.com/previous-versions/aspnet/20yh9f1b(v=vs.100))

    - [Procédure pas à pas : Déploiement d’une Application Web ASP.NET à l’aide de XCOPY](https://docs.microsoft.com/previous-versions/aspnet/f735abw9(v=vs.100))

     Pour plus d’informations sur les options de déploiement pour un [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] application, consultez [vue d’ensemble du déploiement Web pour Visual Studio et ASP.NET](https://docs.microsoft.com/previous-versions/aspnet/dd394698(v=vs.110)).

    > [!TIP]
    > Avant de tenter de déployer le service de données sur IIS, testez le déploiement sur un serveur Web qui exécute IIS. Pour plus d'informations, voir [Procédure : Développer un Service de données WCF s’exécutant sur IIS](../../../../docs/framework/data/wcf/how-to-develop-a-wcf-data-service-running-on-iis.md).

- **Windows Azure**

     Vous pouvez déployer un service de données vers Windows Azure à l’aide de Windows Azure Tools pour Visual Studio. Vous pouvez télécharger Windows Azure Tools pour Visual Studio à partir de la [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkID=201848). Pour plus d’informations sur le déploiement d’un service de données vers Windows Azure, consultez le billet [déploiement d’un OData Service dans Windows Azure](https://go.microsoft.com/fwlink/?LinkId=201847).

### <a name="deployment-considerations"></a>Points à prendre en considération pour le déploiement

Vous devez tenir compte de ce qui suit lorsque vous déployez un service de données :

- Lorsque vous déployez un service de données qui utilise le fournisseur [!INCLUDE[adonet_ef](../../../../includes/adonet-ef-md.md)] pour accéder à une base de données SQL Server, vous devrez peut-être propager des structures de données, des données, ou les deux à votre déploiement de service de données. Visual Studio peut créer automatiquement des scripts (fichiers .sql) pour ce faire, dans la base de données de destination, et ces scripts peuvent être inclus dans le package de déploiement Web d’un [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] application. Pour plus d'informations, voir [Procédure : Déployer une base de données avec un projet d’Application Web](https://docs.microsoft.com/previous-versions/dd465343(v=vs.100)). Pour un [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] site Web, vous pouvez faire à l’aide de la **Assistant Publication de base de données** dans Visual Studio. Pour plus d’informations, consultez [publication d’une base de données SQL](https://docs.microsoft.com/previous-versions/aspnet/bb907585(v=vs.100)).

- Étant donné que WCF Data Services inclut une implémentation WCF de base, vous pouvez utiliser Windows Server AppFabric pour surveiller un service de données déployé sur IIS s’exécutant sur Windows Server. Pour plus d’informations sur l’utilisation de Windows Server AppFabric pour surveiller un service de données, consultez le billet [suivi de WCF Data Services avec Windows Server AppFabric](https://go.microsoft.com/fwlink/?LinkID=202005).

## <a name="see-also"></a>Voir aussi

- [Hébergement du service de données](../../../../docs/framework/data/wcf/hosting-the-data-service-wcf-data-services.md)
- [Sécurisation de WCF Data Services](../../../../docs/framework/data/wcf/securing-wcf-data-services.md)
- [Définition de WCF Data Services](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)
