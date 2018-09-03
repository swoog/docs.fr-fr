---
title: Utilisation de TransactedReceiveScope
ms.date: 03/30/2017
ms.assetid: d455f1dc-bfc5-43d6-8ae9-bc3b3a3ea08a
ms.openlocfilehash: bc1c418f3fa116f5e1c1647af3543a38122842f5
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43481469"
---
# <a name="use-of-transactedreceivescope"></a>Utilisation de TransactedReceiveScope
Cet exemple montre comment passer une transaction d'un client à un serveur à l'aide de <xref:System.Activities.Statements.TransactionScope> pour créer une transaction sur le client et un <xref:System.ServiceModel.Activities.TransactedReceiveScope> pour recevoir un message avec une transaction passée et mesurer l'étendue de la durée de vie de la transaction sur le serveur. Cet exemple est composé deux projets qui jouent les rôles de client et serveur.  
  
## <a name="client-application"></a>Application cliente  
 L'application cliente exécute un workflow qui imprime l'ID de transaction distribuée, envoie un message au serveur, passe la transaction, reçoit la réponse, imprime à nouveau l'ID de transaction distribuée et se termine. Lorsque l'ID de transaction distribuée est initialement imprimé, il s'agit d'un GUID vide, car la transaction est encore uniquement locale.  
  
## <a name="server-application"></a>Application serveur  
 Le projet serveur est semblable ; toutefois, le workflow est hébergé dans <xref:System.ServiceModel.Activities.WorkflowServiceHost> parce qu'il doit écouter le message du client sur un point de terminaison. Le workflow est centré sur le <xref:System.ServiceModel.Activities.TransactedReceiveScope>, qui reçoit la transaction passée du client, imprime le message envoyé, imprime l'ID de transaction distribuée et envoie la réponse au client. L'ID de transaction distribuée est maintenant un GUID non vide et, si une activité prenant en charge les transactions a été ajoutée au corps du <xref:System.ServiceModel.Activities.TransactedReceiveScope>, elle s'exécute sous la transaction passée.  
  
#### <a name="to-run-the-sample"></a>Pour exécuter l'exemple  
  
1.  Ouvrez la solution TransactedReceiveScope.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Pour générer la solution, appuyez sur CTRL + MAJ + B ou sélectionnez **générer la Solution** à partir de la **Build** menu.  
  
3.  Une fois la génération a réussi, cliquez sur la solution et sélectionnez **définir les projets de démarrage**. Dans la boîte de dialogue, sélectionnez **plusieurs projets de démarrage** et vérifiez que l’action pour les deux projets est **Démarrer**.  
  
4.  Appuyez sur F5 ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu. Ou bien, vous pouvez appuyer sur CTRL + F5 ou sélectionnez **démarrer sans débogage** à partir de la **déboguer** menu afin d’exécuter sans débogage.  
  
    > [!NOTE]
    >  Le serveur doit être en cours d'exécution avant de démarrer le client. La sortie de la fenêtre de console qui héberge le service indique le moment où il a démarré.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Transactions\TransactedReceiveScope`