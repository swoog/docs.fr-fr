---
title: Services WCF et ASP.NET
ms.date: 03/30/2017
ms.assetid: b980496a-f0b0-4319-8e55-a0f0fa32da70
ms.openlocfilehash: 6cfd4f8a5dc2a7835cba409a37b09166e49e8df3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="wcf-services-and-aspnet"></a>Services WCF et ASP.NET
Cette rubrique décrit l’hébergement Windows Communication Foundation (WCF) services côte à côte avec ASP.NET et leur hébergement en mode de compatibilité ASP.NET.  
  
## <a name="hosting-wcf-side-by-side-with-aspnet"></a>Hébergement côte à côte de WCF avec ASP.NET  
 Services WCF hébergés dans Internet Information Services (IIS) peuvent être sur le même emplacement. Les pages ASPX et les services Web ASMX dans un domaine d’Application unique et commun. ASP.NET fournit des services d’infrastructure communs tels que la gestion AppDomain et la compilation dynamique pour WCF et le runtime HTTP ASP.NET. La configuration par défaut pour WCF est côte à côte avec ASP.NET.  
  
 ![Les Services WCF et ASP .NET : état de partage](../../../../docs/framework/wcf/feature-details/media/hostingwcfwithaspnet.gif "HostingWCFwithASPNET")  
  
 L’exécution d’ASP.NET HTTP gère des demandes ASP.NET mais ne pas participe au traitement des demandes destinées aux services WCF, même si ces services sont hébergés dans le même AppDomain, car ASP.NET n’est contenu. Au lieu de cela, le modèle de Service WCF intercepte les messages adressés aux services WCF et de les acheminer via la pile de transport ou du canal WCF.  
  
 Les résultats du modèle côte à côte est le suivant :  
  
-   Les services ASP.NET et WCF peuvent partager l’état AppDomain. Étant donné que les deux infrastructures peuvent coexister dans le même AppDomain, WCF peut également partager l’état AppDomain avec ASP.NET (y compris les variables statiques, des événements et ainsi de suite).  
  
-   Les services WCF se comportent de façon cohérente, indépendant du transport et environnement d’hébergement. L'exécution d'ASP.NET HTTP est intentionnellement associée à l'environnement d'hébergement de IIS/ASP.NET et à la communication HTTP. À l’inverse, WCF est conçu pour un comportement cohérent entre les environnements d’hébergement (WCF comporte toujours à la fois à l’intérieur et en dehors d’IIS) et sur le transport (un service hébergé dans IIS 7.0 et versions ultérieur a un comportement cohérent entre les points de terminaison qu’il expose, même si certaines de ces points de terminaison utilisent des protocoles autres que HTTP).  
  
-   Dans un AppDomain, les fonctionnalités implémentées par le runtime HTTP s’appliquent au contenu ASP.NET mais pas à WCF. Nombre de fonctionnalités spécifiques à HTTP de la plate-forme d’application ASP.NET ne s’appliquent pas aux Services WCF hébergés dans un AppDomain qui contient le contenu ASP.NET. Voici des exemples de ces fonctionnalités :  
  
    -   HttpContext : <xref:System.Web.HttpContext.Current%2A> est toujours `null` lors de l’accès à partir d’un service WCF. Utilisez <!--zz <xref:System.ServiceModel.OperationContext.Current.RequestContext>--> `RequestContext` à la place.  
  
    -   Autorisation basée sur le fichier : modèle de sécurité le WCF n’autorise pas la liste de contrôle d’accès (ACL) appliquée au fichier .svc du service lorsque vous décidez si une demande de service est autorisée.  
  
    -   Basée sur la configuration de l’autorisation d’URL : De même, le modèle de sécurité WCF n’est pas conforme à toutes les règles d’autorisation basée sur l’URL spécifiées dans System.Web \<autorisation > élément de configuration. Si un service se trouve dans un espace d’URL sécurisé par ASP, ces paramètres sont ignorés pour les demandes WCF. Règles d’autorisation de NET URL.  
  
    -   Extensibilité HttpModule : infrastructure d’hébergement WCF l’intercepte WCF demandes quand le <xref:System.Web.HttpApplication.PostAuthenticateRequest> événement est déclenché et ne retourne pas de traitement au pipeline HTTP ASP.NET. Les modules encodés pour intercepter les demandes à des étapes ultérieures du pipeline n’interceptent pas les demandes WCF.  
  
    -   Emprunt d’identité ASP.NET : par défaut, WCF demande toujours s’exécute le processus IIS identité, même si ASP.NET est configuré pour activer l’emprunt d’identité à l’aide de System.Web \<identity impersonate = « true » / > option de configuration.  
  
 Ces restrictions s’appliquent uniquement aux services WCF hébergés dans une application IIS. Le comportement du contenu ASP.NET n’est pas affecté par la présence de WCF.  
  
 Applications WCF qui nécessitent les fonctionnalités traditionnellement fournies par le pipeline HTTP doivent envisager d’utiliser les équivalents WCF, hôte et indépendant du transport :  
  
