---
title: Points de terminaison SOAP et HTTP
ms.date: 03/30/2017
ms.assetid: e3c8be75-9dda-4afa-89b6-a82cb3b73cf8
ms.openlocfilehash: c07391ccd1f8db6e5d2cb6e0c24fc06152d7517f
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64617520"
---
# <a name="soap-and-http-endpoints"></a>Points de terminaison SOAP et HTTP
Cet exemple montre comment implémenter un service RPC et l’exposer aux formats SOAP et le format « Plain Old XML » (POX) à l’aide du modèle de programmation Web WCF. Consultez le [Service HTTP de base](../../../../docs/framework/wcf/samples/basic-http-service.md) exemple pour plus d’informations sur la liaison HTTP pour le service. Cet exemple se concentre sur les détails ayant trait à l’exposition du même service sur SOAP et HTTP au moyen de différentes liaisons.  
  
## <a name="demonstrates"></a>Démonstrations  
 Exposition d’un service RPC sur SOAP et HTTP à l’aide de WCF.  
  
## <a name="discussion"></a>Discussion  
 Cet exemple se compose de deux composants : un projet d’Application Web (Service) qui contient un service WCF et une application de console (Client) qui appelle des opérations de service à l’aide de liaisons SOAP et HTTP.  
  
 Le service WCF expose 2 opérations –`GetData` et `PutData` – qui renvoient la chaîne qui a été passée en tant qu’entrée. Les opérations de service sont annotées avec <xref:System.ServiceModel.Web.WebGetAttribute> et <xref:System.ServiceModel.Web.WebInvokeAttribute>. Ces attributs contrôlent la projection HTTP de ces opérations. Elles sont aussi annotées avec <xref:System.ServiceModel.OperationContractAttribute>, ce qui permet leur exposition sur des liaisons SOAP. La méthode `PutData` du service lève un <xref:System.ServiceModel.Web.WebFaultException>, qui est renvoyé sur HTTP avec le code d'état HTTP et sur SOAP en tant qu'erreur SOAP.  
  
 Le fichier Web.config configure le service WCF avec 3 points de terminaison :  
  
- le point de terminaison ~/service.svc/mex qui expose les métadonnées du service pour l'accès des clients SOAP ;  
  
- le point de terminaison ~/service.svc/http qui permet aux clients d’accéder au service en utilisant la liaison HTTP ;  
  
- le point de terminaison ~/service.svc/soap qui permet aux clients d’accéder au service en utilisant la liaison SOAP sur HTTP.  
  
 Le point de terminaison HTTP est configuré avec un <`webHttp`> point de terminaison standard qui a `helpEnabled` défini sur `true`. Par conséquent, le service expose sous ~/service.svc/http/help une page d'aide XHTML que les clients HTTP peuvent utiliser pour accéder au service.  
  
 Le projet client illustre l’accès au service à l’aide d’un proxy SOAP (généré par le biais **ajouter une référence de Service**) et à l’aide <xref:System.Net.WebClient>.  
  
 L'exemple se compose d'un service hébergé sur le Web et d'une application console. Lorsque l'application console s'exécute, le client adresse des requêtes au service et affiche les informations pertinentes des réponses dans la fenêtre de console.  
  
#### <a name="to-run-the-sample"></a>Pour exécuter l'exemple  
  
1. Ouvrez la solution de l'exemple des points de terminaison SOAP et HTTP.  
  
2. Appuyez sur Ctrl+Maj+B pour générer la solution.  
  
3. Si elle n’est pas déjà ouverte, appuyez sur CTRL + W, S pour ouvrir le **l’Explorateur de solutions** fenêtre.  
  
4. À partir de la **l’Explorateur de solutions** fenêtre, avec le bouton droit le **Service** de projet et placez le curseur sur le **déboguer** option de menu contextuel afin que le **démarrer une nouvelle Instance** menu contextuel s’affiche. Cliquez sur **démarrer une nouvelle Instance**. Cette opération lance le serveur de développement ASP.NET, qui héberge le service.  
  
5. À partir des fenêtres de l’Explorateur de solutions, cliquez sur le projet Client et placez le curseur sur le **déboguer** option de menu contextuel afin que le **démarrer une nouvelle Instance** menu contextuel s’affiche. Cliquez sur **démarrer une nouvelle Instance**.  
  
6. La fenêtre de console du client apparaît et fournit l'URI du service en cours d'exécution, ainsi que l'URI de sa page d'aide HTML. Vous pouvez à tout moment consulter la page d'aide HTML en tapant son URI dans un navigateur.  
  
7. Lorsque l'exemple s'exécute, le client écrit l'état de l'activité actuelle.  
  
8. Appuyez sur une touche quelconque pour arrêter l'application console Client.  
  
9. Appuyez sur MAJ+F5 pour arrêter le débogage du service.  
  
10. Dans la zone de Notification Windows, cliquez sur l’icône de serveur de développement ASP.NET et sélectionnez **arrêter** dans le menu contextuel.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Web\SoapAndHttpEndpoints`
