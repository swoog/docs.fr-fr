---
title: Découvrir un service avec Unique Listen Uri Mode Sample
ms.date: 03/30/2017
ms.assetid: 9a6d35b2-0469-43c8-a0c9-63623e3d2733
ms.openlocfilehash: 7e1c5ae0cb1a44c72a27566035b4bc20acbf1614
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46532557"
---
# <a name="discover-a-service-with-unique-listen-uri-mode-sample"></a>Découvrir un service avec Unique Listen Uri Mode Sample
Cet exemple montre comment découvrir un service dont la propriété <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> a la valeur <xref:System.ServiceModel.Description.ListenUriMode.Unique>. Lorsque la propriété <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> a la valeur <xref:System.ServiceModel.Description.ListenUriMode.Unique>, le caractère unique de ListenUri peut être garanti soit en définissant le port de sorte qu'il soit unique, soit en ajoutant un GUID pour que le chemin d'accès soit unique.  
  
### <a name="features-on-the-service"></a>Fonctionnalités sur le service  
 La propriété <xref:System.ServiceModel.Channels.BindingContext.ListenUriMode%2A> a la valeur <xref:System.ServiceModel.Description.ListenUriMode.Unique> pour le point de terminaison TCP. Le service est alors rendu détectable sur un point de terminaison <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>.  
  
### <a name="features-on-the-client"></a>Caractéristiques sur le client  
 Ce client se connecte au service à l'aide du `Via.Uri` en utilisant la méthode <xref:System.ServiceModel.Discovery.DiscoveryClient.Find%2A>. Le <xref:System.ServiceModel.Discovery.FindResponse> retourné par la méthode est alors interrogé pour déterminer s'il contient un <xref:System.ServiceModel.Endpoint.ListenUri%2A> valide et s'il est différent d'`Address.Uri`. Les informations appropriées sont ensuite passées à la méthode `InvokeCalculatorService`. Dans la méthode `InvokeCalculatorService`, l'appelant passe <xref:System.ServiceModel.Endpoint.ListenUri%2A>, suite à quoi un `ClientViaBehavior` avec le `Via.Uri` correct est ajouté au point de terminaison du client.  
  
##### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  À l'aide de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], ouvrez UniqueListenUriMode.sln.  
  
2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
3.  Exécutez l'application du service, générée dans le dossier [répertoire de base de la solution]\service\bin\debug.  
  
4.  Exécutez l’application du client, générée dans le dossier [répertoire de base de la solution]\Client\bin\debug.  
  
     Le client trouve le service en cours d'exécution et écrit dans la console les métadonnées publiées par le point de terminaison du service.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\UniqueListenUriMode`  
  
## <a name="see-also"></a>Voir aussi
