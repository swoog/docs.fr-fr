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
ms.openlocfilehash: be1f216af61c1e7b77e84c584dc9d965a97c56b2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539656"
---
# <a name="how-to-set-the-size-of-status-bar-panels"></a><span data-ttu-id="b8909-102">Procédure : Définir la taille des panneaux de barre d’état</span><span class="sxs-lookup"><span data-stu-id="b8909-102">How to: Set the Size of Status-Bar Panels</span></span>
> [!NOTE]
>  <span data-ttu-id="b8909-103">Le contrôle <xref:System.Windows.Forms.ToolStripStatusLabel> remplace le contrôle <xref:System.Windows.Forms.StatusBar> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.StatusBar> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="b8909-103">The <xref:System.Windows.Forms.ToolStripStatusLabel> control replaces and adds functionality to the <xref:System.Windows.Forms.StatusBar> control; however, the <xref:System.Windows.Forms.StatusBar> control is retained for both backward compatibility and future use, if you choose.</span></span>  
  
 <span data-ttu-id="b8909-104">Chaque instance de la <xref:System.Windows.Forms.StatusBarPanel> classe au sein d’un [du contrôle StatusBar](../../../../docs/framework/winforms/controls/statusbar-control-windows-forms.md) contrôle a un nombre de propriétés dynamiques qui déterminent sa largeur et de comportement de redimensionnement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b8909-104">Each instance of the <xref:System.Windows.Forms.StatusBarPanel> class within a [StatusBar Control](../../../../docs/framework/winforms/controls/statusbar-control-windows-forms.md) control has a number of dynamic properties that determine its width and resize behavior at run time.</span></span>  
  
### <a name="to-set-the-size-of-a-panel"></a><span data-ttu-id="b8909-105">Pour définir la taille d’un panneau</span><span class="sxs-lookup"><span data-stu-id="b8909-105">To set the size of a panel</span></span>  
  
1.  <span data-ttu-id="b8909-106">Dans une procédure, définissez le <xref:System.Windows.Forms.StatusBarPanel.AutoSize%2A>, <xref:System.Windows.Forms.StatusBarPanel.MinWidth%2A>, et <xref:System.Windows.Forms.StatusBarPanel.Width%2A> propriétés (ou tout sous-ensemble qui y sont) pour la barre d’état panneaux utilisant leur index passé le <xref:System.Windows.Forms.StatusBar.Panels%2A> propriété de la <xref:System.Windows.Forms.StatusBarPanel> collection.</span><span class="sxs-lookup"><span data-stu-id="b8909-106">In a procedure, set the <xref:System.Windows.Forms.StatusBarPanel.AutoSize%2A>, <xref:System.Windows.Forms.StatusBarPanel.MinWidth%2A>, and <xref:System.Windows.Forms.StatusBarPanel.Width%2A> properties (or any subset therein) for the status-bar panels using their index passed through the <xref:System.Windows.Forms.StatusBar.Panels%2A> property of the <xref:System.Windows.Forms.StatusBarPanel> collection.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="b8909-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8909-107">See also</span></span>
- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [<span data-ttu-id="b8909-108">Procédure pas à pas : La mise à jour des informations de barre d’état en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="b8909-108">Walkthrough: Updating Status Bar Information at Run Time</span></span>](../../../../docs/framework/winforms/controls/walkthrough-updating-status-bar-information-at-run-time.md)
- [<span data-ttu-id="b8909-109">Guide pratique pour Déterminer l’utilisateur a cliqué sur le panneau du contrôle StatusBar Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b8909-109">How to: Determine Which Panel in the Windows Forms StatusBar Control Was Clicked</span></span>](../../../../docs/framework/winforms/controls/determine-which-panel-wf-statusbar-control-was-clicked.md)
- [<span data-ttu-id="b8909-110">Vue d’ensemble du contrôle StatusBar</span><span class="sxs-lookup"><span data-stu-id="b8909-110">StatusBar Control Overview</span></span>](../../../../docs/framework/winforms/controls/statusbar-control-overview-windows-forms.md)
