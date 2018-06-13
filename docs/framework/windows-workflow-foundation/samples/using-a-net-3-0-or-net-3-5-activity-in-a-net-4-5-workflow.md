---
title: Utilisation d'une activité .NET Framework 3.0 ou .NET Framework 3.5 dans un Workflow .NET Framework 4.5
ms.date: 03/30/2017
ms.assetid: 6c53fd4c-5dd0-4fb4-ab6b-111302629548
ms.openlocfilehash: ab2e93918617bd1ca21fb32878d446db0dd2ef16
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33514897"
---
# <a name="using-a-net-framework-30-or-net-framework-35-activity-in-a-net-framework-45-workflow"></a>Utilisation d'une activité .NET Framework 3.0 ou .NET Framework 3.5 dans un Workflow .NET Framework 4.5
Le <xref:System.Activities.Statements.Interop> activité vous permet d’exécuter une activité .NET Framework 3.0 Windows Workflow Foundation (WF) dans un [!INCLUDE[netfx_current_short](../../../../includes/netfx-current-short-md.md)] flux de travail. Cet exemple montre comment utiliser l'activité <xref:System.Activities.Statements.Interop> pour passer une chaîne en tant qu'argument à une activité [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)] personnalisée.  
  
## <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  À l'aide de [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], ouvrez le fichier solution SimpleInterop.sln.  
  
2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
3.  Pour exécuter la solution, appuyez sur Ctrl+F5.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Migration\SimpleInterop`  
  
## <a name="see-also"></a>Voir aussi
