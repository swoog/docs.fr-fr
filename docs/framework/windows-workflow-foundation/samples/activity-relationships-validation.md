---
title: Validation des relations des activités
ms.date: 03/30/2017
ms.assetid: 6f11a34e-ed67-4bce-88ce-7e96bbb4d052
ms.openlocfilehash: e6dd0e6a7b48444073ebae378e21c1b45977a1f0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33515106"
---
# <a name="activity-relationships-validation"></a>Validation des relations des activités
Cet exemple se compose de trois activités, `CreateCity`, `CreateState` et `CreateCountry`. `CreateCity` doit être à l'intérieur d'une activité `CreateState`, et `CreateState` à l'intérieur d'une activité `CreateCountry`. Pour les besoins de cet exemple, la logique de validation est dans le code pour l'activité `CreateState`, et dans XAML pour l'activité `CreateCity`. Les deux contraintes ont le même comportement.  
  
 [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] fournit les trois activités d'assistance suivantes qui permettent au développeur de valider les relations entre les activités :  
  
 <xref:System.Activities.Validation.GetParentChain>  
 Fournit la collection de toutes les activités qui appartiennent au parent du nœud actuel  
  
 <xref:System.Activities.Validation.GetChildSubtree>  
 Fournit la collection de toutes les activités qui appartiennent à la sous-arborescence du nœud actuel, à l'exclusion du nœud actuel  
  
 <xref:System.Activities.Validation.GetWorkflowTree>  
 Fournit la collection de toutes les activités de la même arborescence que le nœud actuel  
  
 Dans l'exemple, une activité <xref:System.Activities.Statements.ForEach%601> est utilisée pour parcourir la collection retournée par <xref:System.Activities.Validation.GetParentChain> Pour chaque élément de la collection, son type est comparé à `CreateCountry` (ou à `CreateState` si `CreateCity` est validé). Une fois que qu'une correspondance est trouvée, l'indicateur de résultat a la valeur `true`. Enfin, un <xref:System.Activities.Validation.AssertValidation> est utilisé pour générer une erreur de validation si l'indicateur de résultat a la valeur `false`.  
  
### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Ouvrez l'exemple de solution ContainmentValidation.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Générez la solution.  
  
3.  Appuyez sur Ctrl+F5 pour lancer le programme.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer :  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant :  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Validation\ActivityRelationships`
