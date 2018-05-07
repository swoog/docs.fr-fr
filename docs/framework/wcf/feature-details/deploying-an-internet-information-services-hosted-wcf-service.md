---
title: Déploiement d'un service WCF hébergé dans Internet Information Services
ms.date: 03/30/2017
ms.assetid: 04ebd329-3fbd-44c3-b3ab-1de3517e27d7
ms.openlocfilehash: 59f18d8487deb52f5ecb5b5c814ec9bdbc74e2cc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="deploying-an-internet-information-services-hosted-wcf-service"></a>Déploiement d'un service WCF hébergé dans Internet Information Services
Développer et déployer un service Windows Communication Foundation (WCF) qui est hébergé dans Internet Information Services (IIS) comprend les tâches suivantes :  
  
-   Vérifiez que IIS, ASP.NET, WCF et le composant d’activation WCF sont correctement installés et inscrits.  
  
-   Créer une application IIS ou réutiliser une application [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] existante.  
  
-   Créez un fichier .svc pour le service WCF.  
  
-   Déployer l'implémentation de service vers l'application IIS.  
  
-   Configurer le service WCF.  
  
 Pour une description détaillée de la création d’un service WCF hébergé par IIS, consultez [Comment : héberger un Service WCF dans IIS](../../../../docs/framework/wcf/feature-details/how-to-host-a-wcf-service-in-iis.md).  
  
## <a name="ensure-that-iis-aspnet-and-wcf-are-correctly-installed-and-registered"></a>Vérifier que les services IIS, ASP.NET et WCF sont installés et enregistrés correctement  
 WCF, IIS et ASP.NET doivent être installé pour les services WCF hébergé par IIS fonctionner correctement. Les procédures d’installation de WCF (dans le cadre de le [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)]), ASP.NET et IIS varient selon la version du système d’exploitation utilisée. Pour plus d’informations sur l’installation de WCF et [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)], consultez [le programme d’installation de Microsoft .NET Framework 4 Web](http://go.microsoft.com/fwlink/?LinkId=201185). Les instructions pour installer les services IIS se trouvent à la page [Installing IIS (Installation d’IIS)](http://go.microsoft.com/fwlink/?LinkId=201188).  
  
 Le processus d’installation pour le [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)] enregistre automatiquement WCF avec IIS, si IIS est déjà présent sur l’ordinateur. Si IIS est installé après le [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)], une étape supplémentaire est requise pour inscrire WCF dans IIS et [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]. Pour ce faire, procédez comme suit selon votre système d'exploitation :  
  
-   [!INCLUDE[wxpsp2](../../../../includes/wxpsp2-md.md)], Windows 7, et [!INCLUDE[ws2003](../../../../includes/ws2003-md.md)]: utiliser le [outil d’inscription ServiceModel (ServiceModelReg.exe)](../../../../docs/framework/wcf/servicemodelreg-exe.md) l’outil pour inscrire WCF avec IIS : pour utiliser cet outil, tapez **ServiceModelReg.exe /i /x** dans Visual Studio invite de commandes. Pour ouvrir cette invite de commandes, cliquez sur le bouton Démarrer, sélectionnez **Tous les programmes**, **Microsoft Visual Studio 2012**, **Visual Studio Tools**et **Invite de commandes Visual Studio**.  
  
-   [!INCLUDE[wv](../../../../includes/wv-md.md)]: installez le sous-composant Windows Communication Foundation Activation Components du [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)]. Pour ce faire, dans le panneau de configuration, cliquez sur **Ajout / Suppression de programmes** , puis **ajouter\/supprimer des composants Windows**. Cette procédure active l' **Assistant Composants de Windows**.  
  
-   Windows 7 :  
  
 Enfin, vous devez vérifier qu'ASP.NET est configuré pour utiliser le .NET Framework version 4. Pour cela, exécutez l'outil ASPNET_Regiis avec l'option –i. Pour plus d’informations, consultez [ASP.NET IIS Registration, outil](http://go.microsoft.com/fwlink/?LinkId=201186)  
  
