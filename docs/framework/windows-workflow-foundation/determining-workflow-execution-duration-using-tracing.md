---
title: Détermination de la durée d'exécution d'un workflow à l'aide du suivi
ms.date: 03/30/2017
ms.assetid: f04ad0fd-edc7-4cbc-8979-356f2a1131c4
ms.openlocfilehash: c51fdf4543939fc068092b84e02eeb5f52e77d6d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43486279"
---
# <a name="determining-workflow-execution-duration-using-tracing"></a>Détermination de la durée d'exécution d'un workflow à l'aide du suivi
Cette rubrique montre comment déterminer le temps nécessaire à l'exécution avec succès d'un workflow auto-hébergé à l'aide du suivi de workflow.  
  
### <a name="to-determine-workflow-application-execution-duration-by-using-workflow-tracing"></a>Pour déterminer la durée d'exécution d'une application de workflow à l'aide du suivi  
  
1.  Ouvrez [!INCLUDE[vs2010](../../../includes/vs2010-md.md)].  Sélectionnez **fichier**, **nouveau**, **projet**.  Sous **c#**, sélectionnez le **Workflow** nœud.  Sélectionnez **Application Console de Workflow** à partir de la liste des modèles.  Nommez le nouveau projet `WorkflowDurationTracing` et cliquez sur **OK**.  
  
2.  Ouvrez le fichier Workflow1.xaml.  Faites glisser une activité <xref:System.Activities.Statements.Delay> sur l'aire du concepteur. Affectez la valeur 00:00:10 (dix secondes) à la propriété Duration de l'activité.  
  
3.  Ouvrez l’Observateur d’événements en cliquant sur **Démarrer**, **exécuter**et en entrant `eventvwr.exe`.  
  
4.  Si vous n’avez pas activé le suivi de workflow, développez **journaux des Applications et Services**, **Microsoft**, **Windows**, **serveur d’applications-Applications** . Sélectionnez **vue**, **afficher analytiques et les journaux de débogage**. Avec le bouton droit **déboguer** et sélectionnez **activer le journal**. Laissez l'Observateur d'événements ouvert afin que les traces soient visibles après l'exécution du workflow.  
  
5.  Exécutez l'application de workflow en appuyant sur Ctrl+Maj+B.  
  
6.  Dans l'Observateur d'événements, recherchez un événement récent portant l'ID 1009 et un message semblable au suivant. Notez l'heure à laquelle le message a été enregistré.  
  
 **Activité parente '', DisplayName : '', InstanceId : '' enfant planifiée activité 'WorkflowDurationTracking.Workflow1', DisplayName : 'Workflow1', InstanceId : '1'.**  
  
7.  Recherchez un autre événement récent portant l'ID 1001 et un message semblable au suivant.  Soustrayez l'heure du message précédent de la valeur enregistrée dans ce message pour déterminer la durée d'exécution du workflow, qui doit être d'environ dix secondes.  
  
 **WorkflowInstance Id : '1bbac57b-3322-498e-9e27-8833fda3a5bf' est terminée à l’état Closed.**  
  
## <a name="see-also"></a>Voir aussi  
 [Suivi de workflow](../../../docs/framework/windows-workflow-foundation/workflow-tracing.md)  
 [Surveillance de Windows Server App Fabric](https://go.microsoft.com/fwlink/?LinkId=201273)  
 [Surveillance des Applications avec App Fabric](https://go.microsoft.com/fwlink/?LinkId=201275)
