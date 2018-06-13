---
title: Meilleures pratiques pour l'hébergement dans Internet Information Services
ms.date: 03/30/2017
ms.assetid: 0834768e-9665-46bf-86eb-d4b09ab91af5
ms.openlocfilehash: 119f14df9d46883a33272903558d83128501b293
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33495760"
---
# <a name="internet-information-services-hosting-best-practices"></a>Meilleures pratiques pour l'hébergement dans Internet Information Services
Cette rubrique décrit quelques-unes des meilleures pratiques pour l’hébergement des services Windows Communication Foundation (WCF).  
  
## <a name="implementing-wcf-services-as-dlls"></a>Implémentation des services WCF comme DLL  
 Implémentation d’un service WCF service comme une DLL qui est déployée dans le répertoire \bin d’une application Web vous permet de que réutiliser le service en dehors du modèle d’application Web, par exemple, dans un environnement de test qui ne disposent pas de Services Internet (IIS) sont déployées.  
  
## <a name="service-hosts-in-iis-hosted-applications"></a>Hôtes de service dans les applications hébergées par IIS  
 N'utilisez pas les API auto-hébergées impératives pour créer de nouveaux hôtes de service qui écoutent les transports de réseau non pris en charge en mode natif par l'environnement d'hébergement IIS (par exemple, [!INCLUDE[iis601](../../../../includes/iis601-md.md)] pour héberger les services TCP, étant donné que la communication TCP n'est pas prise en charge en mode natif sur [!INCLUDE[iis601](../../../../includes/iis601-md.md)]). Cette approche n'est pas recommandée. Les hôtes de service créés de manière impérative ne sont pas connus dans l'environnement d'hébergement IIS. Le point critique est que le traitement effectué par les services créés de manière impérative n'est pas pris en charge par les services IIS lorsqu'il détermine si le pool d'applications d'hébergement est inactif. Le résultat est que les applications qui possèdent ce type d'hôtes de service ont un environnement d'hébergement IIS qui élimine systématiquement les processus d'hôte IIS.  
  
## <a name="uris-and-iis-hosted-endpoints"></a>URI et points de terminaison hébergés par IIS  
 Les points de terminaison pour un service hébergé par IIS doivent être configurés à l'aide d'URI relatifs, pas d'adresses absolues. De cette manière, vous êtes certain que l'adresse du point de terminaison se situe dans le jeu des adresses URI qui appartiennent à l'application d'hébergement et que l'activation basée sur message se produit comme prévu.  
  
## <a name="state-management-and-process-recycling"></a>Gestion des états et recyclage de processus  
 L'environnement d'hébergement IIS est optimisé pour les services qui ne maintiennent pas l'état local en mémoire. Les services IIS recyclent le processus hôte en réponse à divers événements externes et internes, ce qui peut entraîner la perte de tout état volatil stocké exclusivement dans la mémoire. Les services hébergés dans IIS doivent stocker leur état en dehors du processus (par exemple, dans une base de données) ou dans un cache en mémoire qui peut être recréé facilement si un événement de recyclage d'application se produit.  
  
> [!NOTE]
>  Les protocoles utilise WCF pour la fiabilité de la couche de message et de sécurité rendre l’utilisation de l’état en mémoire volatile. Les sessions fiables WCF et des sessions de sécurité peuvent se fermer inopinément en raison du recyclage d’application. Les applications hébergées sur IIS qui utilisent ces protocoles doivent soit dépendre d’un élément autre que la clé de session fournie par WCF pour corréler l’état de la couche application (par exemple, une construction de la couche application ou un en-tête de corrélation personnalisé) ou désactiver IIS recyclage de processus pour l’application hébergée.  
  
## <a name="optimizing-performance-in-middle-tier-scenarios"></a>Optimisation des performances dans les scénarios de couche intermédiaire  
 Pour des performances optimales dans un *scénario de couche intermédiaire*: un service qui appelle d’autres services en réponse aux messages entrants, instanciez le client du service WCF au service distant une fois et réutilisez-le dans plusieurs entrant demandes. L’instanciation des clients de service WCF est une opération coûteuse par rapport à un service d’appeler sur une instance de client existant et scénarios de couche intermédiaire produisent des gains de performances distincts en mettant en cache des clients distants entre les demandes. Les clients du service WCF sont thread-safe, il n’est pas nécessaire synchroniser l’accès à un client sur plusieurs threads.  
  
 Les scénarios de couche intermédiaire produisent également des gains de performance en utilisant les API asynchrones générées par l'option `svcutil /a`. Le `/a` option entraîne la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour générer `BeginXXX/EndXXX` méthodes pour chaque opération de service, qui autorise les appels potentiellement longue services à distance doit être effectuée sur threads d’arrière-plan.  
  
