---
title: Imbrication de TransactionScope dans un service
ms.date: 03/30/2017
ms.assetid: e7e1ba64-1384-4eba-add8-415636e2d6d0
ms.openlocfilehash: cf73c0c2d061f1c997a8ade5d7b2bf61887915ca
ms.sourcegitcommit: ba5c189bf44d44204a3e8838e59ec378a62d82f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44700022"
---
# <a name="nesting-of-transactionscope-within-a-service"></a>Imbrication de TransactionScope dans un service
Cet exemple se compose de deux scénarios qui s'exécutent, en montrant comment gérer des instances d'activité <xref:System.Activities.Statements.TransactionScope> dans un service. En premier lieu, la transaction est initiée à l'aide de l'activité <xref:System.Activities.Statements.TransactionScope> pour créer une transaction sur le client et <xref:System.ServiceModel.Activities.TransactedReceiveScope> pour recevoir et mesurer l'étendue de la durée de vie de la transaction sur le serveur. Le premier scénario dans le service exécute une activité <xref:System.Activities.Statements.TransactionScope> secondaire pour illustrer l'imbrication des activités <xref:System.Activities.Statements.TransactionScope> dans le service. Le deuxième scénario montre comment les délais d'expiration sont respectés dans les activités <xref:System.Activities.Statements.TransactionScope> imbriquées.  
  
## <a name="client-application"></a>Application cliente  
 L'application cliente exécute un workflow qui démarre une activité <xref:System.Activities.Statements.TransactionScope>, imprime l'ID de transaction distribuée, envoie un message au serveur, passe la transaction, reçoit la réponse, imprime à nouveau l'ID de transaction distribuée et se termine. Cette opération est effectuée une fois pour chaque scénario de service.  
  
## <a name="server-application"></a>Application serveur  
 Le projet serveur est hébergé dans <xref:System.ServiceModel.Activities.WorkflowServiceHost>, ce qui crée le point de terminaison sur lequel écouter le message du client. Le workflow est centré sur le <xref:System.ServiceModel.Activities.TransactedReceiveScope>, qui reçoit la transaction passée du client, imprime l'ID de transaction distribuée, puis exécute une deuxième activité <xref:System.Activities.Statements.TransactionScope>. Dans le premier scénario, la transaction est effectuée avec succès. Dans le deuxième scénario, le corps de l'activité <xref:System.Activities.Statements.TransactionScope> est un délai de cinq secondes et le délai d'expiration de la transaction est défini à deux secondes. Lorsque la transaction expire, elle est abandonnée.  
  
#### <a name="to-run-the-sample"></a>Pour exécuter l'exemple  
  
1.  Ouvrez la solution TransactionServiceExample.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Pour générer la solution, appuyez sur CTRL + MAJ + B ou sélectionnez **générer la Solution** à partir de la **Build** menu.  
  
3.  Une fois la génération a réussi, cliquez sur la solution et sélectionnez **définir les projets de démarrage**. Dans la boîte de dialogue, sélectionnez **plusieurs projets de démarrage** et vérifiez que l’action pour les deux projets est **Démarrer**.  
  
4.  Appuyez sur F5 ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu. Ou bien, vous pouvez appuyer sur CTRL + F5 ou sélectionnez **démarrer sans débogage** à partir de la **déboguer** menu afin d’exécuter sans débogage.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Transactions\TRSComposability`
