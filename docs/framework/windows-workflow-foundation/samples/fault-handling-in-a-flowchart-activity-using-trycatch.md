---
title: Gestion des erreurs dans une activité Flowchart à l'aide de TryCatch
ms.date: 03/30/2017
ms.assetid: 50922964-bfe0-4ba8-9422-0e7220d514fd
ms.openlocfilehash: 81bfeb911658a6f363a9f0f95ecc7db68a02dbe2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59331258"
---
# <a name="fault-handling-in-a-flowchart-activity-using-trycatch"></a>Gestion des erreurs dans une activité Flowchart à l'aide de TryCatch
Cet exemple montre comment l'activité <xref:System.Activities.Statements.TryCatch> peut être utilisée dans une activité de flux de contrôle complexe.

 Dans cet exemple, un code promotionnel et un nombre d'enfants sont passés en tant que variables à une activité <xref:System.Activities.Statements.Flowchart> qui calcule une remise basée sur des formules qui correspondent au code promotionnel. L'exemple inclut les versions du code impératif et du concepteur de workflow de l'exemple.

 Le tableau suivant décrit en détail les variables pour l'activité `CreateFlowchartWithFaults`.

|Paramètres|Description|
|----------------|-----------------|
|promoCode|Code promotionnel. Type : Chaîne<br /><br /> Valeurs possibles avec la description entre parenthèses :<br /><br /> -Unique (Single)<br />-MNK (marié sans enfant).<br />-MWK (marié avec enfants).|
|numKids|Nombre d'enfants. Type : int|

 L'activité `CreateFlowchartWithFaults` utilise une activité <xref:System.Activities.Statements.FlowSwitch%601> qui active l'argument `promoCode` et calcule la remise à l'aide de la formule suivante.

|Valeur de `promoCode`|Remise (%)|
|--------------------------|--------------------|
|Single|10|
|MNK|15|
|MWK|15 + (1 : 1 /`numberOfKids`)\*10 **Remarque :**  Potentiellement, ce calcul peut lever un <xref:System.DivideByZeroException>. Par conséquent, le calcul de la remise est inclus dans un wrapper dans une activité <xref:System.Activities.Statements.TryCatch> qui intercepte l'exception <xref:System.DivideByZeroException> et définit la remise à zéro.|

#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple

1. À l’aide de Visual Studio 2010, ouvrez le fichier solution FlowchartWithFaultHandling.sln.

2. Pour générer la solution, appuyez sur Ctrl+Maj+B.

3. Pour exécuter la solution, appuyez sur F5.

> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\FlowChartWithFaultHandling`  
  
## <a name="see-also"></a>Voir aussi

- [Workflows d’organigramme](../flowchart-workflows.md)
- [Exceptions](../exceptions.md)
