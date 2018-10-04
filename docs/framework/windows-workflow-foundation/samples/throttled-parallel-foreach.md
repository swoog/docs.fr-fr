---
title: ParallelForEach limité
ms.date: 03/30/2017
ms.assetid: f2855b5f-e9a7-433d-96a4-40fc31025215
ms.openlocfilehash: 8691edb8a5a61204b187be8def553f2f06be0f0d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48581860"
---
# <a name="throttled-parallel-foreach"></a>ParallelForEach limité
Le `ThrottleParallelForEach` activité est similaire à la <!--zz <xref:System.Activities.Statements.ParallelForEach>--> `System.Activities.Statements.ParallelForEach` activité avec la seule exception qu’elle permet de définir un facteur de concurrence pour restreindre le nombre de branches simultanées à exécuter. L'activité `ThrottleParallelForEach` dérive de <xref:System.Activities.NativeActivity>, parce qu'elle doit planifier d'autres activités (activités enfants) et est uniquement accessible via la classe <xref:System.Activities.NativeActivityContext>.

## <a name="projects"></a>Projets

|**ProjectName**|**Description**|**Fichiers principaux**|
|-|-|-|
|ThrottledParallelForEach|Contient l'activité `ThrottledParallelForEach` et son concepteur.|ThrottledParallelForEach.cs<br /><br /> Définition de l'activité `ThrottledParallelForEach`.|
|CodeTestClient|Exemple d'application cliente qui configure et exécute un workflow avec un `ThrottledParallelForEach` à l'aide de code impératif.|Program.cs<br /><br /> Définit et exécute une instance de l'exemple de workflow.|

#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple

1.  À l’aide de Visual Studio 2010, ouvrez le fichier ThrottledParallelForEach.sln.

2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.

3.  Pour exécuter la solution, appuyez sur F5.

> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\ThrottledParallelForEach`