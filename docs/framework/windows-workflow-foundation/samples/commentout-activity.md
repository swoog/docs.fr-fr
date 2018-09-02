---
title: Activité CommentOut
ms.date: 03/30/2017
ms.assetid: 340204c3-f827-45fb-870e-55e2ac457ca5
ms.openlocfilehash: 3e9f6945755bd60c551674ea8a3471a9f612da52
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43404748"
---
# <a name="commentout-activity"></a>Activité CommentOut
Cet exemple montre comment écrire une activité personnalisée qui supprime d’autres activités du chemin d’exécution, en les transformant en fait en commentaire.  
  
## <a name="the-commentout-activity"></a>Activité CommentOut  
 Pour atteindre son objectif, l'activité CommentOut dérive de la classe de base <xref:System.Activities.CodeActivity> et implémente une méthode <xref:System.Activities.CodeActivity.Execute%2A> vide.  
  
```  
protected override void Execute(CodeActivityContext context)  
{  
}  
```  
  
 La classe est déclarée comme indiqué dans l'exemple suivant.  
  
```  
[Designer(typeof(CommentOutDesigner))]  
[ContentProperty("Body")]  
public sealed class CommentOut : CodeActivity  
```  
  
 L'attribut `Designer` spécifie la classe qui implémente l'interface graphique de l'activité au moment du design. L'attribut `ContentProperty` déclare que la propriété `"Body"` peut être ignorée dans la représentation XAML d'une instance de cette activité.  
  
```  
<Border x:Uid="Border_1" BorderThickness ="1">  
    <sad:WorkflowItemPresenter   
    x:Uid="sad:WorkflowItemPresenter_1" AutomationProperties.AutomationId="Body" Item="{Binding Path=ModelItem.Body, Mode=TwoWay}"  
    AllowedItemType="{x:Type sa:Activity}"  
    HintText="Drop activity here"   
    Margin="5,5,5,5" />  
</Border>  
```  
  
 Dans la classe de concepteur, le XAML est utilisé pour créer une représentation visuelle personnalisée de l'activité. <xref:System.Activities.Presentation.WorkflowItemPresenter> est une classe qui fournit l'éditeur visuel.  
  
 Une seule activité peut être supprimée sur la surface de l'activité `CommentOut`. Si vous voulez ajouter plusieurs activités à cette surface, faites-y d'abord glisser une activité de séquence.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Ouvrez CommentOut.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Compilez la solution en appuyant sur CTRL+MAJ+B.  
  
3.  Démarrez l'exemple sans débogage en appuyant sur CTRL+F5.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\CommentOut`