-   <xref:System.ServiceModel.OperationContext> plutôt que <xref:System.Web.HttpContext>.  
  
-   <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior> au lieu de l'autorisation de fichier/URL de ASP.NET.  
  
-   <xref:System.ServiceModel.Dispatcher.IDispatchMessageInspector> ou des canaux en couche personnalisés au lieu des modules HTTP.  
  
-   Emprunt d’identité pour chaque opération à l’aide de WCF au lieu de l’emprunt d’identité System.Web.  
  
 Vous pouvez également envisager d’exécuter vos services en mode de compatibilité ASP.NET de WCF.  
  
## <a name="hosting-wcf-services-in-aspnet-compatibility-mode"></a>Hébergement des services WCF en mode de compatibilité ASP.NET  
 Bien que le modèle de WCF est conçu pour un comportement cohérent entre les environnements d’hébergement et les transports, il existe souvent des scénarios où une application ne requiert pas ce degré de souplesse. Mode de compatibilité ASP.NET de WCF est approprié pour les scénarios qui ne requièrent pas la possibilité d’hôte en dehors d’IIS ou pour communiquer via des protocoles autres que HTTP, mais qui utilisent toutes les fonctionnalités de la plate-forme d’application Web ASP.NET.  
  
 Contrairement à la configuration côte à côte par défaut, où l’infrastructure d’hébergement WCF intercepte les messages WCF et les route hors du pipeline HTTP, les services WCF en cours d’exécution en Mode de compatibilité ASP.NET participent pleinement au cycle de vie de demande HTTP ASP.NET. En mode de compatibilité, les services WCF utilisent le pipeline HTTP via une <xref:System.Web.IHttpHandler> implémentation, similaire aux requêtes de façon pour les pages ASPX et les services Web ASMX sont gérées. Par conséquent, WCF a un comportement identique à ASMX en ce qui concerne les fonctionnalités ASP.NET suivantes :  
  
-   <xref:System.Web.HttpContext>: Les services WCF en cours d’exécution en Mode de compatibilité ASP.NET peuvent accéder à <xref:System.Web.HttpContext.Current%2A> et son état associé.  
  
-   Autorisation basée sur le fichier : services WCF en cours d’exécution en mode de compatibilité ASP.NET peuvent être sécurisés en joignant des listes de contrôle d’accès (ACL) du système de fichiers au fichier .svc du service.  
  
-   Autorisation d’URL configurable : ASP. Règles d’autorisation de NET URL sont appliquées pour les demandes WCF lorsque le service WCF s’exécute en Mode de compatibilité ASP.NET.  
  
