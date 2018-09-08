---
title: Exemple de point de terminaison de gestion de workflow
ms.date: 03/30/2017
ms.assetid: 3ac6e08f-c43d-4bb7-83c3-e3890a4dac03
ms.openlocfilehash: 3d99cbef20895381f5e40ee939e1d94a409f1391
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44130511"
---
# <a name="workflow-management-endpoint-sample"></a>Exemple de point de terminaison de gestion de workflow
Cet exemple montre comment un point de terminaison de contrôle de workflow peut être utilisé pour créer et exécuter des workflows à la fois localement et à distance. Il montre comment héberger un point de terminaison de contrôle et écrire des clients qui appellent le point de terminaison de contrôle pour créer et exécuter l'instance d'un workflow. Le workflow n'est pas un service.  
  
 Du côté service de l'exemple ,un workflow est hébergé avec WorkflowServiceHost et un WorkflowControlEndpoint est ajouté afin que les clients puissent exécuter des opérations de contrôle (Suspendre, Démarrer, etc.). Un CreationEndpoint défini par l'utilisateur est également ajouté pour permettre la création du workflow. Le service utilise ensuite ces points de terminaison pour démarrer le workflow dans un état suspendu, puis pour reprendre le workflow. Le client exécute les mêmes opérations mais à partir du code client. Pour plus d’informations sur ces interfaces, consultez [point de terminaison de contrôle de flux de travail](../../../../docs/framework/wcf/feature-details/workflow-control-endpoint.md) et [Comment : héberger un workflow sans service dans IIS](../../../../docs/framework/wcf/feature-details/how-to-host-a-non-service-workflow-in-iis.md)  
  
#### <a name="to-run-the-sample"></a>Pour exécuter l'exemple  
  
1.  Exécutez [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] avec des privilèges d'administrateur.  
  
2.  Ouvrez la solution ManagementEndpoint.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
3.  Pour générer la solution, appuyez sur CTRL + MAJ + B ou sélectionnez **générer la Solution** à partir de la **Build** menu.  
  
4.  Démarrez l'application ManagementEndpoint.exe.  
  
5.  Démarrez l'application Client.exe.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\ManagementEndpoint`