## <a name="create-a-new-iis-application-or-reuse-an-existing-aspnet-application"></a>Créer une nouvelle application IIS ou réutiliser une application ASP.NET existante  
 Les services WCF hébergés dans IIS doivent résider dans une application IIS. Vous pouvez créer une nouvelle application IIS pour héberger les services WCF exclusivement. Vous pouvez également déployer un service WCF dans une application existante qui héberge déjà [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)] contenu (par exemple, les pages .aspx et services Web ASP.NET [ASMX]). Pour plus d’informations sur ces options, consultez le « hébergement WCF-côte avec ASP.NET » et « Hébergement des Services WCF en Mode de compatibilité ASP.NET » dans les sections [Services WCF et ASP.NET](../../../../docs/framework/wcf/feature-details/wcf-services-and-aspnet.md).  
  
 Notez que [!INCLUDE[iis601](../../../../includes/iis601-md.md)] et les versions ultérieures redémarrent périodiquement une application de programmation orientée objet isolée. La valeur par défaut est 1740 minutes. La valeur maximale est de 71,582 minutes. Ce redémarrage peut être désactivé. Pour plus d’informations sur cette propriété, consultez le [PeriodicRestartTime](http://go.microsoft.com/fwlink/?LinkId=109968).  
  
## <a name="create-an-svc-file-for-the-wcf-service"></a>Créer un fichier .svc pour le service WCF  
 Les services WCF hébergés dans IIS sont représentés en tant que fichiers de contenu spéciaux (fichiers .svc) à l’intérieur de l’application IIS. Ce modèle est semblable à la façon dont les pages ASMX sont représentées dans une application IIS sous la forme de fichiers .asmx. Un fichier .svc contient une directive de traitement spécifiques à WCF ([@ServiceHost](../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md)) qui permet à l’infrastructure d’hébergement WCF activer les services hébergés en réponse aux messages entrants. La syntaxe la plus courante d'un fichier .svc se trouve dans l'instruction suivante.  
  
```  
<% @ServiceHost Service="MyNamespace.MyServiceImplementationTypeName" %>  
```  
  
 Elle se compose de la directive [@ServiceHost](../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md) et de l’attribut unique `Service`. La valeur de l'attribut `Service` est le nom de type du Common Language Runtime (CLR) de l'implémentation de service. L'utilisation de cette directive revient essentiellement à créer un hôte de service à l'aide du code suivant :  
  
```  
new ServiceHost( typeof( MyNamespace.MyServiceImplementationTypeName ) );  
```  
  
 La configuration d'hébergement supplémentaire, telle que la création d'une liste d'adresses de base pour le service peut aussi être effectuée. Vous pouvez aussi utiliser un <xref:System.ServiceModel.Activation.ServiceHostFactory> personnalisé pour étendre la directive et l'utiliser avec des solutions d'hébergement personnalisées. Les applications IIS qui hébergent des services WCF ne sont pas chargées de gérer la création et la durée de vie de <xref:System.ServiceModel.ServiceHost> instances. L’infrastructure d’hébergement géré WCF crée le nécessaire <xref:System.ServiceModel.ServiceHost> instance dynamiquement lorsque la première demande est reçue pour le fichier .svc. L'instance n'est pas libérée tant qu'elle n'est pas fermée explicitement par le code ou que l'application est recyclée.  
  
 Pour plus d’informations sur la syntaxe des fichiers .svc, consultez [ @ServiceHost ](../../../../docs/framework/configure-apps/file-schema/wcf-directive/servicehost.md).  
  
## <a name="deploy-the-service-implementation-to-the-iis-application"></a>Déployer l'implémentation de service vers l'application IIS  
 Les services WCF hébergés dans IIS utilisent le même modèle de compilation dynamique en tant que [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)]. Comme avec [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], vous pouvez déployer le code d’implémentation pour les services WCF hébergé par IIS différentes à différents emplacements, procédez comme suit :  
  
-   Sous forme d'un fichier .dll précompilé situé dans le cache d'assembly global (GAC, Global Assembly Cache) ou dans le répertoire \bin de l'application. Les binaires précompilés ne sont pas mis à jour tant qu'une nouvelle version de la bibliothèque de classes n'a pas été déployée.  
  
-   Sous la forme de fichiers sources non compilés situés dans le répertoire \App_Code de l'application. Les fichiers sources situés dans ce répertoire sont requis dynamiquement lors du traitement de la première demande de l'application. Les modifications apportées aux fichiers dans le répertoire \App_Code provoque le recyclage et la recompilation de l'application toute entière lorsque la demande suivante est reçue.  
  
