---
title: Gestion de l'instance interrompue
ms.date: 03/30/2017
ms.assetid: f5ca3faa-ba1f-4857-b92c-d927e4b29598
ms.openlocfilehash: f614770121185644c3395f923cf7835141653f55
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43394598"
---
# <a name="suspended-instance-management"></a>Gestion de l'instance interrompue
Cet exemple montre comment gérer des instances de workflow qui ont été interrompues.  L'action par défaut pour <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> est `AbandonAndSuspend`. Cela signifie que, par défaut, les exceptions non gérées levées à partir d'une instance de workflow hébergée dans le <xref:System.ServiceModel.WorkflowServiceHost> provoqueront la suppression de l'instance de la mémoire (abandon), et la version durable/persistante de l'instance sera marquée comme interrompue. Une instance de workflow interrompue ne sera pas en mesure de fonctionner tant que l'interruption n'a pas été annulée.  
  
 L'exemple montre comment un utilitaire en ligne de commande peut être implémenté pour rechercher des instances interrompues et comment permettre à l'utilisateur de reprendre ou de terminer l'instance. Dans cet exemple, un service de workflow lève une exception intentionnellement, ce qui provoque son interruption. L'utilitaire en ligne de command peut ensuite être utilisé pour rechercher l'instance et, par la suite, la reprendre ou la terminer.  
  
## <a name="demonstrates"></a>Démonstrations  
 <xref:System.ServiceModel.WorkflowServiceHost> avec <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior> et <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> dans Windows Workflow Foundation (WF).  
  
## <a name="discussion"></a>Discussion  
 L'utilitaire en ligne de commande implémenté dans cet exemple est spécifique à l'implémentation du magasin d'instances SQL fournie dans [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)]. Si vous avez une implémentation personnalisée du magasin d'instances, vous pouvez adapter cet utilitaire en remplaçant les implémentations `WorkflowInstanceCommand` dans l'exemple par des implémentations qui sont spécifiques à votre magasin d'instances.  
  
 L'implémentation fournie exécute directement des commandes SQL dans le magasin d'instances SQL pour répertorier les instances interrompues et s'appuie sur un <xref:System.ServiceModel.Activities.WorkflowControlEndpoint> ajouté au <xref:System.ServiceModel.WorkflowServiceHost> pour reprendre ou terminer les instances.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Cet exemple requiert que les composants Windows suivants soient activés :  
  
    1.  Serveur de file d'attente Microsoft Message Queue (MSMQ)  
  
    2.  SQL Server Express  
  
2.  Configurez la base de données SQL Server.  
  
    1.  À partir d’un [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] invite de commandes, exécutez « setup.cmd » à partir de l’exemple suspendedinstancemanagement, qui effectue les opérations suivantes :  
  
        1.  Crée une base de données de persistance à l'aide de SQL Server Express. Si la base de données de persistance existe déjà, elle est supprimée et recréée.  
  
        2.  Configure la base de données pour la persistance.  
  
        3.  Ajoute IIS APPPOOL\DefaultAppPool et NT AUTHORITY\Network Service au rôle InstanceStoreUsers qui a été défini lors de la configuration de la base de données pour la persistance.  
  
3.  Configurez la file d'attente de service.  
  
    1.  Dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], cliquez sur le **SampleWorkflowApp** projet puis cliquez sur **définir comme projet de démarrage**.  
  
    2.  Compilez et exécutez SampleWorkflowApp en appuyant sur **F5**. La file d'attente requise sera ainsi créée.  
  
    3.  Appuyez sur **entrée** pour arrêter SampleWorkflowApp.  
  
    4.  Ouvrez la console Gestion de l'ordinateur en exécutant Compmgmt.msc à partir d'une invite de commandes.  
  
    5.  Développez **Service et les Applications**, **Message Queuing**, **files d’attente privées**.  
  
    6.  Bouton droit sur le **ReceiveTx** de file d’attente et sélectionnez **propriétés**.  
  
    7.  Sélectionnez le **sécurité** onglet et autoriser **tout le monde** disposer d’autorisations à **recevoir un Message**, **lire le Message**, et  **Envoyer le Message**.  
  
4.  Exécutez maintenant l'exemple.  
  
    1.  Dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], réexécutez le projet SampleWorkflowApp sans déboguer en appuyant sur **Ctrl + F5**. Deux adresses de point de terminaison seront imprimées dans la fenêtre de console : une pour le point de terminaison d'application et l'autre pour le <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>. Une instance de workflow est ensuite créée et les enregistrements de suivi pour cette instance s'afficheront dans la fenêtre de console. L'instance de workflow lèvera une exception qui provoquera l'interruption et l'abandon de l'instance.  
  
    2.  L'utilitaire en ligne de commande peut ensuite être utilisé pour entreprendre des actions supplémentaires sur chacune de ces instances. La syntaxe pour les arguments de ligne de commande est la suivante :  
  
         `SuspendedInstanceManagement -Command:[CommandName] -Server:[ServerName] -Database:[DatabaseName] -InstanceId:[InstanceId]`  
  
         Les commandes prises en charge sont `Query`, `Resume` et `Terminate`.  Le commutateur InstanceId est uniquement obligatoire pour les opérations `Resume` et `Terminate`.  
  
#### <a name="to-cleanup-optional"></a>Pour effectuer un nettoyage (facultatif)  
  
1.  Ouvrez la console Gestion de l'ordinateur en exécutant Compmgmt.msc à partir d'une invite de commandes `vs2010`.  
  
2.  Développez **Service et les Applications**, **Message Queuing**, **files d’attente privées**.  
  
3.  Supprimer le **ReceiveTx** file d’attente.  
  
4.  Pour supprimer la base de données de persistance, exécutez cleanup.cmd.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Application\SuspendedInstanceManagement`
