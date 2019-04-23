---
title: 'Procédure : Supprimer un ToolStripMenuItem d’un Menu du menu déroulant MDI (Windows Forms)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- menu items [Windows Forms], removing from MDI drop-down menus
- MenuStrip control [Windows Forms], merging
- MenuStrip control [Windows Forms], removing
- MDI [Windows Forms], merging menu items
ms.assetid: bdafe60d-82ee-45bc-97fe-eeefca6e54c1
ms.openlocfilehash: 7c84d260783e3a511b5ef6a651c71f1ee55acffe
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59295339"
---
# <a name="how-to-remove-a-toolstripmenuitem-from-an-mdi-drop-down-menu-windows-forms"></a><span data-ttu-id="0539f-102">Procédure : Supprimer un ToolStripMenuItem d’un Menu du menu déroulant MDI (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="0539f-102">How to: Remove a ToolStripMenuItem from an MDI Drop-Down Menu (Windows Forms)</span></span>
<span data-ttu-id="0539f-103">Dans certaines applications, le type d'une fenêtre enfant d'interface multidocument (MDI) peut être différent de celui de la fenêtre parente MDI.</span><span class="sxs-lookup"><span data-stu-id="0539f-103">In some applications, the kind of a multiple-document interface (MDI) child window can be different from the MDI parent window.</span></span> <span data-ttu-id="0539f-104">Par exemple, le parent MDI peut être une feuille de calcul et l'enfant MDI un graphique.</span><span class="sxs-lookup"><span data-stu-id="0539f-104">For example, the MDI parent might be a spreadsheet, and the MDI child might be a chart.</span></span> <span data-ttu-id="0539f-105">Dans ce cas, vous souhaitez mettre à jour le contenu du menu du parent MDI avec le contenu du menu de l'enfant MDI à mesure que des fenêtres enfants MDI de types différents sont activées.</span><span class="sxs-lookup"><span data-stu-id="0539f-105">In that case, you want to update the contents of the MDI parent's menu with the contents of the MDI child's menu as MDI child windows of different kinds are activated.</span></span>  
  
 <span data-ttu-id="0539f-106">La procédure suivante utilise le <xref:System.Windows.Forms.Form.IsMdiContainer%2A>, <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A>, <xref:System.Windows.Forms.MergeAction>, et <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> propriétés à supprimer un élément de menu à partir de la partie déroulante du menu MDI parent.</span><span class="sxs-lookup"><span data-stu-id="0539f-106">The following procedure uses the <xref:System.Windows.Forms.Form.IsMdiContainer%2A>, <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A>, <xref:System.Windows.Forms.MergeAction>, and <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> properties to remove a menu item from the drop-down part of the MDI parent menu.</span></span> <span data-ttu-id="0539f-107">Fermeture de la fenêtre MDI enfant restaure les éléments de menu supprimé au menu MDI parent.</span><span class="sxs-lookup"><span data-stu-id="0539f-107">Closing the MDI child window restores the removed menu items to the MDI parent menu.</span></span>  
  
### <a name="to-remove-a-menustrip-from-an-mdi-drop-down-menu"></a><span data-ttu-id="0539f-108">Pour supprimer un MenuStrip dans le menu déroulant MDI</span><span class="sxs-lookup"><span data-stu-id="0539f-108">To remove a MenuStrip from an MDI drop-down menu</span></span>  
  
1. <span data-ttu-id="0539f-109">Créez un formulaire et affectez la valeur `true` à sa propriété <xref:System.Windows.Forms.Form.IsMdiContainer%2A>.</span><span class="sxs-lookup"><span data-stu-id="0539f-109">Create a form and set its <xref:System.Windows.Forms.Form.IsMdiContainer%2A> property to `true`.</span></span>  
  
2. <span data-ttu-id="0539f-110">Ajoutez un <xref:System.Windows.Forms.MenuStrip> à `Form1` et affectez la valeur `true` à la propriété <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> du <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="0539f-110">Add a <xref:System.Windows.Forms.MenuStrip> to `Form1` and set the <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> property of the <xref:System.Windows.Forms.MenuStrip> to `true`.</span></span>  
  
3. <span data-ttu-id="0539f-111">Ajoutez un élément de menu de niveau supérieur au <xref:System.Windows.Forms.MenuStrip> de `Form1` et affectez la valeur `&File` à sa propriété <xref:System.Windows.Forms.Control.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="0539f-111">Add a top-level menu item to the `Form1`<xref:System.Windows.Forms.MenuStrip> and set its <xref:System.Windows.Forms.Control.Text%2A> property to `&File`.</span></span>  
  
