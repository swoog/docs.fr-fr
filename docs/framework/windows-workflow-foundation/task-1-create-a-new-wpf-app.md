---
title: 'Tâche 1 : créer une nouvelle application Windows Presentation Foundation.'
ms.date: 03/30/2017
ms.assetid: 270eaeba-9492-4532-af9f-403ce5c9935b
ms.openlocfilehash: 5576d6f893aa405d454758387334b85a473b0c73
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33517947"
---
# <a name="task-1-create-a-new-windows-presentation-foundation-application"></a>Tâche 1 : créer une nouvelle application Windows Presentation Foundation.
Dans cette tâche, vous créez une application Windows Presentation Foundation (WPF) vide en utilisant le modèle Visual Studio d’Application WPF et ajouter des références approprié [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] assemblys de workflow.  
  
### <a name="to-create-the-wpf-application-project"></a>Pour créer le projet d'application WPF  
  
1.  Ouvrez Visual Studio et sur le **fichier** menu, pointez sur **nouveau**, puis cliquez sur **projet**.  
  
2.  Dans le **nouveau projet** boîte de dialogue, sélectionnez soit **Visual C#** ou **Visual Basic** à partir de la **modèles installés** volet situé à gauche de la zone. Si la langue de votre choix n’apparaît pas, regardez sous **autres langages**.  
  
3.  Sélectionnez **Windows** dans les **modèles installés** volet.  
  
4.  Dans le volet supérieur, vérifiez que (la valeur par défaut) **.NET Framework 4** a été sélectionné dans la zone de liste déroulante, puis sélectionnez **Application WPF**.  
  
5.  Définissez le nom du projet pour **HostingApplication** au bas de la fenêtre.  
  
6.  Définissez le nom de la solution sur **RehostingTheDesigner**.  
  
7.  Cliquez sur **OK** pour créer le projet d’application. Visual Studio crée une base WPF UI pour votre application et inclut les fichiers code-behind XAML approprié.  
  
8.  Ajoutez des références aux **WorkflowModel** assemblys. Pour ce faire, dans **l’Explorateur de solutions**, avec le bouton droit le **HostingApplication** de projet et sélectionnez **ajouter une référence**.  
  
9. Dans le **ajouter une référence** boîte de dialogue, cliquez sur le **.NET** onglet, maintenez la touche CTRL enfoncée, sélectionnez les assemblys suivants, puis cliquez sur **OK**:  
  
    -   System.Activities  
  
    -   System.Activities.Presentation  
  
    -   System.Activities.Core.Presentation  
  
10. Cliquez sur **OK**.  
  
11. Consultez [tâche 2 : héberger le Workflow Designer](../../../docs/framework/windows-workflow-foundation/task-2-host-the-workflow-designer.md) pour en savoir plus sur l’hôte de la zone de conception du Concepteur de workflow.  
  
## <a name="see-also"></a>Voir aussi  
 [Réhébergement du concepteur de flux de travail](../../../docs/framework/windows-workflow-foundation/rehosting-the-workflow-designer.md)  
 [Tâche 2 : Héberger le concepteur de flux de travail](../../../docs/framework/windows-workflow-foundation/task-2-host-the-workflow-designer.md)
