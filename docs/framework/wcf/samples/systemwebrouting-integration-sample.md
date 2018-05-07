---
title: Exemple SystemWebRouting Integration
ms.date: 03/30/2017
ms.assetid: f1c94802-95c4-49e4-b1e2-ee9dd126ff93
ms.openlocfilehash: 43785f84cb3852a35f1ed3bd555287842455a89b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="systemwebrouting-integration-sample"></a>Exemple SystemWebRouting Integration
Cet exemple illustre l'intégration de la couche d'hébergement avec les classes de l'espace de noms <xref:System.Web.Routing>. Les classes de l'espace de noms <xref:System.Web.Routing> permettent à une application d'utiliser des URL qui ne correspondent pas directement à une ressource physique. L'utilisation du routage Web permet au développeur de créer des adresses virtuelles pour HTTP qui sont ensuite remappées aux véritables services [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]. Cela peut être utile lorsqu'un service WCF doit être hébergé sans requérir de fichier ou ressource physique, ou lorsque des services doivent être accessibles via des URL qui ne contiennent pas de fichiers tels que .html ou .aspx. Cet exemple montre comment utiliser la classe <xref:System.Web.Routing.RouteTable> pour créer des URI virtuels qui mappent aux services en cours d'exécution définis dans global.asax. 

> [!NOTE]
>  Les classes de l'espace de noms <xref:System.Web.Routing> ne fonctionnent que pour des services hébergés sur HTTP.  
  
Cet exemple utilise WCF pour créer deux flux RSS : un `movies` flux et un `channels` de flux. Les URL pour activer les services ne contiennent pas d’extension et sont enregistrés dans le `Application_Start` méthode de la `Global` classe dérivée de la <xref:System.Web.HttpApplication> classe.  
  
> [!NOTE]
>  Cet exemple fonctionne uniquement dans les Services Internet (IIS) 7.0 et ultérieures, IIS 6.0 utilise une autre méthode pour prendre en charge des URL sans extension.  

#### <a name="to-download-this-sample"></a>Pour télécharger cet exemple
  
Cet exemple peut-être déjà être installé sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
   
`<InstallDrive>:\WF_WCF_Samples`  
   
 Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
   
`<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\Hosting\WebRoutingIntegration`  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  À l’aide de Visual Studio, ouvrez le fichier WebRoutingIntegration.sln.  
  
2.  Pour exécuter la solution et démarrer le serveur de développement Web, appuyez sur F5.  
  
     Une liste des répertoires de l'exemple s'affiche. Notez l’absence de fichiers ayant l’extension .svc.  
  
3.  Dans la barre d’adresses, ajoutez `movies` à l’URL, par conséquent, qu’il lit http://localhost:[port] /Movies et appuyez sur ENTRÉE.  
  
     Le flux movies s'affiche dans le navigateur.  
  
4.  Dans la barre d’adresses, ajoutez `channels` à l’URL, qui est donc lectures http://localhost:[port] /Channels et appuyez sur ENTRÉE.  
  
     Le flux channels s'affiche dans le navigateur.  
  
5.  Fermez le navigateur Web en appuyant sur ALT+F4.  
  
     Si le serveur de développement n’est pas terminé, cliquez sur l’icône de zone de notification et sélectionnez **arrêter**.  
  
#### <a name="to-use-this-sample-when-hosted-in-iis"></a>Pour utiliser cet exemple avec hébergement dans IIS  
  
1.  À l’aide de Visual Studio, ouvrez le fichier WebRoutingIntegration.sln.  
  
2.  Générez le projet en appuyant sur Ctrl+Maj+B.  
  
3.  Créez une application Web dans le Gestionnaire des services Internet (IIS).  
  
    1.  Dans le Gestionnaire des services Internet, bouton droit sur le **Site Web par défaut** et sélectionnez **ajouter une Application**.  
  
    2.  Pour le **alias**, tapez `WebRoutingIntegration`.  
  
    3.  Pour le **chemin d’accès physique**, sélectionnez le dossier Service situé dans le projet.  
  
    4.  Press **OK**.  
  
4.  Démarrer l’application, en double-cliquant sur l’application Web et en sélectionnant **gérer l’Application** , puis **Parcourir**.  
  
5.  Dans la barre d’adresses, ajoutez `movies` à l’URL, qui est donc lectures http://localhost:[port] /Movies et appuyez sur ENTRÉE.  
  
     Le flux movies s'affiche dans le navigateur.  
  
6.  Dans la barre d’adresses, ajoutez `channels` à l’URL, qui est donc lectures http://localhost:[port] /Channels et appuyez sur ENTRÉE.  
  
     Le flux channels s'affiche dans le navigateur.  
  
7.  Fermez le navigateur Web en appuyant sur ALT+F4.  
  
 Cet exemple montre que la couche d'hébergement est capable de composer avec les classes de l'espace de noms <xref:System.Web.Routing> pour router les requêtes de services hébergés sur HTTP.  
  
> [!NOTE]
>  Vous devez mettre à jour la version de pool d’applications par défaut à [!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)] si elle est définie à la version 2.  
  
## <a name="see-also"></a>Voir aussi  
 [Hébergement de AppFabric et exemples de persistance](http://go.microsoft.com/fwlink/?LinkId=193961)
