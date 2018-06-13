---
title: Calculatrice corrélée
ms.date: 03/30/2017
ms.assetid: c365166e-6552-49a4-bf17-9f4e597d4d41
ms.openlocfilehash: 77e13b3ca913d2432cfe5d4a95e83764effbb109
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33514139"
---
# <a name="correlated-calculator"></a>Calculatrice corrélée
Cet exemple montre comment utiliser les activités de messagerie (<xref:System.ServiceModel.Activities.Receive> et <xref:System.ServiceModel.Activities.SendReply>) dans le concepteur avec une corrélation basée sur le contenu selon un paramètre dans le message. Dans ce scénario, les opérations de la calculatrice sont dans un convoi parallèle. Une instance et une corrélation (selon `CalculatorId`) sont toutes deux créées lorsque le premier message est envoyé au workflow et les messages suivants avec le même `CalculatorId` sont distribués à cette instance jusqu'à l'appel de l'opération de réinitialisation. Le client est implémenté comme une application WPF qui utilise un proxy client basé sur du code pour communiquer avec le service.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Démarrez [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] avec des autorisations élevées, ouvrez le fichier solution For.sln.  
  
    1.  Naviguez jusqu'au dossier qui contient [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
    2.  Cliquez sur Devenv.exe et sélectionnez **exécuter en tant qu’administrateur**.  
  
2.  À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution CorrelatedCalculator.sln.  
  
3.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
4.  Pour exécuter le projet de service, appuyez sur CTRL+F5.  
  
5.  Une fois que le service est prêt et qu'il écoute les messages, dans l'Explorateur de solutions, cliquez avec le bouton droit sur le projet Client et exécutez-le.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\Services\CorellatedCalculator`