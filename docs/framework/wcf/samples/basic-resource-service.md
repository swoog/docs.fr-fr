---
title: Basic Resource Service
ms.date: 03/30/2017
ms.assetid: 4360063e-cc8c-4648-846e-c05a5af51a7a
ms.openlocfilehash: 2d55aecfdf6579b1de4c0cc324e59e23c251b12d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43520134"
---
# <a name="basic-resource-service"></a>Basic Resource Service
Cet exemple montre comment implémenter un service basé sur HTTP à l’aide du modèle de programmation REST Windows Communication Foundation (WCF) qui expose une collection de clients prenant en charge la récupération, ajouter, supprimer et remplacer des opérations. Cet exemple se compose de 2 composants : un service HTTP WCF auto-hébergé (Service.cs) et une application de console (program.cs) qui crée le service et effectue des appels à ce dernier.  
  
## <a name="sample-details"></a>Détails de l'exemple  
 Le service WCF expose une collection de clients de façon orientée/REST ressources. En résumé, cela implique de disposer d’URI uniques pour la collection de clients et chaque client de la collection. Le service prend en charge l'envoi d'un HTTP `GET` à l'URI de la collection pour récupérer la collection entière et d'un HTTP `POST` à l'URI de la collection pour ajouter un nouveau client à la collection. Il prend aussi en charge, à l'URI d'un client individuel, HTTP `GET` pour obtenir les informations du client, HTTP `PUT` pour remplacer les informations du client et HTTP `DELETE` pour supprimer le client de la collection. Lorsqu’un nouveau client est ajouté à la collection, le service lui assigne un URI unique et stocke l’URI avec les informations du client. Il communique aussi l'URI au client à l'aide de l'en-tête HTTP Location de la réponse.  
  
 Le fichier App.config configure le service WCF avec un <xref:System.ServiceModel.Description.WebHttpEndpoint> par défaut dont la propriété <xref:System.ServiceModel.Description.WebHttpEndpoint.HelpEnabled%2A> a la valeur `true`. Par conséquent, WCF crée une page d’aide HTML automatique sous `http://localhost:8000/Customers/help` qui fournit des informations sur la construction HTTP demande au service et comment accéder à la réponse du service HTTP – par exemple, un exemple de la façon dont les détails du client est représenté au format XML et JSON.  
  
 Exposer ainsi la collection customer (et plus généralement, n'importe quelle ressource) permet au client d'interagir avec elle de façon uniforme en utilisant des URI et HTTP `GET`, `PUT`, `DELETE` et `POST`. Program.cs montre comment un tel client peut être créé à l'aide de <xref:System.Net.HttpWebRequest>. Notez qu’il s’agit tout simplement un moyen d’accéder à un service WCF REST. Il est également possible d'accéder au service à l'aide d'autres classes .NET Framework, comme <xref:System.ServiceModel.ChannelFactory> et <xref:System.Net.WebClient>. Autres exemples du SDK (telles que la [Service HTTP de base](../../../../docs/framework/wcf/samples/basic-http-service.md) exemple et le [la sélection automatique du Format](../../../../docs/framework/wcf/samples/automatic-format-selection.md) exemple) montrent comment utiliser ces classes pour communiquer avec un service WCF.  
  
 L'exemple est constitué d'un service auto-hébergé et d'un client qui s'exécutent tous deux dans une application console. Lorsque l'application console s'exécute, le client adresse des requêtes au service et affiche les informations pertinentes des réponses dans la fenêtre de console.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Ouvrez la solution de l'exemple Basic Resource Service. Pour que l'exemple fonctionne correctement, vous devez exécuter [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] en tant qu'administrateur. Cela en double-cliquant sur le [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] icône et en sélectionnant **exécuter en tant qu’administrateur** dans le menu contextuel.  
  
2.  Appuyez sur CTRL+MAJ+B pour générer la solution, puis appuyez sur Ctrl+F5 pour exécuter l'application console. La fenêtre de console apparaît et fournit l'URI du service en cours d'exécution, ainsi que l'URI de sa page d'aide HTML. Vous pouvez à tout moment consulter la page d'aide HTML en tapant son URI dans un navigateur. Lorsque l'exemple s'exécute, le client écrit l'état de l'activité actuelle.  
  
3.  Appuyez sur une touche quelconque pour arrêter l'exemple.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Web\BasicResourceService`  
  
## <a name="see-also"></a>Voir aussi  
 [Service HTTP de base](../../../../docs/framework/wcf/samples/basic-http-service.md)  
 [Sélection automatique du format](../../../../docs/framework/wcf/samples/automatic-format-selection.md)
