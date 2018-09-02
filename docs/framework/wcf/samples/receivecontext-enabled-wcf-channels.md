---
title: Canaux WCF prenant en charge ReceiveContext
ms.date: 03/30/2017
ms.assetid: d990d119-7321-4b8c-852b-10256f59f9b0
ms.openlocfilehash: d7f80d0874606129876fbf7dfa30c0327680b922
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43442744"
---
# <a name="receivecontext-enabled-wcf-channels"></a>Canaux WCF prenant en charge ReceiveContext
Cet exemple montre l'utilité de canaux WCF prenant en charge <xref:System.ServiceModel.Channels.ReceiveContext>. L'exemple implémente un service pour rechercher le produit de deux nombres à l'aide d'un canal NetMSMQ.  
  
 La classe <xref:System.ServiceModel.Channels.ReceiveContext> permet à une application de décider s'il faut accéder au message ou le laisser dans la file d'attente pour un traitement supplémentaire, même une fois le contenu du message inspecté. Dans cet exemple, un client envoie des entiers aléatoires à une file d'attente transactionnelle. Le service `ProductCalculator` reçoit les messages et en inspecte le contenu, en l'occurrence, des entiers, afin de déterminer si le produit peut être calculé. Si l'opération réalisée par le service ne calcule pas le produit, le message est remis en file d'attente et peut à nouveau être reçu par le service qui écoute la file d'attente.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer :  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant :  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\Net\MSMQ\ReceiveContextProductGenerator`  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Vérifiez que Microsoft Message Queuing (MSMQ) est installé.  
  
    1.  Pour installer MSMQ sur [!INCLUDE[lserver](../../../../includes/lserver-md.md)] :  
  
        1.  Dans **le Gestionnaire de serveur**, cliquez sur **fonctionnalités**.  
  
        2.  Dans le volet droit sous **résumé des fonctionnalités**, cliquez sur **ajouter des fonctionnalités**.  
  
        3.  Dans la fenêtre résultante, développez **Message Queuing**.  
  
        4.  Développez **Services de file d’attente de messages**.  
  
        5.  Cliquez sur **intégration de Services d’annuaire** (pour les ordinateurs joints à un domaine), puis cliquez sur **prise en charge HTTP**.  
  
        6.  Cliquez sur **suivant**, puis cliquez sur **installer**.  
  
    2.  Pour installer MSMQ sur [!INCLUDE[wv](../../../../includes/wv-md.md)] :  
  
        1.  Ouvrez le **Panneau de configuration**.  
  
        2.  Cliquez sur **programmes** puis, sous **programmes et fonctionnalités**, cliquez sur **activer et désactiver des fonctionnalités Windows**.  
  
        3.  Développez **Microsoft Message Queue Server (MSMQ)**, développez **Microsoft Message Queue (MSMQ) Server Core**, puis sélectionnez les cases à cocher pour les fonctionnalités suivantes de Message Queuing à installer :  
  
            -   Serveur Message Queuing  
  
            -   Intégration des services de domaine Active Directory MSMQ (pour les ordinateurs liés à un domaine).  
  
            -   Prise en charge HTTP MSMQ  
  
        4.  Cliquez sur **OK**.  
  
        5.  Si vous êtes invité à redémarrer l’ordinateur, cliquez sur **OK** pour terminer l’installation.  
  
2.  Assurez-vous que [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] est installé sur l'ordinateur.  
  
3.  À l'aide de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], ouvrez le fichier solution ReceiveContextProductGenerator.sln.  
  
4.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
5.  Pour exécuter la solution, appuyez sur Ctrl+F5.
