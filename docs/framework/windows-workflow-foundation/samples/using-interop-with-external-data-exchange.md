---
title: Utilisation d'Interop avec l'échange interne de données
ms.date: 03/30/2017
ms.assetid: 96f6fe26-5305-494f-9119-7748e0c4b3fa
ms.openlocfilehash: 534321e5b5568e0dd0988333dc98ccc18ff33df8
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45520384"
---
# <a name="using-interop-with-external-data-exchange"></a>Utilisation d'Interop avec l'échange interne de données
Le <xref:System.Activities.Statements.Interop> activité peut être utilisée pour exécuter des activités à partir de Windows Workflow Foundation (WF) dans [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)] et [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)] (WF3) et des flux de travail dans Windows Workflow Foundation dans [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] (WF4). Cet exemple montre comment configurer et exécuter un workflow WF3 qui utilise <xref:System.Workflow.Activities.ExternalDataExchangeService> (et les activités personnalisées correspondantes pour appeler les méthodes et gérer les événements) à l'aide de l'activité <xref:System.Activities.Statements.Interop> dans un service de workflow WF4.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Migration\ExternalDataExchange`  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Ouvrez le fichier ExternalDataExchange.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Pour créer l'exemple, appuyez sur Ctrl+Maj+B.  
  
3.  Pour exécuter l'exemple, appuyez sur F5.
