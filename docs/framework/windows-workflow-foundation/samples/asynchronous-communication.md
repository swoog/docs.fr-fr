---
title: Communication asynchrone
ms.date: 03/30/2017
ms.assetid: 128dc092-9eb2-4e33-9470-9a7f62b60df6
ms.openlocfilehash: 9eafeab89aefb181ae016dc0219f9155d9bd2a25
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33515158"
---
# <a name="asynchronous-communication"></a>Communication asynchrone
Cet exemple montre comment la communication entre deux services Windows Workflow Foundation (WF) s’effectue de façon asynchrone par défaut.  
  
## <a name="demonstrates"></a>Démonstrations  
 Communication asynchrone entre des services [!INCLUDE[wf1](../../../../includes/wf1-md.md)].  
  
## <a name="discussion"></a>Discussion  
 Cet exemple montre comment la communication entre des applications [!INCLUDE[wf1](../../../../includes/wf1-md.md)] s'effectue de façon asynchrone à l'aide des activités de messagerie fournies par le .NET Framework.  
  
 Cet exemple est composé des trois projets suivants :  
  
 CreditCheckService  
 Ce service reçoit le niveau de crédit d'une personne particulière ou la valeur de l'élément à acquérir, puis décide si le crédit est accordé à la personne.  
  
 RentalApprovalService  
 Ce service reçoit une application d'une personne qui a besoin d'un crédit. Il communique de façon asynchrone avec `CreditCheckService` pour décider si l'application de crédit est valide.  
  
 Client  
 Le client communique de façon synchrone avec `RentalApprovalService` pour savoir si le crédit est approuvé.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Cliquez sur le **AsynchronousCommunication** solution et sélectionnez **propriétés**.  
  
2.  Dans **propriétés communes**, sélectionnez **projet de démarrage**, puis sélectionnez **plusieurs projets de démarrage**.  
  
3.  Déplacer **RentalApprovalService** pour la première position dans la liste, suivi de **CreditCheckService**, suivi par **Client**. Définir le **Démarrer** action sur toutes les trois projets.  
  
4.  Cliquez sur **OK**, appuyez sur F5 pour exécuter l’exemple.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\Services\AsynchronousCommunication`