4. <span data-ttu-id="0539f-112">Ajoutez trois éléments de sous-menu à la `&File` élément de menu et définissez leurs <xref:System.Windows.Forms.ToolStripItem.Text%2A> propriétés à `&Open`, `&Import from`, et `E&xit`.</span><span class="sxs-lookup"><span data-stu-id="0539f-112">Add three submenu items to the `&File` menu item and set their <xref:System.Windows.Forms.ToolStripItem.Text%2A> properties to `&Open`, `&Import from`, and `E&xit`.</span></span>  
  
5. <span data-ttu-id="0539f-113">Ajoutez deux éléments de sous-menu à la `&Import from` élément de sous-menu et définissez leurs <xref:System.Windows.Forms.ToolStripItem.Text%2A> propriétés à `&Word` et `&Excel`.</span><span class="sxs-lookup"><span data-stu-id="0539f-113">Add two submenu items to the `&Import from` submenu item and set their <xref:System.Windows.Forms.ToolStripItem.Text%2A> properties to `&Word` and `&Excel`.</span></span>  
  
6. <span data-ttu-id="0539f-114">Ajoutez un formulaire au projet, ajoutez un <xref:System.Windows.Forms.MenuStrip> au formulaire et affectez la valeur `true` à la propriété <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> du <xref:System.Windows.Forms.MenuStrip> de `Form2`.</span><span class="sxs-lookup"><span data-stu-id="0539f-114">Add a form to the project, add a <xref:System.Windows.Forms.MenuStrip> to the form, and set the <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> property of the `Form2`<xref:System.Windows.Forms.MenuStrip> to `true`.</span></span>  
  
7. <span data-ttu-id="0539f-115">Ajoutez un élément de menu de niveau supérieur au <xref:System.Windows.Forms.MenuStrip> de `Form2` et affectez la valeur `&File` à sa propriété <xref:System.Windows.Forms.ToolStripItem.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="0539f-115">Add a top-level menu item to the `Form2`<xref:System.Windows.Forms.MenuStrip> and set its <xref:System.Windows.Forms.ToolStripItem.Text%2A> property to `&File`.</span></span>  
  
8. <span data-ttu-id="0539f-116">Ajouter un `&Import from` élément de sous-menu à la `&File` menu de `Form2`et ajoutez un `&Word` élément de sous-menu à le `&File` menu.</span><span class="sxs-lookup"><span data-stu-id="0539f-116">Add an `&Import from` submenu item to the `&File` menu of `Form2`, and add an `&Word` submenu item to the `&File` menu.</span></span>  
  
9. <span data-ttu-id="0539f-117">Définir le <xref:System.Windows.Forms.MergeAction> et <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> propriétés de la `Form2` les éléments de menu comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0539f-117">Set the <xref:System.Windows.Forms.MergeAction> and <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> properties of the `Form2` menu items as shown in the following table.</span></span>  
  
    |<span data-ttu-id="0539f-118">Élément de menu Form2</span><span class="sxs-lookup"><span data-stu-id="0539f-118">Form2 menu item</span></span>|<span data-ttu-id="0539f-119">Valeur MergeAction</span><span class="sxs-lookup"><span data-stu-id="0539f-119">MergeAction value</span></span>|<span data-ttu-id="0539f-120">Valeur MergeIndex</span><span class="sxs-lookup"><span data-stu-id="0539f-120">MergeIndex value</span></span>|  
    |---------------------|-----------------------|----------------------|  
    |<span data-ttu-id="0539f-121">Fichier</span><span class="sxs-lookup"><span data-stu-id="0539f-121">File</span></span>|<span data-ttu-id="0539f-122">MatchOnly</span><span class="sxs-lookup"><span data-stu-id="0539f-122">MatchOnly</span></span>|<span data-ttu-id="0539f-123">-1</span><span class="sxs-lookup"><span data-stu-id="0539f-123">-1</span></span>|  
    |<span data-ttu-id="0539f-124">Importer à partir de</span><span class="sxs-lookup"><span data-stu-id="0539f-124">Import from</span></span>|<span data-ttu-id="0539f-125">MatchOnly</span><span class="sxs-lookup"><span data-stu-id="0539f-125">MatchOnly</span></span>|<span data-ttu-id="0539f-126">-1</span><span class="sxs-lookup"><span data-stu-id="0539f-126">-1</span></span>|  
    |<span data-ttu-id="0539f-127">Word</span><span class="sxs-lookup"><span data-stu-id="0539f-127">Word</span></span>|<span data-ttu-id="0539f-128">Remove</span><span class="sxs-lookup"><span data-stu-id="0539f-128">Remove</span></span>|<span data-ttu-id="0539f-129">-1</span><span class="sxs-lookup"><span data-stu-id="0539f-129">-1</span></span>|  
  
