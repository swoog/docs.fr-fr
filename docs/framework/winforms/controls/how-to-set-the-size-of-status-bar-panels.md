---
title: 'Procédure : définir la taille des panneaux de barre d’état'
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
ms.openlocfilehash: c6c9d6570e9b5c2f6d4eee0262c3d90e29e4b493
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59131052"
---
# <a name="how-to-set-the-size-of-status-bar-panels"></a><span data-ttu-id="b5bcb-102">Procédure : définir la taille des panneaux de barre d’état</span><span class="sxs-lookup"><span data-stu-id="b5bcb-102">How to: Set the Size of Status-Bar Panels</span></span>
> [!NOTE]
>  <span data-ttu-id="b5bcb-103">Le contrôle <xref:System.Windows.Forms.ToolStripStatusLabel> remplace le contrôle <xref:System.Windows.Forms.StatusBar> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.StatusBar> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="b5bcb-103">The <xref:System.Windows.Forms.ToolStripStatusLabel> control replaces and adds functionality to the <xref:System.Windows.Forms.StatusBar> control; however, the <xref:System.Windows.Forms.StatusBar> control is retained for both backward compatibility and future use, if you choose.</span></span>  
  
 <span data-ttu-id="b5bcb-104">Chaque instance de la <xref:System.Windows.Forms.StatusBarPanel> classe au sein d’un [du contrôle StatusBar](statusbar-control-windows-forms.md) contrôle a un nombre de propriétés dynamiques qui déterminent sa largeur et de comportement de redimensionnement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b5bcb-104">Each instance of the <xref:System.Windows.Forms.StatusBarPanel> class within a [StatusBar Control](statusbar-control-windows-forms.md) control has a number of dynamic properties that determine its width and resize behavior at run time.</span></span>  
  
### <a name="to-set-the-size-of-a-panel"></a><span data-ttu-id="b5bcb-105">Pour définir la taille d’un panneau</span><span class="sxs-lookup"><span data-stu-id="b5bcb-105">To set the size of a panel</span></span>  
  
1.  <span data-ttu-id="b5bcb-106">Dans une procédure, définissez le <xref:System.Windows.Forms.StatusBarPanel.AutoSize%2A>, <xref:System.Windows.Forms.StatusBarPanel.MinWidth%2A>, et <xref:System.Windows.Forms.StatusBarPanel.Width%2A> propriétés (ou tout sous-ensemble qui y sont) pour la barre d’état panneaux utilisant leur index passé le <xref:System.Windows.Forms.StatusBar.Panels%2A> propriété de la <xref:System.Windows.Forms.StatusBarPanel> collection.</span><span class="sxs-lookup"><span data-stu-id="b5bcb-106">In a procedure, set the <xref:System.Windows.Forms.StatusBarPanel.AutoSize%2A>, <xref:System.Windows.Forms.StatusBarPanel.MinWidth%2A>, and <xref:System.Windows.Forms.StatusBarPanel.Width%2A> properties (or any subset therein) for the status-bar panels using their index passed through the <xref:System.Windows.Forms.StatusBar.Panels%2A> property of the <xref:System.Windows.Forms.StatusBarPanel> collection.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="b5bcb-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5bcb-107">See also</span></span>

- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [<span data-ttu-id="b5bcb-108">Procédure pas à pas : mise à jour des informations de barre d’état au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="b5bcb-108">Walkthrough: Updating Status Bar Information at Run Time</span></span>](walkthrough-updating-status-bar-information-at-run-time.md)
- [<span data-ttu-id="b5bcb-109">Procédure : déterminer sur quel panneau l’utilisateur a cliqué dans le contrôle StatusBar Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b5bcb-109">How to: Determine Which Panel in the Windows Forms StatusBar Control Was Clicked</span></span>](determine-which-panel-wf-statusbar-control-was-clicked.md)
- [<span data-ttu-id="b5bcb-110">Vue d’ensemble du contrôle StatusBar</span><span class="sxs-lookup"><span data-stu-id="b5bcb-110">StatusBar Control Overview</span></span>](statusbar-control-overview-windows-forms.md)
