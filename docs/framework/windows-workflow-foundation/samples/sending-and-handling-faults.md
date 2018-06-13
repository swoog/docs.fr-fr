---
title: Envoi et gestion des erreurs
ms.date: 03/30/2017
ms.assetid: 98e8e04d-2ac9-4a33-ae08-462f757a7a14
ms.openlocfilehash: 6796b4daccd88adc3bd006f454ce96ca155fbcb3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33516124"
---
# <a name="sending-and-handling-faults"></a>Envoi et gestion des erreurs
Cet exemple montre comment utiliser les activités de messagerie <xref:System.ServiceModel.Activities.SendReply> et <xref:System.ServiceModel.Activities.ReceiveReply> pour envoyer et recevoir des erreurs attendues et inattendues. Dans ce scénario, la première demande du client génère une erreur attendue qui a été incluse dans sa collection <xref:System.ServiceModel.Activities.Send.KnownTypes%2A>. Les demandes suivantes du client entrainent la réception d'erreurs inattendues, avant que la dernière demande réussisse.  
  
## <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Ouvrez [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] avec des autorisations élevées, en cliquant sur le [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] icône et en sélectionnant **exécuter en tant qu’administrateur**.  
  
2.  Ouvrez le fichier solution Faults.sln.  
  
3.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
4.  Exécutez le projet de service.  
  
    1.  Dans **l’Explorateur de solutions**, avec le bouton droit le `FaultService` de projet et sélectionnez **définir comme projet de démarrage**.  
  
    2.  Appuyez sur CTRL+F5.  
  
5.  Ouvrir une autre copie de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] avec des autorisations élevées, en cliquant sur le [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] icône et en sélectionnant **exécuter en tant qu’administrateur**.  
  
6.  Ouvrez le fichier solution Faults.sln.  
  
7.  Exécutez le projet client.  
  
    1.  Dans **l’Explorateur de solutions**, avec le bouton droit le `FaultClient` de projet et sélectionnez **définir comme projet de démarrage**.  
  
    2.  Appuyez sur CTRL+F5.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\Faults`