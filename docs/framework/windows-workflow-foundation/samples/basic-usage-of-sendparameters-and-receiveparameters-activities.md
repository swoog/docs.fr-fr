---
title: Utilisation de base des activités SendParameters et ReceiveParameters
ms.date: 03/30/2017
ms.assetid: 1b6b1681-3d41-403f-bfe2-3f600f24aa8c
ms.openlocfilehash: c13999ad1571a6413e30e801b6c642000f8e4654
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43467693"
---
# <a name="basic-usage-of-sendparameters-and-receiveparameters-activities"></a>Utilisation de base des activités SendParameters et ReceiveParameters
Cet exemple illustre l'utilisation des activités <xref:System.ServiceModel.Activities.SendParametersContent> et <xref:System.ServiceModel.Activities.ReceiveParametersContent>. Le service expose une opération qui accepte un argument de type chaîne et retourne l'entrée au client. L'exemple montre comment configurer les paramètres pour ces activités de messagerie.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\SendReceiveParameters`  
  
#### <a name="using-this-sample"></a>Utilisation de cet exemple  
  
1.  Chargez la solution du projet dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] et générez le projet.  
  
2.  En premier lieu, exécutez l'application EchoWorkflowService, générée dans [répertoire de base de la solution]\EchoWorkflowService\bin\debug.  
  
3.  En second lieu, exécutez l'application EchoWorkflowClient, générée dans [répertoire de base de la solution]\EchoWorkflowClient\bin\debug.  
  
4.  Le client appelle l'opération Echo sur le service et imprime les résultats. Une fois cette opération terminée, appuyez sur ENTRÉE pour quitter le client, puis le service.