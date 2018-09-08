---
title: Activité RangeEnumeration
ms.date: 03/30/2017
ms.assetid: ca5b78f4-94fa-4aa7-830d-26039ac422c8
ms.openlocfilehash: c9cf522227620422b414adc26cbc0bf338bf57d4
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44207588"
---
# <a name="rangeenumeration-activity"></a>Activité RangeEnumeration
Cet exemple montre comment créer une activité personnalisée qui itère au sein d'une collection de nombres. Le tableau suivant détaille les fichiers principaux inclus dans l'exemple.  
  
|Nom de fichier|Description|  
|---------------|-----------------|  
|RangeEnumeration.cs|Définit une activité personnalisée nommée `RangeEnumeration` qui substitue la classe <xref:System.Activities.NativeActivity> et effectue une boucle sur une série de nombres.|  
|RangeEnumerationSample.cs|Application cliente qui utilise l'activité `RangeEnumeration` pour itérer au sein d'une collection de nombres.|  
  
 Le tableau suivant détaille les propriétés de l'activité `RangeEnumeration`.  
  
|Propriété|Description|  
|--------------|-----------------|  
|Démarrer|Entier auquel démarrer la boucle.|  
|Arrêter|Entier auquel arrêter la boucle.|  
|Étape|Spécifie le volume d'itération à chaque fois.|  
|Corps|Spécifie le code à exécuter pendant chaque itération.|  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution RangeEnumeration.sln.  
  
2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
3.  Pour exécuter la solution, appuyez sur Ctrl+F5.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\RangeEnumeration`