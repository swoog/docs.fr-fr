---
title: 'Procédure : ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tabs [Windows Forms], removing from pages
- TabPage control
- TabControl control [Windows Forms], adding and removing tabs
- tabs [Windows Forms], adding to pages
- tab pages
ms.assetid: 66d4dfca-41e8-44e3-9c80-fb7ac4cb1619
ms.openlocfilehash: 723e05803b1f7d2bc56476248987085dbe5e23f0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59101599"
---
# <a name="how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol"></a><span data-ttu-id="ef247-102">Procédure : ajouter et supprimer des onglets avec le contrôle TabControl de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ef247-102">How to: Add and Remove Tabs with the Windows Forms TabControl</span></span>
<span data-ttu-id="ef247-103">Par défaut, un <xref:System.Windows.Forms.TabControl> contrôle contient deux <xref:System.Windows.Forms.TabPage> contrôles.</span><span class="sxs-lookup"><span data-stu-id="ef247-103">By default, a <xref:System.Windows.Forms.TabControl> control contains two <xref:System.Windows.Forms.TabPage> controls.</span></span> <span data-ttu-id="ef247-104">Vous pouvez accéder à ces onglets via le <xref:System.Windows.Forms.TabControl.TabPages%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ef247-104">You can access these tabs through the <xref:System.Windows.Forms.TabControl.TabPages%2A> property.</span></span>  
  
### <a name="to-add-a-tab-programmatically"></a><span data-ttu-id="ef247-105">Pour ajouter un onglet par programme</span><span class="sxs-lookup"><span data-stu-id="ef247-105">To add a tab programmatically</span></span>  
  
-   <span data-ttu-id="ef247-106">Utilisez le <xref:System.Windows.Forms.TabControl.TabPageCollection.Add%2A> méthode de la <xref:System.Windows.Forms.TabControl.TabPages%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ef247-106">Use the <xref:System.Windows.Forms.TabControl.TabPageCollection.Add%2A> method of the <xref:System.Windows.Forms.TabControl.TabPages%2A> property.</span></span>  
  
    ```vb  
    Dim myTabPage As New TabPage()  
    myTabPage.Text = "TabPage" & (TabControl1.TabPages.Count + 1)  
    TabControl1.TabPages.Add(myTabPage)  
    ```  
  
    ```csharp  
    string title = "TabPage " + (tabControl1.TabCount + 1).ToString();  
    TabPage myTabPage = new TabPage(title);  
    tabControl1.TabPages.Add(myTabPage);  
    ```  
  
    ```cpp  
    String^ title = String::Concat("TabPage ",  
       (tabControl1->TabCount + 1).ToString());  
    TabPage^ myTabPage = gcnew TabPage(title);  
    tabControl1->TabPages->Add(myTabPage);  
    ```  
  
### <a name="to-remove-a-tab-programmatically"></a><span data-ttu-id="ef247-107">Pour supprimer un onglet par programme</span><span class="sxs-lookup"><span data-stu-id="ef247-107">To remove a tab programmatically</span></span>  
  
-   <span data-ttu-id="ef247-108">Pour supprimer les onglets sélectionnés, utilisez la <xref:System.Windows.Forms.TabControl.TabPageCollection.Remove%2A> méthode de la <xref:System.Windows.Forms.TabControl.TabPages%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ef247-108">To remove selected tabs, use the <xref:System.Windows.Forms.TabControl.TabPageCollection.Remove%2A> method of the <xref:System.Windows.Forms.TabControl.TabPages%2A> property.</span></span>  
  
     <span data-ttu-id="ef247-109">- ou -</span><span class="sxs-lookup"><span data-stu-id="ef247-109">-or-</span></span>  
  
-   <span data-ttu-id="ef247-110">Pour supprimer tous les onglets, utilisez la <xref:System.Windows.Forms.TabControl.TabPageCollection.Clear%2A> méthode de la <xref:System.Windows.Forms.TabControl.TabPages%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ef247-110">To remove all tabs, use the <xref:System.Windows.Forms.TabControl.TabPageCollection.Clear%2A> method of the <xref:System.Windows.Forms.TabControl.TabPages%2A> property.</span></span>  
  
    ```vb  
    ' Removes the selected tab:  
    TabControl1.TabPages.Remove(TabControl1.SelectedTab)  
    ' Removes all the tabs:  
    TabControl1.TabPages.Clear()  
    ```  
  
    ```csharp  
    // Removes the selected tab:  
    tabControl1.TabPages.Remove(tabControl1.SelectedTab);  
    // Removes all the tabs:  
    tabControl1.TabPages.Clear();  
    ```  
  
    ```cpp  
    // Removes the selected tab:  
    tabControl1->TabPages->Remove(tabControl1->SelectedTab);  
    // Removes all the tabs:  
    tabControl1->TabPages->Clear();  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="ef247-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef247-111">See also</span></span>

- [<span data-ttu-id="ef247-112">Vue d’ensemble du contrôle TabControl</span><span class="sxs-lookup"><span data-stu-id="ef247-112">TabControl Control Overview</span></span>](tabcontrol-control-overview-windows-forms.md)
- [<span data-ttu-id="ef247-113">Procédure : ajouter un contrôle à un onglet</span><span class="sxs-lookup"><span data-stu-id="ef247-113">How to: Add a Control to a Tab Page</span></span>](how-to-add-a-control-to-a-tab-page.md)
- [<span data-ttu-id="ef247-114">Procédure : désactiver des onglets</span><span class="sxs-lookup"><span data-stu-id="ef247-114">How to: Disable Tab Pages</span></span>](how-to-disable-tab-pages.md)
- [<span data-ttu-id="ef247-115">Procédure : modifier l’aspect du contrôle TabControl Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ef247-115">How to: Change the Appearance of the Windows Forms TabControl</span></span>](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
