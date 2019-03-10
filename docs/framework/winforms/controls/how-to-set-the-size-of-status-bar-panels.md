---
title: 'Procédure : Définir la taille des panneaux de barre d’état'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- StatusBar control [Windows Forms], panel size
- status bars [Windows Forms], setting panel size
- panels [Windows Forms], setting size in status bars
ms.assetid: a01bee43-d9eb-4954-84e6-45a93532d08d
ms.openlocfilehash: 5b78463ca273f089f036166f5339977be435ccc9
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57711939"
---
# <a name="how-to-set-the-size-of-status-bar-panels"></a>Procédure : Définir la taille des panneaux de barre d’état
> [!NOTE]
>  Le contrôle <xref:System.Windows.Forms.ToolStripStatusLabel> remplace le contrôle <xref:System.Windows.Forms.StatusBar> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.StatusBar> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.  
  
 Chaque instance de la <xref:System.Windows.Forms.StatusBarPanel> classe au sein d’un [du contrôle StatusBar](statusbar-control-windows-forms.md) contrôle a un nombre de propriétés dynamiques qui déterminent sa largeur et de comportement de redimensionnement au moment de l’exécution.  
  
### <a name="to-set-the-size-of-a-panel"></a>Pour définir la taille d’un panneau  
  
1.  Dans une procédure, définissez le <xref:System.Windows.Forms.StatusBarPanel.AutoSize%2A>, <xref:System.Windows.Forms.StatusBarPanel.MinWidth%2A>, et <xref:System.Windows.Forms.StatusBarPanel.Width%2A> propriétés (ou tout sous-ensemble qui y sont) pour la barre d’état panneaux utilisant leur index passé le <xref:System.Windows.Forms.StatusBar.Panels%2A> propriété de la <xref:System.Windows.Forms.StatusBarPanel> collection.  
  
    ```vb  
    Public Sub SetStatusBarPanelSize()  
    ' Create panel and set text property.  
       StatusBar1.Panels.Add("One")  
    ' Set properties of panels.  
       StatusBar1.Panels(0).AutoSize = StatusBarPanelAutoSize.Spring  
       StatusBar1.Panels(0).Width = 200  
    ' Enable the StatusBar control to display panels.  
       StatusBar1.ShowPanels = True  
        End Sub  
    ```  
  
    ```csharp  
    public void SetStatusBarPanelSize()  
    {  
       // Create panel and set text property.  
       statusBar1.Panels.Add("One");  
       // Set properties of panels.  
       statusBar1.Panels[0].AutoSize = StatusBarPanelAutoSize.Spring;  
       statusBar1.Panels[0].Width = 200;  
       statusBar1.ShowPanels = true;  
    }  
    ```  
  
    ```cpp  
    public:  
       void SetStatusBarPanelSize()  
       {  
          // Create panel and set text property.  
          statusBar1->Panels->Add("One");  
          // Set properties of panels.  
          statusBar1->Panels[0]->AutoSize =  
             StatusBarPanelAutoSize::Spring;  
          statusBar1->Panels[0]->Width = 200;  
          statusBar1->ShowPanels = true;  
       }  
    ```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [Procédure pas à pas : La mise à jour des informations de barre d’état en cours d’exécution](walkthrough-updating-status-bar-information-at-run-time.md)
- [Guide pratique pour Déterminer l’utilisateur a cliqué sur le panneau du contrôle StatusBar Windows Forms](determine-which-panel-wf-statusbar-control-was-clicked.md)
- [Vue d’ensemble du contrôle StatusBar](statusbar-control-overview-windows-forms.md)
