---
title: Expressions2
ms.date: 03/30/2017
ms.assetid: 43a85905-77b5-4893-bb38-1cb9b293d69d
ms.openlocfilehash: e852b62e6d0b6b4b3ddc19b197902de5325310a1
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45964655"
---
# <a name="expressions"></a>Expressions
Cet exemple montre comment utiliser des expressions de base dans un workflow. Il se compose d'un workflow qui calcule des statistiques de salaires de base pour deux employés d'une société fictive. Deux classes, `Employee` et `SalaryStats`, sont définies dans Employee.cs et SalaryStats.cs. Ces classes sont utilisées dans un workflow qui montre comment effectuer des opérations arithmétiques et de chaîne simples sur les propriétés de variables de types complexes.  
  
 Le workflow de calcul des salaires est défini à la fois en XAML et en C# pour montrer les deux styles de création. La version XAML est contenue dans SalaryCalculation.xaml, et peut être affichée et modifiée dans le concepteur de workflow. La version C# se trouve dans Program.cs. Les expressions utilisées en XAML sont conformes à la syntaxe Visual Basic et utilisent les activités d'expressions <xref:Microsoft.VisualBasic.Activities.VisualBasicValue%601> et <xref:Microsoft.VisualBasic.Activities.VisualBasicReference%601> à exécuter. Pour plus d’informations, consultez expressions Visual Basic [Expressions Visual Basic](https://go.microsoft.com/fwlink/?LinkId=165912). Par ailleurs, les expressions en C# sont écrites sous la forme d'expressions lambda et utilisent des activités d'expressions <xref:System.Activities.Expressions.LambdaValue%601> et <xref:System.Activities.Expressions.LambdaReference%601>. L’écriture d’expressions sous la forme d’expressions lambda permet au compilateur C# de fournir une mise en surbrillance de la syntaxe et une vérification statique. Pour plus d’informations sur les expressions lambda en c#, consultez [Expressions Lambda (Guide de programmation c#)](https://go.microsoft.com/fwlink/?LinkId=182082). Si un workflow est créé dans le code à l’aide de Visual Basic, les expressions lambda Visual Basic sont utilisées. Pour plus d’informations sur les expressions lambda en Visual Basic, consultez [Expressions Lambda (Visual Basic)](https://go.microsoft.com/fwlink/?LinkId=152437). Pour plus d’informations sur la création de workflows à l’aide de code, consultez [création de Workflows, des activités et des Expressions à l’aide de/Code impératif](../../../../docs/framework/windows-workflow-foundation/authoring-workflows-activities-and-expressions-using-imperative-code.md).  
  
#### <a name="to-run-the-sample"></a>Pour exécuter l'exemple  
  
1.  Ouvrez la solution Expressions.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Appuyez sur CTRL + MAJ + B pour générer la solution ou sélectionnez **générer la Solution** à partir de la **Build** menu.  
  
    > [!NOTE]
    >  Pour ouvrir SalaryCalculation.xaml dans le concepteur Visual Studio, vous devez d'abord compiler votre projet pour vérifier que les classes `Employee` et `SalaryStats` sont disponibles pour le concepteur.  
  
3.  Une fois la génération a réussi, appuyez sur F5 ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu. Vous pouvez également vous pouvez appuyer sur Ctrl + F5 ou sélectionnez **démarrer sans débogage** à partir de la **déboguer** menu afin d’exécuter sans débogage.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Expressions`