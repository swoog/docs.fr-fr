---
title: Hébergement dans les services IIS (Internet Information Services)
ms.date: 03/30/2017
helpviewer_keywords:
- hosting services [WCF], IIS
ms.assetid: ddae14e8-143c-442d-b660-2046809b2d43
ms.openlocfilehash: 588e069280afc369256fdbee0132f732348ffc37
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="hosting-in-internet-information-services"></a>Hébergement dans les services IIS (Internet Information Services)
Une des options pour l’hébergement des services Windows Communication Foundation (WCF) sont à l’intérieur d’une application Internet Information Services (IIS). Ce modèle d'hébergement est semblable au modèle utilisé par [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] et les services Web ASP.NET (ASMX).  
  
## <a name="versions-of-iis"></a>Versions d'IIS  
 WCF peut être hébergé sur les versions suivantes d’IIS sur les systèmes d’exploitation suivants :  
  
-   IIS 5.1 sur [!INCLUDE[wxpsp2](../../../../includes/wxpsp2-md.md)]. Cet environnement est utile pour la conception et développement d'applications hébergées par IIS et déployées ultérieurement sur un système d'exploitation de serveur tel que [!INCLUDE[ws2003](../../../../includes/ws2003-md.md)].  
  
-   [!INCLUDE[iis601](../../../../includes/iis601-md.md)] sur [!INCLUDE[ws2003](../../../../includes/ws2003-md.md)]. [!INCLUDE[iis601](../../../../includes/iis601-md.md)] fournit un modèle de processus avancé qui offre une évolutivité, une fiabilité et une isolation d'application améliorées. Cet environnement est adapté au déploiement de production des services WCF qui utilisent la communication HTTP exclusivement.  
  
-   IIS 7.0 sur [!INCLUDE[wv](../../../../includes/wv-md.md)] et [!INCLUDE[lserver](../../../../includes/lserver-md.md)]. ISS 7.0 fournit le même modèle de processus avancé que [!INCLUDE[iis601](../../../../includes/iis601-md.md)], mais il utilise le service d'activation de processus de Windows (WAS) pour autoriser l'activation et la communication réseau sur des protocoles autres que HTTP. Cet environnement est adapté au développement de services WCF qui communiquent sur tous les protocoles réseau pris en charge par WCF (y compris HTTP, net.tcp, net.pipe et net.msmq). Pour plus d’informations sur WAS, consultez [hébergement dans le Service d’Activation des processus Windows](../../../../docs/framework/wcf/feature-details/hosting-in-windows-process-activation-service.md).  
  
-   [Windows Server AppFabric](http://go.microsoft.com/fwlink/?LinkId=196496) fonctionne avec [!INCLUDE[iisver](../../../../includes/iisver-md.md)] et le Service de l’Activation des processus Windows (WAS) pour fournir une environnement de services aux services NET4 WCF et WF d’hébergement d’application riche. Ces avantages incluent la gestion du cycle de vie de processus, le recyclage de processus, l'hébergement partagé, la protection rapide contre les incidents, les processus parallèles, l'activation à la demande et le contrôle d'état. Pour plus d’informations, consultez [fonctionnalités d’hébergement AppFabric](http://go.microsoft.com/fwlink/?LinkId=196494) et [Concepts d’hébergement AppFabric](http://go.microsoft.com/fwlink/?LinkId=196495).  
  
## <a name="benefits-of-iis-hosting"></a>Avantages de l'hébergement IIS  
 Hébergement de services WCF dans IIS offre plusieurs avantages :  
  
-   Les services WCF hébergés dans IIS sont déployés et gérés comme tout autre type d’application IIS, y compris [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] ASMX et les applications.  
  
-   IIS assure l'activation de processus, la gestion de l'intégrité et le recyclage des fonctions afin d'accroître la fiabilité des applications hébergées.  
  
-   Comme [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], les services WCF hébergés dans [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] peuvent tirer parti de la [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] modèle d’hébergement partagé où plusieurs applications résident dans un processus de travail courants de densité de serveur améliorée et d’évolutivité.  
  
-   Les services WCF hébergés dans IIS utilisent le même modèle de compilation dynamique en tant que [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)], ce qui simplifie le développement et déploiement des services hébergés.  
  
 Lorsque vous décidez d’héberger des services WCF dans IIS, il est important de se rappeler que IIS 5.1 et [!INCLUDE[iis601](../../../../includes/iis601-md.md)] sont limités à la communication HTTP uniquement. Pour plus d’informations sur le choix d’un environnement d’hébergement, consultez [Services d’hébergement](../../../../docs/framework/wcf/hosting-services.md).  
  
## <a name="deploying-an-iis-hosted-wcf-service"></a>Déploiement d'un service WCF hébergé par IIS  
 Développement et déploiement d’un service WCF hébergé par IIS impliquent les tâches suivantes :  
  
-   Vérifiez que IIS, ASP.NET, WCF et le composant d’activation HTTP de WCF sont correctement installés et inscrits.  
  
-   Créer une application IIS ou réutiliser une application [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] existante.  
  
-   Créez un fichier .svc pour le service WCF.  
  
-   Déployer l'implémentation de service vers l'application IIS.  
  
-   Configurer le service WCF.  
  
 Pour en savoir plus sur chacune de ces tâches, consultez [déploiement d’un Service WCF de sujet](../../../../docs/framework/wcf/feature-details/deploying-an-internet-information-services-hosted-wcf-service.md).  
  
## <a name="wcf-services-and-aspnet"></a>Services WCF et ASP.NET  
 Les services WCF peuvent être hébergés soit côte à côte avec [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] ou dans [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] le Mode de compatibilité dans lequel les services peuvent tirer pleinement parti des fonctionnalités fournies par le [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] plate-forme d’application Web. Pour une description de ces fonctionnalités, consultez [Services WCF et ASP.NET](../../../../docs/framework/wcf/feature-details/wcf-services-and-aspnet.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Extension de l’hébergement à l’aide de ServiceHostFactory](../../../../docs/framework/wcf/extending/extending-hosting-using-servicehostfactory.md)  
 [Déploiement d’un service WCF hébergé dans Internet Information Services](../../../../docs/framework/wcf/feature-details/deploying-an-internet-information-services-hosted-wcf-service.md)  
 [Services WCF et ASP.NET](../../../../docs/framework/wcf/feature-details/wcf-services-and-aspnet.md)  
 [Bonnes pratiques pour l’hébergement dans Internet Information Services](../../../../docs/framework/wcf/feature-details/internet-information-services-hosting-best-practices.md)  
 [Configuration des services Internet Information Services 7.0 pour Windows Communication Foundation](../../../../docs/framework/wcf/feature-details/configuring-iis-for-wcf.md)  
 [Fonctionnalités d’hébergement de Windows Server App Fabric](http://go.microsoft.com/fwlink/?LinkId=201276)
