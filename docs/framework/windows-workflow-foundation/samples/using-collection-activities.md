---
title: Utilisation d’activités de collection
ms.date: 03/30/2017
ms.assetid: e1977cf8-1695-4071-b946-7046fe39601e
ms.openlocfilehash: 3c30a7fb46d9b155ec645a7b6845715d808d63b6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33516593"
---
# <a name="using-collection-activities"></a>Utilisation d’activités de collection
Cet exemple montre comment utiliser les activités de collection (<xref:System.Activities.Statements.AddToCollection%601>, <xref:System.Activities.Statements.ClearCollection%601>, <xref:System.Activities.Statements.ExistsInCollection%601> et <xref:System.Activities.Statements.RemoveFromCollection%601>) avec une classe qui implémente l'interface <xref:System.Collections.ICollection> et comment créer une activité personnalisée qui itère au sein d'une collection pour imprimer le contenu de chaque élément de la collection. L'activité personnalisée nommée `PrintCollection`imprime sur la console les membres d'élément d'une collection nommée `Numbers`.  
  
 Le tableau suivant décrit les quatre activités qui fournissent la manipulation de collection pour les workflows.  
  
|Nom de l'activité|Description|  
|-------------------|-----------------|  
|<xref:System.Activities.Statements.AddToCollection%601>|Ajoute un élément à une collection.|  
|<xref:System.Activities.Statements.ClearCollection%601>|Efface tous les éléments d'une collection.|  
|<xref:System.Activities.Statements.ExistsInCollection%601>|Retourne `true` si l'élément spécifié existe dans la collection.|  
|<xref:System.Activities.Statements.RemoveFromCollection%601>|Supprime un élément d'une collection.|  
  
 L'exemple se compose de deux solutions, une sous le répertoire CodedWorkflow et l'autre sous le répertoire DesignerWorkflow. Elles illustrent deux façons différentes d'utiliser les activités dans le même but.  
  
|Solution|Description|Fichiers principaux|  
|-|-|-|  
|CodedWorkflow|Exemple d’application cliente qui montre comment appeler les activités de collection par programmation.|**PrintCollection.cs**: activité d’assistance pour imprimer sur la console chaque élément dans une collection.<br /><br /> **Program.cs**: crée par programmation une activité de séquence qui contient une série d’activités de collection et l’exécute.|  
|DesignerWorkflow|Exemple d’application cliente qui montre comment utiliser de façon déclarative les activités de collection dans le concepteur de workflow.|**CollectionWorkflow.xaml**: un workflow créé de façon déclarative avec le concepteur qui utilise les activités de collection.<br /><br /> **PrintCollection.cs**: activité d’assistance pour imprimer sur la console chaque élément dans une collection.<br /><br /> **Program.cs**: appelle le workflow décrit dans CollectionWorkflow.xaml.|  
  
 Dans la démonstration, les membres d'élément de collection `Numbers` sont imprimés sur la console à l'aide d'une activité définie pour la personnalisation appelée `PrintCollection`.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution Collection.sln.  
  
2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
3.  Pour exécuter la solution, appuyez sur Ctrl+F5.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\Collection`