## <a name="wcf-in-multi-homed-or-multi-named-scenarios"></a>WCF dans des scénarios multi-résidents ou multi-nommés  
 Vous pouvez déployer des services WCF à l’intérieur d’une batterie de serveurs Web IIS, où un ensemble d’ordinateurs partagent un nom externe commun (tel que http://www.contoso.com) mais sont adressés individuellement par des noms d’hôte (par exemple, http://www.contoso.com peut diriger le trafic vers deux ordinateurs différents nommé http://machine1.internal.contoso.com et http://machine2.internal.contoso.com). Ce scénario de déploiement est entièrement pris en charge par WCF, mais requiert une configuration spéciale du site Web IIS qui héberge les services WCF pour afficher le nom d’hôte correct (externe) dans les métadonnées du service (Web Services Description Language).  
  
 Pour vous assurer que le nom d’hôte correct apparaisse dans les métadonnées de service que WCF génère, configurez l’identité par défaut pour le site Web IIS qui héberge les services WCF pour utiliser un nom d’hôte explicite. Par exemple, les ordinateurs qui résident dans la ferme www.contoso.com doivent utiliser une liaison de site IIS de * : 80 : www.contoso.com pour HTTP et \*: 443:www.contoso.com pour le protocole HTTPS.  
  
 Vous pouvez configurer des liaisons de site web IIS en utilisant le composant logiciel enfichable IIS Microsoft Management Console (MMC).  
  
## <a name="application-pools-running-in-different-user-contexts-overwrite-assemblies-from-other-accounts-in-the-temporary-folder"></a>Les pools d’applications qui s’exécutent dans des contextes d’utilisateur différents remplacent des assemblys d’autres comptes dans le dossier temporaire  
 Pour garantir que les pools d'applications qui s'exécutent dans les contextes d'utilisateur différents ne peuvent pas remplacer d'assemblys d'autres comptes dans le dossier des fichiers [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] temporaire, utilisez des identités et des dossiers temporaires différents pour des applications différentes. Par exemple, si vous avez deux applications virtuelles /Application1 et / Application2, vous pouvez créer deux pools d'applications, A et B, avec deux identités différentes. Le pool d'applications A peut s'exécuter sous une identité d'utilisateur (user1), et le pool d'applications B peut s'exécuter sous une autre identité d'utilisateur (user2), et configurer /Application1 pour utiliser A et /Application2 pour utiliser B.  
  
 Dans le fichier Web.config, vous pouvez configurer le dossier temporaire à l’aide de \< system.web/compilation/@tempFolder>. Pour/Application1, il peut être « c:\tempForUser1 » et pour application2, il peut être « c:\tempForUser2 ». Accordez l’autorisation en écriture correspondante à ces dossiers pour les deux identités.  
  
 Dès lors, user2 ne peut pas modifier le dossier de génération du code pour /application2 (sous c:\tempForUser1).  
  
## <a name="enabling-asynchronous-processing"></a>Activation du traitement asynchrone  
 Par défaut, les messages envoyés à un service WCF hébergé sous IIS 6.0 et versions antérieures sont traités de façon synchrone. ASP.NET appelle WCF sur son propre thread (le thread de travail ASP.NET) et WCF utilise un autre thread pour traiter la demande. WCF met en attente le thread de travail ASP.NET jusqu'à la fin du traitement. Cela conduit au traitement synchrone des demandes. Traitement des demandes de façon asynchrone permet de plus grande évolutivité car il réduit le nombre de threads requis pour traiter une demande – WCF ne contient pas le thread ASP.NET lors du traitement de la demande. Utilisation d’un comportement asynchrone n’est pas recommandée pour les ordinateurs exécutant IIS 6.0 car il n’existe aucun moyen de limiter les demandes entrantes qui exposent le serveur à *par déni de Service* attaques (DOS). Depuis IIS 7.0, une limitation des demandes simultanées a été mise en place : `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\ASP.NET\2.0.50727.0]"MaxConcurrentRequestsPerCpu`. Grâce à cette nouvelle limitation, l'utilisation du traitement asynchrone peut s'effectuer en toute sécurité.  Par défaut dans IIS 7.0, le gestionnaire asynchrone et le module sont inscrits. Si cette option a été désactivée, vous pouvez activer manuellement le traitement asynchrone des demandes dans le fichier Web.config de votre application. Les paramètres que vous utilisez dépendent de votre paramètre `aspNetCompatibilityEnabled`. Si `aspNetCompatibilityEnabled` a la valeur `false`, configurez `System.ServiceModel.Activation.ServiceHttpModule` comme illustré dans l'extrait de configuration suivant.  
  
```xml  
<system.serviceModel>  
    <serviceHostingEnvironment aspNetCompatibilityEnabled="false" />      
  </system.serviceModel>  
  <system.webServer>  
    <modules>  
      <remove name="ServiceModel"/>  
      <add name="ServiceModel"   
           preCondition="integratedMode,runtimeVersionv2.0"   
           type="System.ServiceModel.Activation.ServiceHttpModule, System.ServiceModel,Version=3.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>  
    </modules>  
    </system.webServer>  
```  
  
 Si `aspNetCompatibilityEnabled` a la valeur `true`, configurez `System.ServiceModel.Activation.ServiceHttpHandlerFactory` comme illustré dans l'extrait de configuration suivant.  
  
```xml  
<system.serviceModel>  
    <serviceHostingEnvironment aspNetCompatibilityEnabled="true" />      
  </system.serviceModel>  
  <system.webServer>  
    <handlers>  
          <clear/>  
          <add name="TestAsyncHttpHandler"   
               path="*.svc"   
               verb="*"   
               type="System.ServiceModel.Activation.ServiceHttpHandlerFactory, System.ServiceModel, Version=3.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"           
               />  
    </handlers>      
  </system.webServer>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Exemples de services d’hébergement](http://msdn.microsoft.com/library/f703a3f6-0fba-418a-a92f-7ce75ccfa47e)  
 [Fonctionnalités d’hébergement de Windows Server App Fabric](http://go.microsoft.com/fwlink/?LinkId=201276)
