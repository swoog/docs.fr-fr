---
title: AspNetRouteIntegration
ms.date: 03/30/2017
ms.assetid: 0638ce0e-d053-47df-a447-688e447a03fb
ms.openlocfilehash: 8d9a0710e5106cbc3d02a06e81f4f8ed9ae3e03b
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43475879"
---
# <a name="aspnetrouteintegration"></a>AspNetRouteIntegration
Cet exemple montre comment héberger un service REST Windows Communication Foundation (WCF) à l’aide d’itinéraires ASP.NET. Le [Basic Resource Service](../../../../docs/framework/wcf/samples/basic-resource-service.md) exemple montre une version auto-hébergée de ce scénario et traite en détail l’implémentation de service. Cette rubrique met l’accent sur la fonctionnalité d’intégration ASP.NET. Pour plus d’informations sur le routage ASP.NET, consultez <xref:System.Web.Routing>.  
  
## <a name="sample-details"></a>Détails de l'exemple  
 Le service WCF expose une collection de clients de façon orientée/REST ressources. Tout comme un service WCF basé sur SOAP, le service peut être hébergé dans ASP.NET à l’aide d’un fichier .svc. Toutefois, cette façon de procéder est rarement celle à privilégier pour les scénarios HTTP, car elle implique la présence de .svc dans l'URL du service. En outre, elle requiert le déploiement d'un fichier .svc avec la bibliothèque du service. Ces limitations peuvent être évitées en hébergeant le service à l'aide d'itinéraires ASP.NET, comme le montre cet exemple.  
  
 L'exemple héberge le service dans ASP.NET en ajoutant un <xref:System.ServiceModel.Activation.ServiceRoute> dans un fichier Global.asax. Le <xref:System.ServiceModel.Activation.ServiceRoute> spécifie le type du service (‘Service’ dans ce cas), le type de la fabrique d'hôte de service à utiliser pour le service (<xref:System.ServiceModel.Activation.WebServiceHostFactory> dans ce cas) et l'adresse de base HTTP pour le service (‘~/Customers’ dans ce cas).  
  
 L'exemple inclut en outre un fichier Web.config qui ajoute l'<xref:System.Web.Routing.UrlRoutingModule> (pour activer les itinéraires ASP.NET) et comprend la configuration du service. En particulier, la configuration configure le service WCF avec une valeur par défaut <xref:System.ServiceModel.Description.WebHttpEndpoint> qui a le <xref:System.ServiceModel.Description.WebHttpEndpoint.HelpEnabled%2A> à `true`. Par conséquent, l’infrastructure WCF crée une page d’aide HTML automatique à `http://localhost/Customers/help` qui fournit des informations sur la construction HTTP demande au service et comment accéder à la réponse du service HTTP – par exemple, un exemple de client détails sont représentés au format XML et JSON.  
  
 Exposer ainsi la collection customer (et plus généralement, n'importe quelle ressource) permet à un client d'interagir avec un service de façon uniforme en utilisant des URI et HTTP `GET`, `PUT`, `DELETE` et `POST`.  
  
 Le fichier program.cs du projet Client montre comment un tel client peut être créé à l'aide de <xref:System.Net.HttpWebRequest>. Notez qu'il ne s'agit là que de l'un des moyens d'accéder à un service WCF. Il est également possible d’accéder au service à l’aide d’autres classes .NET Framework telles que la fabrication de canal WCF et <xref:System.Net.WebClient>. Autres exemples du SDK (telles que la [Service HTTP de base](../../../../docs/framework/wcf/samples/basic-http-service.md) exemple et le [la sélection automatique du Format](../../../../docs/framework/wcf/samples/automatic-format-selection.md) exemple) montrent comment utiliser ces classes pour communiquer avec un service WCF.  
  
 Cet exemple est composé de 3 projets :  
  
 Service  
 Projet d'application Web qui inclut un service HTTP WCF hébergé dans ASP.NET.  
  
 Client  
 Projet d'application console qui passe des appels au service.  
  
 Communes  
 Bibliothèque partagée qui contient le type `Customer` utilisé par le client et le service. Lorsque l'application console Client s'exécute, le client adresse des requêtes au service et affiche les informations pertinentes des réponses dans la fenêtre de console.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Ouvrez la solution de l'exemple ASP.NET Routes Integration dans [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)].  
  
2.  Appuyez sur Ctrl+Maj+B pour générer la solution.  
  
3.  Si elle n’est pas déjà ouverte, appuyez sur « CTRL + W, S » pour ouvrir le **l’Explorateur de solutions** fenêtre.  
  
4.  À partir de la **l’Explorateur de solutions** avec le bouton droit de windows, le **Service** de projet et placez le curseur sur le **déboguer** option de menu contextuel afin que le **Démarrer Nouvelle Instance** menu contextuel s’affiche et sélectionnez **démarrer une nouvelle Instance**.  Cette opération lance le serveur de développement ASP.NET, qui héberge le service.  
  
5.  À partir de la **l’Explorateur de solutions** avec le bouton droit de windows, le **Client** de projet et placez le curseur sur le **déboguer** option de menu contextuel afin que le **démarrer une nouvelle Instance** menu contextuel s’affiche et sélectionnez **démarrer une nouvelle Instance**.  
  
6.  La fenêtre de console du client apparaît et fournit l'URI du service en cours d'exécution, ainsi que l'URI de sa page d'aide HTML. Vous pouvez à tout moment consulter la page d'aide HTML en tapant son URI dans un navigateur. Lorsque l'exemple s'exécute, le client écrit l'état de l'activité actuelle.  
  
7.  Appuyez sur une touche quelconque pour arrêter l'application console Client.  
  
8.  Appuyez sur MAJ + F5 pour arrêter le débogage du service et dans la zone de Notification Windows, cliquez sur l’icône de serveur de développement ASP.NET et sélectionnez **arrêter** dans le menu contextuel.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Web\AspNetRouteIntegration`  
  
## <a name="see-also"></a>Voir aussi
