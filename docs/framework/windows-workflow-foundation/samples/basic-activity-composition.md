---
title: Composition de l'activité de base
ms.date: 03/30/2017
ms.assetid: c283a1a7-1245-4ecd-8072-206c1b4ca379
ms.openlocfilehash: ade8187ca44a8182b55cf0f01e5bfe5a9a747255
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43518374"
---
# <a name="basic-activity-composition"></a>Composition de l'activité de base
Cet exemple montre comment composer des activités personnalisées et des activités fournies par le système pour générer d'autres activités personnalisées.  
  
 Le workflow, à l'aide de l'activité Survey, planifie l'enquête avec une liste de questions, puis fournit en sortie les réponses reçues.  
  
## <a name="sample-details"></a>Détails de l'exemple  
 Cet exemple utilise trois activités personnalisées. `ReadLine` est une simple <xref:System.Activities.NativeActivity> \<chaîne > qui crée un <xref:System.Activities.Bookmark> lorsque planifiée, puis affecte la `Return` <xref:System.Activities.OutArgument%601> à la valeur avec laquelle le <xref:System.Activities.Bookmark> est repris. `Prompt` est un <xref:System.Activities.Activity%601> \<string > qui prend un <xref:System.Activities.InArgument%601>< chaîne\> nommé `Text` et retourne les utilisateurs réponse dans le `Result` <xref:System.Activities.OutArgument%601> \<chaîne >. L'activité `Prompt` utilise les activités <xref:System.Activities.Statements.Sequence> et <xref:System.Activities.Statements.WriteLine> fournies dans le cadre du .NET Framework, et incorpore également l'activité `ReadLine` personnalisée pour l'obtention de l'entrée d'utilisateur. La dernière activité personnalisée est l'activité `Survey`. Il s’agit une <xref:System.Activities.Activity>< ICollection\<chaîne >>.  Cette activité prend une <xref:System.Activities.InArgument%601>< IEnumerable < chaîne\>> nommé `Questions` et remplit la `Result` out argument avec les réponses. L'activité `Survey` utilise <xref:System.Activities.Statements.ForEach%601>, <xref:System.Activities.Statements.Sequence> et <xref:System.Activities.Statements.AddToCollection%601> du .NET Framework et emploie l'activité `Prompt` pour poser les questions de l'enquête et obtenir des réponses.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  Ouvrez le **BasicActivityComposition.sln** exemple de solution dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Générez et exécutez la solution.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Composite\ActivityComposition`