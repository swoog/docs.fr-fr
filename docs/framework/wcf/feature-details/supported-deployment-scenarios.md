---
title: Scénarios de déploiement pris en charge
ms.date: 03/30/2017
ms.assetid: 3399f208-3504-4c70-a22e-a7c02a8b94a6
ms.openlocfilehash: d0afd12b1c17f9356146aa13c90f8db65ed9ec0a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="supported-deployment-scenarios"></a>Scénarios de déploiement pris en charge
Le sous-ensemble de fonctionnalités de Windows Communication Foundation (WCF) prises en charge pour une utilisation dans les applications de confiance partiel est conçu pour répondre aux exigences de certains, mais pas tous, scénarios pour l’utilisation de WCF. Sur le serveur, WCF répond aux exigences de l’échelle d’Internet partagé fournisseurs d’hébergement qui exécutent des applications tierces dans le [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)] Medium Trust jeu d’autorisations pour des raisons de sécurité. Sur le client, prise en charge de la confiance partielle WCF est conçu pour répondre aux exigences des technologies de déploiement telles que [déploiement ClickOnce](http://go.microsoft.com/fwlink/?LinkId=83712) ou [!INCLUDE[avalon2](../../../../includes/avalon2-md.md)]de technologie d’Application de navigateur XAML, permettant transparentes et sécurisées déploiement d’applications de bureau à partir de sites non fiables.  
  
## <a name="minimum-permission-requirements"></a>Autorisations minimales requises  
 WCF prend en charge un sous-ensemble de fonctionnalités dans les applications qui s’exécutent sous des jeux d’autorisations nommés standard suivants :  
  
-   Autorisations de confiance moyenne  
  
-   Autorisations de la zone Internet  
  
 Toute tentative d’utilisation de WCF dans les applications de confiance partielle avec des autorisations plus restrictives peut entraîner des exceptions de sécurité lors de l’exécution.  
  
 Pour plus d’informations sur les fonctionnalités prises en charge dans ces jeux d’autorisations, consultez [Partial Trust Feature Compatibility](../../../../docs/framework/wcf/feature-details/partial-trust-feature-compatibility.md).  
  
## <a name="partial-trust-on-the-server"></a>Confiance partielle sur le serveur  
 De nombreux fournisseurs commerciaux de services d'hébergement d'application Web [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] exigent que les applications qui s'exécutent sur leurs serveurs s'exécutent dans le jeu d'autorisations de confiance moyenne [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)] . WCF services peuvent s’exécuter dans ces environnements s’ils utilisent le <xref:System.ServiceModel.BasicHttpBinding>, le <xref:System.ServiceModel.WebHttpBinding>, ou <<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`> avec la sécurité au niveau du transport.  
  
 Les services WCF en cours d’exécution dans les environnements d’hébergement de confiance moyenne peuvent également fonctionner comme services de couche intermédiaire en envoyant des messages vers d’autres serveurs en réponse aux demandes du client. Les scénarios de couche intermédiaire sur le serveur sont pris en charge si l'environnement d'hébergement a accordé le <xref:System.Net.WebPermission> approprié à l'application pour effectuer des demandes sortantes vers le serveur souhaité.  
  
 En plus de la messagerie SOAP à l’aide d’une des liaisons SOAP prises en charge, WCF prend en charge la <xref:System.ServiceModel.WebHttpBinding> pour la création de services de style Web dans les applications de confiance partielle. Le [modèle de programmation WCF Web HTTP](../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md), [Syndication WCF](../../../../docs/framework/wcf/feature-details/wcf-syndication.md), et [intégration d’AJAX et prise en charge JSON](../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md) fonctionnalités de WCF sont toutes prises en charge en mode de confiance partielle.  
  
 Les services de workflow requièrent des autorisations de confiance totale et ne peuvent pas être utilisés dans les applications de confiance partielle.  
  
 Pour plus d’informations, consultez [Comment : utilisation de confiance moyenne dans ASP.NET 2.0](http://go.microsoft.com/fwlink/?LinkId=84603).  
  
## <a name="partial-trust-on-the-client"></a>Confiance partielle sur le client  
 Certaines précautions de sécurité doivent être prises lors du téléchargement et de l'exécution du code à partir de sites Internet non fiables. La technologie [ClickOnce Deployment](http://go.microsoft.com/fwlink/?LinkId=83712) (Déploiement ClickOnce) et la technologie d’application du navigateur XAML (XBAP) de [!INCLUDE[avalon2](../../../../includes/avalon2-md.md)]utilisent la confiance de niveau partiel pour accorder des autorisations limitées (zone Internet) au code non fiable.  
  
 WCF peut être utilisé pour communiquer avec des serveurs distants à partir des applications de confiance partiel déployées par une [déploiement ClickOnce](http://go.microsoft.com/fwlink/?LinkId=83712) ou XBAP. Le jeu d’autorisations de Zone Internet inclut <xref:System.Net.WebPermission> pour l’hôte d’origine, ce qui autorise ces applications à communiquer avec leur serveur d’origine en utilisant l’une des liaisons WCF pris en charge décrites dans [compatibilité des fonctionnalités de confiance partielle ](../../../../docs/framework/wcf/feature-details/partial-trust-feature-compatibility.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Sécurité d’accès du code](http://go.microsoft.com/fwlink/?LinkId=83717)  
 [Vue d’ensemble de Windows Presentation Foundation Applications hébergées par un navigateur](http://go.microsoft.com/fwlink/?LinkId=98397)  
 [Confiance partielle](../../../../docs/framework/wcf/feature-details/partial-trust.md)  
 [Confiance moyenne ASP.Net](http://go.microsoft.com/fwlink/?LinkId=69328)