-   <xref:System.Web.HttpModuleCollection> extensibilité : les services WCF, car en cours d’exécution en Mode de compatibilité ASP.NET participent pleinement au cycle de vie de demande HTTP ASP.NET, n’importe quel module HTTP configuré dans le pipeline HTTP est en mesure de fonctionner sur les demandes WCF avant et après l’appel de service.  
  
-   Emprunt d’identité ASP.NET : Les services WCF exécutées à l’aide de l’identité actuelle de ASP.NET d’emprunter l’identité thread, ce qui peut être différent de celui de l’identité du processus IIS si l’emprunt d’identité ASP.NET a été activé pour l’application. Si l’emprunt d’identité ASP.NET et WCF sont toutes deux activées pour une opération de service particulier, l’implémentation de service s’exécute finalement à l’aide de l’identité obtenue de WCF.  
  
 Mode de compatibilité ASP.NET de WCF est activé au niveau de l’application via la configuration suivante (situé dans le fichier Web.config de l’application) :  
  
```xml  
<system.serviceModel>  
    <serviceHostingEnvironment aspNetCompatibilityEnabled="true" />  
</system.serviceModel>  
```  
  
 Cette valeur par défaut est «`true`» si non spécifié. La valeur «`false`» indique que tous les services WCF en cours d’exécution dans l’application ne s’exécutera pas en Mode de compatibilité ASP.NET.  
  
 Étant donné que le Mode de compatibilité ASP.NET implique des sémantiques de traitement de demande fondamentalement diffèrent de la valeur par défaut WCF, les implémentations de service individuels ont la possibilité contrôle si elles s’exécutent à l’intérieur d’une application qui ASP.NET Mode de compatibilité a été activé. Les services peuvent utiliser <xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsAttribute> pour indiquer s'ils prennent en charge le mode de compatibilité ASP.NET. La valeur par défaut de cet attribut est <xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsMode.Allowed>.  
  
 `[AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]`  
  
 `public class CalculatorService : ICalculatorSession`  
  
 `{//Implement calculator service methods.}`  
  
 Le tableau suivant illustre comment le paramètre de mode de compatibilité défini au niveau de l'application interagit avec le niveau de prise en charge déclaré du service :  
  
|Paramètre de mode de compatibilité défini au niveau de l'application|[AspNetCompatibilityRequirementsMode]<br /><br /> Paramètre|Résultat observé|  
|--------------------------------------------------|---------------------------------------------------------|---------------------|  
|aspNetCompatibilityEnabled = «`true`»|<xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsMode.Required>|Le service est activé.|  
|aspNetCompatibilityEnabled = «`true`»|<xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsMode.Allowed>|Le service est activé.|  
|aspNetCompatibilityEnabled = «`true`»|<xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsMode.NotAllowed>|Une erreur d'activation se produit lorsque le service reçoit un message.|  
|aspNetCompatibilityEnabled = «`false`»|<xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsMode.Required>|Une erreur d'activation se produit lorsque le service reçoit un message.|  
|aspNetCompatibilityEnabled = «`false`»|<xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsMode.Allowed>|Le service est activé.|  
|aspNetCompatibilityEnabled = «`false`»|<xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsMode.NotAllowed>|Le service est activé.|  
  
> [!NOTE]
>  IIS 7.0 et WAS permet de communiquer via des protocoles autres que HTTP, les services WCF. Toutefois, les services WCF en cours d’exécution dans les applications qui ont activé le mode de compatibilité ASP.NET ne sont pas autorisés à exposer des points de terminaison non-HTTP. Une telle configuration génère une exception d'activation lorsque le service reçoit son premier message.  
  
 Pour plus d’informations sur l’activation du mode de compatibilité ASP.NET pour les services WCF, consultez <xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsMode> et [compatibilité ASP.NET](../../../../docs/framework/wcf/samples/aspnet-compatibility.md) exemple.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Activation.AspNetCompatibilityRequirementsAttribute>  
 [Fonctionnalités d’hébergement de Windows Server App Fabric](http://go.microsoft.com/fwlink/?LinkId=201276)