-   Sous la forme de code non compilé placé directement dans le fichier .svc. Code d’implémentation peut également être situé inline dans le fichier du service .svc, après la @ServiceHost directive. Les transformations apportées au code inline provoquent le recyclage et la recompilation de l'application lorsque la demande suivante est reçue.  
  
 Pour plus d’informations sur la [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)] modèle de compilation, consultez [vue d’ensemble de la Compilation ASP.NET](http://go.microsoft.com/fwlink/?LinkId=94773).  
  
## <a name="configure-the-wcf-service"></a>Configurer le service WCF  
 Les services WCF hébergés dans IIS stockent leur configuration dans le fichier Web.config des applications. Services hébergés dans IIS utilisent les mêmes éléments de configuration et la syntaxe en tant que services WCF hébergés en dehors d’IIS. Toutefois, les contraintes suivantes sont uniques à l'environnement d'hébergement IIS :  
  
-   Adresses de base pour les services hébergés dans IIS.  
  
-   Applications de services d’hébergement de WCF en dehors d’IIS peuvent contrôler l’adresse de base des services qu’elles hébergent en passant un ensemble de base de l’adresse URI à la <xref:System.ServiceModel.ServiceHost> constructeur ou en fournissant un [ \<hôte >](../../../../docs/framework/configure-apps/file-schema/wcf/host.md) élément dans le configuration du service. Les services hébergés dans IIS n'ont pas la capacité de contrôler leur adresse de base ; l'adresse de base d'un service hébergé dans IIS est l'adresse de son fichier .svc.  
  
### <a name="endpoint-addresses-for-iis-hosted-services"></a>Adresses de point de terminaison pour les services hébergés dans IIS  
 Lorsqu'elles sont hébergées dans IIS, les adresses de point de terminaison sont toujours considérées relatives à l'adresse du fichier .svc qui représente le service. Par exemple, si l’adresse de base d’un service WCF est http://localhost/Application1/MyService.svc avec la configuration de point de terminaison suivante.  
  
```xml  
<endpoint address="anotherEndpoint" .../>  
```  
  
 Cela fournit un point de terminaison qui peut être atteint à «http://localhost/Application1/MyService.svc/anotherEndpoint».  
  
 De même, l’élément de configuration de point de terminaison qui utilise une chaîne vide comme l’adresse relative fournit un point de terminaison accessible à http://localhost/Application1/MyService.svc, qui est l’adresse de base.  
  
```xml  
<endpoint address="" ... />  
```  
  
 Vous devez toujours utiliser des adresses de point de terminaison relatives pour les points de terminaison de service hébergés dans IIS. En fournissant une adresse de point de terminaison complet (par exemple, http://localhost/MyService.svc) peut entraîner des erreurs dans le déploiement du service si l’adresse de point de terminaison ne pointe pas vers l’application IIS qui héberge le service exposant le point de terminaison. L'utilisation d'adresses de point de terminaison relatives pour les services hébergés évite ces risques de conflits.  
  
### <a name="available-transports"></a>Transports disponibles  
 Les services WCF hébergés dans IIS 5.1 et [!INCLUDE[iis601](../../../../includes/iis601-md.md)] sont limités à l’utilisation de communication basée sur HTTP. Sur ces plateformes IIS, configurer un service hébergé pour utiliser une liaison non-HTTP entraîne une erreur pendant l'activation du service. Pour [!INCLUDE[iisver](../../../../includes/iisver-md.md)], les transports pris en charge incluent HTTP, Net.TCP, Net.Pipe, Net.MSMQ et msmq.formatname pour la compatibilité descendante avec les applications MSMQ existantes.  
  
### <a name="http-transport-security"></a>Sécurité de transport HTTP  
 Les services WCF hébergés dans IIS peuvent tirer parti du protocole HTTP (par exemple, HTTP et HTTPS schémas d’authentification tels que Basic, Digest et l’authentification intégrée Windows) de sécurité de transport tant que le répertoire virtuel IIS qui contient le service prend en charge les Paramètres. Les paramètres de la sécurité de transport HTTP sur la liaison d'un point de terminaison hébergé doivent correspondre aux paramètres de sécurité de transport sur le répertoire virtuel IIS qui la contient.  
  
 Par exemple, un point de terminaison WCF configuré pour utiliser l’authentification digest HTTP doit résider dans un répertoire virtuel IIS qui est également configuré pour permettre l’authentification digest HTTP. Combinaisons non appariées de paramètres IIS et les paramètres de point de terminaison WCF génère une erreur lors de l’activation du service.  
  
## <a name="see-also"></a>Voir aussi  
 [Hébergement dans les services IIS (Internet Information Services)](../../../../docs/framework/wcf/feature-details/hosting-in-internet-information-services.md)  
 [Bonnes pratiques pour l’hébergement dans Internet Information Services](../../../../docs/framework/wcf/feature-details/internet-information-services-hosting-best-practices.md)  
 [Fonctionnalités d’hébergement de Windows Server App Fabric](http://go.microsoft.com/fwlink/?LinkId=201276)
