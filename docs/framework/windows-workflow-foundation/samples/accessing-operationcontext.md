---
title: Accès à OperationContext
ms.date: 03/30/2017
ms.assetid: 4e92efe8-7e79-41f3-b50e-bdc38b9f41f8
ms.openlocfilehash: cefbc3b10114b427518e640809462eedb131d695
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="accessing-operationcontext"></a>Accès à OperationContext
Cet exemple montre comment les activités de messagerie (<xref:System.ServiceModel.Activities.Receive> et <xref:System.ServiceModel.Activities.Send>) peut être utilisé avec une activité d’étendue personnalisée pour accéder à <xref:System.ServiceModel.OperationContext.Current%2A> et attacher ou récupérer un en-tête de message personnalisé dans un message sortant ou entrant.  
  
## <a name="demonstrates"></a>Démonstrations  
 Activités de messagerie, <xref:System.ServiceModel.Activities.ISendMessageCallback>, <xref:System.ServiceModel.Activities.IReceiveMessageCallback>.  
  
## <a name="discussion"></a>Discussion  
 Cet exemple montre comment utiliser des points d'extensibilité (<xref:System.ServiceModel.Activities.ISendMessageCallback>, <xref:System.ServiceModel.Activities.IReceiveMessageCallback>) dans les activités de messagerie pour accéder à <xref:System.ServiceModel.OperationContext.Current%2A>. Les rappels sont inscrits dans le runtime du workflow sous la forme d'une implémentation d'<xref:System.Activities.IExecutionProperty> qui est choisie par les activités de messagerie lors de l'exécution. Toute activité de messagerie de la même étendue que cette implémentation <xref:System.Activities.IExecutionProperty> est affectée. Plus particulièrement, cet exemple utilise une activité d'étendue personnalisée pour appliquer le comportement de rappel. <xref:System.ServiceModel.Activities.ISendMessageCallback> est utilisé dans le workflow client pour inclure l'<xref:System.Activities.WorkflowApplication.Id%2A> du workflow en tant que <xref:System.ServiceModel.Channels.MessageHeader> sortant. Cet en-tête est ensuite choisi dans le service à l'aide d'<xref:System.ServiceModel.Activities.IReceiveMessageCallback> et la valeur de l'en-tête est imprimée sur la console.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Cet exemple expose un service de workflow à l'aide de points de terminaison HTTP. Pour exécuter cet exemple, bon ACL d’URL doit être ajouté (consultez [configuration de HTTP et HTTPS](http://go.microsoft.com/fwlink/?LinkId=70353) pour plus d’informations), soit en exécutant Visual Studio en tant qu’administrateur ou en exécutant la commande suivante à une invite de commandes avec élévation de privilèges pour ajouter les ACL appropriées. Vérifiez que vos domaine et nom d'utilisateur sont substitués.  
  
    ```  
    netsh http add urlacl url=http://+:8000/ user=%DOMAIN%\%UserName%  
    ```  
  
2.  Une fois les listes de contrôle d'accès (ACL) d'URL ajoutées, effectuez les étapes suivantes.  
  
    1.  Générez la solution.  
  
    2.  Définir plusieurs projets de démarrage en cliquant sur la solution et en sélectionnant **définir les projets de démarrage**.  
  
    3.  Ajouter **Service** et **Client** (dans cet ordre) en tant que plusieurs projets de démarrage.  
  
    4.  Exécutez l'application. La console cliente affiche un workflow qui est exécuté deux fois et la fenêtre Service affiche l'ID d'instance de ces workflows.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\Services\Accessing Operation Context`
