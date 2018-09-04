---
title: Exposition et appel d'ActivityActions
ms.date: 03/30/2017
ms.assetid: 97ce4797-426e-463d-9cc4-1261afad6df4
ms.openlocfilehash: f36d88fc54e5150927113ed8825fbccad84129d4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43520121"
---
# <a name="exposing-and-invoking-activityactions"></a>Exposition et appel d'ActivityActions
Cet exemple montre comment développer une activité personnalisée qui a un <xref:System.Activities.ActivityAction>. Il montre également comment utiliser cette activité en fournissant une implémentation d'<xref:System.Activities.ActivityAction>.  
  
 Un <xref:System.Activities.ActivityAction> permet à un auteur d’activité exposer des « trous » avec des signatures spécifiques où l’utilisateur de l’activité peut incorporer un comportement personnalisé. Par exemple, le <!--zz <xref:System.Activities.Statements.ForEach>--> `System.Activities.Statements.ForEach` activité, (qui fonctionne sur une collection d’éléments), a un <xref:System.Activities.ActivityAction> qui permet à l’utilisateur de l’activité incorporer un comportement qui fonctionne sur l’élément d’itération actuel.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Ouvrez le **ActivityAction.sln** exemple de solution dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Générez et exécutez la solution.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Code-Bodied\ActivityAction`