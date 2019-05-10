---
title: 'Tâche 1 : créer une application Windows Presentation Foundation'
ms.date: 03/30/2017
ms.assetid: 270eaeba-9492-4532-af9f-403ce5c9935b
ms.openlocfilehash: 44152f0af73b134218cd975d93e186166b1e57ae
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64665319"
---
# <a name="task-1-create-a-new-windows-presentation-foundation-application"></a>Tâche 1 : créer une application Windows Presentation Foundation
Dans cette tâche, vous créez une application Windows Presentation Foundation (WPF) vide à l’aide du modèle Application WPF Visual Studio et ajoutez des références appropriés [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] assemblys de workflow.  
  
### <a name="to-create-the-wpf-application-project"></a>Pour créer le projet d'application WPF  
  
1. Ouvrez Visual Studio et sur le **fichier** menu, pointez sur **New**, puis cliquez sur **projet**.  
  
2. Dans le **nouveau projet** boîte de dialogue, sélectionnez soit **Visual C#**  ou **Visual Basic** à partir de la **modèles installés** volet de gauche côté de la zone. Si la langue de votre choix n’apparaît pas, regardez sous **autres langages**.  
  
3. Sélectionnez **Windows** dans le **modèles installés** volet.  
  
4. Dans le volet supérieur, vérifiez que (la valeur par défaut) **.NET Framework 4** a été sélectionné dans la zone de liste déroulante, puis sélectionnez **Application WPF**.  
  
5. Définissez le nom du projet à **HostingApplication** en bas de la fenêtre.  
  
6. La valeur est le nom de la solution **RehostingTheDesigner**.  
  
7. Cliquez sur **OK** pour créer le projet d’application. Visual Studio crée une base UI WPF pour votre application et inclut les fichiers code-behind XAML appropriée.  
  
8. Ajouter des références aux **WorkflowModel** assemblys. Pour ce faire, dans **l’Explorateur de solutions**, avec le bouton droit le **HostingApplication** de projet et sélectionnez **ajouter une référence**.  
  
9. Dans le **ajouter une référence** boîte de dialogue, cliquez sur le **.NET** onglet, maintenez la touche CTRL enfoncée, sélectionnez les assemblys suivants, puis cliquez sur **OK**:  
  
    - System.Activities  
  
    - System.Activities.Presentation  
  
    - System.Activities.Core.Presentation  
  
10. Cliquez sur **OK**.  
  
11. Consultez [tâche 2 : Héberger le Concepteur de flux de travail](task-2-host-the-workflow-designer.md) pour apprendre à héberger la zone de conception du Concepteur de workflow.  
  
## <a name="see-also"></a>Voir aussi

- [Réhébergement du concepteur de flux de travail](rehosting-the-workflow-designer.md)
- [Tâche 2 : Héberger le Concepteur de flux de travail](task-2-host-the-workflow-designer.md)
