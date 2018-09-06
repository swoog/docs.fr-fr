---
title: Utilisation de CancellationScope
ms.date: 03/30/2017
ms.assetid: 39c5c338-b316-43d6-b7fe-a543281dd1ec
ms.openlocfilehash: 82d44fff869f207c09dc7685fc3470630e001a59
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44035763"
---
# <a name="using-cancellationscope"></a>Utilisation de CancellationScope
Cet exemple montre comment utiliser l'activité <xref:System.Activities.Statements.CancellationScope> pour annuler un travail dans une application.  
  
 De nombreux composants et services de niveau intermédiaire comptent sur la construction de programmation connue des transactions pour gérer l'annulation pour eux.  Toutefois, dans un certain nombre de cas, le travail qui ne peut pas être fait dans une transaction doit être annulé.  Il est plus difficile d'utiliser l'annulation que d'utiliser des transactions, car le travail qui doit être annulé doit être d'abord suivi. [!INCLUDE[netfx_current_short](../../../../includes/netfx-current-short-md.md)] vous aide en fournissant une activité <xref:System.Activities.Statements.CancellationScope>.  
  
 L'annulation peut être déclenchée à partir d'une activité ou à partir du parent de l'activité.  Les activités enfants sont planifiées par leur activité parente (telles qu'un <xref:System.Activities.Statements.Sequence>, un <xref:System.Activities.Statements.Parallel>, un <xref:System.Activities.Statements.Flowchart> ou une activité composite personnalisée).  L'activité parente peut annuler des activités enfants pour n'importe quelle raison.  Par exemple, une activité <xref:System.Activities.Statements.Parallel> avec trois branches enfants annule les branches enfants restantes chaque fois qu'elle termine une branche et que l'expression <xref:System.Activities.Statements.Parallel.CompletionCondition%2A> prend la valeur `true`. Le workflow peut également être annulé de manière externe par l'application hôte en appelant <xref:System.Activities.WorkflowApplication.Cancel%2A>.  
  
 Pour utiliser l'activité <xref:System.Activities.Statements.CancellationScope>, placez le travail qui doit être annulé dans la propriété <xref:System.Activities.Statements.CancellationScope.Body%2A>, et placez le travail qui est effectué après l'annulation dans la propriété <xref:System.Activities.Statements.CancellationScope.CancellationHandler%2A>.  
  
 Cet exemple illustre l'annulation d'une activité à partir de l'activité elle-même.  
  
 Le scénario utilisé par l'exemple pour illustrer l'activité <xref:System.Activities.Statements.CancellationScope> est un client qui souhaite acheter dès que possible un billet pour Miami. Il y a deux agences de voyage qui souhaitent traiter l'affaire. L'exemple utilise deux <xref:System.Activities.Statements.CancellationScope> dans une activité <xref:System.Activities.Statements.Parallel> pour modéliser cette logique métier. Le <xref:System.Activities.Statements.Parallel.CompletionCondition%2A> de l'activité <xref:System.Activities.Statements.Parallel> a la valeur `true` ; étant donné que <xref:System.Activities.Statements.Parallel.CompletionCondition%2A> est vérifié une fois chaque branche terminée, cela entraînera l'annulation de la branche restante après la fin de la première branche. L'application cliente demande aux deux agences d'acheter le billet, et lorsque la première confirme que le billet a été acheté, l'application annule la commande auprès de l'autre agence.  
  
## <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution CancelationScopeXAML.sln.  
  
2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
3.  Pour exécuter la solution, appuyez sur Ctrl+F5.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\CancellationScope`