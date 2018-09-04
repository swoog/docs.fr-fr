---
title: Mise en cache des canaux avec Send
ms.date: 03/30/2017
ms.assetid: e69a2502-25cb-43bf-b8d2-95fbdecb41cb
ms.openlocfilehash: 619088def1f5e443a31244516655d75d1e25c9cb
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43503813"
---
# <a name="channel-caching-with-send"></a>Mise en cache des canaux avec Send
Le <xref:System.ServiceModel.Activities.SendMessageChannelCache> permet aux utilisateurs d'avoir différents niveaux de mise en cache des canaux avec les activités <xref:System.ServiceModel.Activities.Send> et <xref:System.ServiceModel.Activities.SendParametersContent>. La mise en cache au niveau de l'instance est activée par défaut et cet exemple illustre les fonctionnalités suivantes :  
  
1.  Partager un <xref:System.ServiceModel.Activities.SendMessageChannelCache> dans un domaine d'application.  
  
2.  Désactiver la mise en cache des canaux.  
  
3.  Partager un <xref:System.ServiceModel.Activities.SendMessageChannelCache> entre des instances de workflow dans un <xref:System.ServiceModel.Activities.WorkflowServiceHost>.  
  
## <a name="demonstrates"></a>Démonstrations  
 Extension <xref:System.ServiceModel.Activities.SendMessageChannelCache>, activités <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.ReceiveContent> et <xref:System.ServiceModel.Activities.SendReply>.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Chargez la solution du projet dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] et générez le projet.  
  
2.  Exécutez l'application EchoWorkflowService générée dans \EchoWorkflowService\bin\debug.  
  
3.  Exécutez l'application EchoWorkflowClient générée dans .\EchoWorkflowClient\bin\debug.  
  
4.  Le client appelle l'opération Echo sur le service et imprime les résultats. Lorsque les résultats ont été imprimés, appuyez sur ENTRÉE pour quitter le client et le service.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\ChannelCache`
