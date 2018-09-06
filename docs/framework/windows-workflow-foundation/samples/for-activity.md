---
title: Activité For
ms.date: 03/30/2017
ms.assetid: 2ea751b4-36f0-48aa-a115-70a2ab89f6d8
ms.openlocfilehash: 7a7023abb9057ab4b25552fbf9a81cd2ae2b4e88
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43881519"
---
# <a name="for-activity"></a>Activité For
L'exemple For montre comment générer une activité personnalisée qui hérite de <xref:System.Activities.NativeActivity>, et l'utiliser dans un workflow pour exécuter un exemple réel. L'activité personnalisée incluse dans cet exemple fonctionne comme l'instruction C# `for`. T  
  
 L'activité personnalisée `For` a des propriétés nommées `InitAction`, `IterationAction`, `Condition` et `Body` qui correspondent respectivement à l'instruction d'initialisation, à l'instruction itérative, à la condition de continuation et à l'instruction du corps se trouvant dans la instruction standard C# `For`.  
  
 Le tableau suivant décrit les fichiers de clés de l'exemple.  
  
|Fichier|Description|  
|----------|-----------------|  
|For.cs|Définition de classe pour l'activité personnalisée `For`, qui étend la classe <xref:System.Activities.NativeActivity> pour fournir les fonctionnalités de l'instruction C# `For`.|  
|Program.cs|Application cliente qui effectue le travail itératif de base sur une collection à l'aide de l'activité `For` personnalisée.|  
  
> [!NOTE]
>  Lorsque vous utilisez l'activité personnalisée `For`, vérifiez que la propriété `Condition` est définie ; sinon, une boucle infinie pourrait se produire.  
  
## <a name="demonstrates"></a>Démonstrations  
 Créez une activité personnalisée qui hérite de l'activité <xref:System.Activities.NativeActivity>.  
  
## <a name="discussion"></a>Discussion  
 Le tableau suivant décrit les propriétés de l'activité incluse dans cet exemple.  
  
 InitAction  
 Instruction d'initialisation  
  
 IterationAction  
 Instruction itérative  
  
 Condition  
 Instruction de continuation  
  
 Corps  
 Instruction du corps  
  
 L'activité hérite de <xref:System.Activities.NativeActivity> pour accéder à des fonctionnalités de runtime telles que la planification de l'exécution d'activités supplémentaires, à l'aide de l'une des méthodes `ScheduleActivity` de <xref:System.Activities.NativeActivityContext>.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution For.sln.  
  
2.  Générez la solution en appuyant sur Ctrl+Maj+B.  
  
3.  Exécutez la solution en appuyant sur F5.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\For`