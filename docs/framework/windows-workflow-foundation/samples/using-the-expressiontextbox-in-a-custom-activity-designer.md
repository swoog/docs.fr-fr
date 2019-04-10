---
title: Utilisation d'ExpressionTextBox dans un concepteur d'activités personnalisées
ms.date: 03/30/2017
ms.assetid: f82e73e7-a256-4a4d-82b7-c0d62f4ab5e7
ms.openlocfilehash: 7c1ba262046a665b8d63157fe3cdb4b1a41c37bf
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59229379"
---
# <a name="using-the-expressiontextbox-in-a-custom-activity-designer"></a>Utilisation d'ExpressionTextBox dans un concepteur d'activités personnalisées
Cet exemple montre comment utiliser le <xref:System.Activities.Presentation.View.ExpressionTextBox> dans un concepteur d'activités personnalisées. L'activité personnalisée, `MultiAssign`, assigne deux valeurs de chaîne à deux variables String. Certains contrôles <xref:System.Activities.Presentation.View.ExpressionTextBox> sont liés à <xref:System.Activities.InArgument>s et d'autres à <xref:System.Activities.OutArgument>s.

## <a name="sample-details"></a>Détails de l'exemple
 Le `ArgumentToExpressionConverter` est le convertisseur de type utilisé lors de la liaison d’expressions aux arguments. Affectez `ConverterParameter` ou `In` à `Out`. `InOut` n’est pas pris en charge.

 Le `UseLocationExpression` attribut est utilisé sur `OutArgument`s pour spécifier que l’expression doit être une expression L-value (« left value » ou « location value »). Dans la plupart des cas, une expression L-value est un identificateur Visual Basic valide utilisé pour indiquer que le `OutArgument` qui est retourné est un nom de variable ou d’argument.

 L'attribut `MaxLines` a la valeur un dans cet exemple et `MinLines` n'est pas défini. Cela indique que le <xref:System.Activities.Presentation.View.ExpressionTextBox> a une taille fixe d'une ligne indépendamment de la quantité de texte tapée par l'utilisateur. Pour permettre au <xref:System.Activities.Presentation.View.ExpressionTextBox> de s'agrandir pour s'ajuster à l'entrée d'utilisateur, affectez à `MaxLines` une valeur supérieure à `MinLines`.

 Un ExpressionTextBox peut être lié uniquement aux arguments et ne peut pas être lié aux propriétés CLR.

#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple

1.  À l’aide de Visual Studio 2010, ouvrez le fichier ExpressionTextBoxSample.sln.

2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.

#### <a name="to-run-this-sample"></a>Pour exécuter cet exemple

1.  Ajoutez une nouvelle application console de workflow à la solution.

2.  Ajoutez une référence à la **ExpressionTextBoxSample** projet à partir de la nouvelle Application Console de Workflow.

3.  Générez la solution.

4.  Faites glisser le **MultiAssign** activité à partir de la boîte à outils et déposez-la dans le flux de travail.

> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\CustomActivityDesigners\ExpressionTextBox`  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Activities.Presentation.View.ExpressionTextBox>
- [Développement d'applications avec Workflow Designer](/visualstudio/workflow-designer/developing-applications-with-the-workflow-designer)