10. <span data-ttu-id="0539f-130">Dans `Form1`, créez un gestionnaire d’événements pour le <xref:System.Windows.Forms.Control.Click> événements de la `&Open` <xref:System.Windows.Forms.ToolStripMenuItem>.</span><span class="sxs-lookup"><span data-stu-id="0539f-130">In `Form1`, create an event handler for the <xref:System.Windows.Forms.Control.Click> event of the `&Open`<xref:System.Windows.Forms.ToolStripMenuItem>.</span></span>  
  
11. <span data-ttu-id="0539f-131">Dans le Gestionnaire d’événements, insérez du code semblable à l’exemple de code suivant pour créer et afficher les nouvelles instances de `Form2` en tant qu’enfants MDI de `Form1`:</span><span class="sxs-lookup"><span data-stu-id="0539f-131">Within the event handler, insert code similar to the following code example to create and display new instances of `Form2` as MDI children of `Form1`:</span></span>  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles openToolStripMenuItem.Click  
        Dim NewMDIChild As New Form2()  
        'Set the parent form of the child window.  
            NewMDIChild.MdiParent = Me  
        'Display the new form.  
            NewMDIChild.Show()  
    End Sub  
    ```  
  
    ```csharp  
    private void openToolStripMenuItem_Click(object sender, EventArgs e)  
    {  
        Form2 newMDIChild = new Form2();  
        // Set the parent form of the child window.  
            newMDIChild.MdiParent = this;  
        // Display the new form.  
            newMDIChild.Show();  
    }  
    ```  
  
12. <span data-ttu-id="0539f-132">Insérez du code similaire à l'exemple de code suivant dans le `&Open`<xref:System.Windows.Forms.ToolStripMenuItem> pour inscrire le gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="0539f-132">Place code similar to the following code example in the `&Open`<xref:System.Windows.Forms.ToolStripMenuItem> to register the event handler.</span></span>  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(sender As Object, e As _  
    EventArgs) Handles openToolStripMenuItem.Click  
    ```  
  
    ```csharp  
    this.openToolStripMenuItem.Click += new _  
    System.EventHandler(this.openToolStripMenuItem_Click);  
    ```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0539f-133">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0539f-133">Compiling the Code</span></span>  
 <span data-ttu-id="0539f-134">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="0539f-134">This example requires:</span></span>  
  
-   <span data-ttu-id="0539f-135">deux <xref:System.Windows.Forms.Form> contrôles nommés `Form1` et `Form2` ;</span><span class="sxs-lookup"><span data-stu-id="0539f-135">Two <xref:System.Windows.Forms.Form> controls named `Form1` and `Form2`.</span></span>  
  
-   <span data-ttu-id="0539f-136">un contrôle <xref:System.Windows.Forms.MenuStrip> sur `Form1` nommé `menuStrip1` et un contrôle <xref:System.Windows.Forms.MenuStrip> sur `Form2` nommé `menuStrip2` ;</span><span class="sxs-lookup"><span data-stu-id="0539f-136">A <xref:System.Windows.Forms.MenuStrip> control on `Form1` named `menuStrip1`, and a <xref:System.Windows.Forms.MenuStrip> control on `Form2` named `menuStrip2`.</span></span>  
  
-   <span data-ttu-id="0539f-137">des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0539f-137">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0539f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0539f-138">See also</span></span>

- [<span data-ttu-id="0539f-139">Guide pratique pour Créer des formulaires MDI parents</span><span class="sxs-lookup"><span data-stu-id="0539f-139">How to: Create MDI Parent Forms</span></span>](../advanced/how-to-create-mdi-parent-forms.md)
- [<span data-ttu-id="0539f-140">Guide pratique pour Créer des formulaires MDI enfants</span><span class="sxs-lookup"><span data-stu-id="0539f-140">How to: Create MDI Child Forms</span></span>](../advanced/how-to-create-mdi-child-forms.md)
- [<span data-ttu-id="0539f-141">Vue d'ensemble du contrôle MenuStrip</span><span class="sxs-lookup"><span data-stu-id="0539f-141">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
