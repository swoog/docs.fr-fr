---
title: 'Comment : insérer un MenuStrip dans un menu déroulant MDI (Windows Forms)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- MenuStrip control [Windows Forms], inserting
- MenuStrip control [Windows Forms], merging
- MDI [Windows Forms], merging menu items
ms.assetid: 0fad444e-26d9-49af-8860-044d9c10d608
ms.openlocfilehash: 9f7534720f9be185a176247ce00b0be5e2649bff
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33538752"
---
# <a name="how-to-insert-a-menustrip-into-an-mdi-drop-down-menu-windows-forms"></a><span data-ttu-id="da2ef-102">Comment : insérer un MenuStrip dans un menu déroulant MDI (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="da2ef-102">How to: Insert a MenuStrip into an MDI Drop-Down Menu (Windows Forms)</span></span>
<span data-ttu-id="da2ef-103">Dans certaines applications, le type d'une fenêtre enfant d'interface multidocument (MDI) peut être différent de celui de la fenêtre parente MDI.</span><span class="sxs-lookup"><span data-stu-id="da2ef-103">In some applications, the kind of a multiple-document interface (MDI) child window can be different from the MDI parent window.</span></span> <span data-ttu-id="da2ef-104">Par exemple, le parent MDI peut être une feuille de calcul et l'enfant MDI un graphique.</span><span class="sxs-lookup"><span data-stu-id="da2ef-104">For example, the MDI parent might be a spreadsheet, and the MDI child might be a chart.</span></span> <span data-ttu-id="da2ef-105">Dans ce cas, vous souhaitez mettre à jour le contenu du menu du parent MDI avec le contenu du menu de l'enfant MDI à mesure que des fenêtres enfants MDI de types différents sont activées.</span><span class="sxs-lookup"><span data-stu-id="da2ef-105">In that case, you want to update the contents of the MDI parent's menu with the contents of the MDI child's menu as MDI child windows of different kinds are activated.</span></span>  
  
 <span data-ttu-id="da2ef-106">La procédure suivante utilise le <xref:System.Windows.Forms.Form.IsMdiContainer%2A>, <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A>, <xref:System.Windows.Forms.MergeAction>, et <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> propriétés pour insérer un groupe d’éléments de menu du menu MDI enfant dans la partie déroulante du menu MDI parent.</span><span class="sxs-lookup"><span data-stu-id="da2ef-106">The following procedure uses the <xref:System.Windows.Forms.Form.IsMdiContainer%2A>, <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A>, <xref:System.Windows.Forms.MergeAction>, and <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> properties to insert a group of menu items from the MDI child menu into the drop-down part of the MDI parent menu.</span></span> <span data-ttu-id="da2ef-107">Fermeture de la fenêtre enfant MDI supprime les éléments de menu inséré le parent MDI.</span><span class="sxs-lookup"><span data-stu-id="da2ef-107">Closing the MDI child window removes the inserted menu items from the MDI parent.</span></span>  
  
### <a name="to-insert-a-menustrip-into-an-mdi-drop-down-menu"></a><span data-ttu-id="da2ef-108">Pour insérer un MenuStrip dans un menu du menu déroulant MDI</span><span class="sxs-lookup"><span data-stu-id="da2ef-108">To insert a MenuStrip into an MDI drop-down menu</span></span>  
  
1.  <span data-ttu-id="da2ef-109">Créez un formulaire et affectez la valeur `true` à sa propriété <xref:System.Windows.Forms.Form.IsMdiContainer%2A>.</span><span class="sxs-lookup"><span data-stu-id="da2ef-109">Create a form and set its <xref:System.Windows.Forms.Form.IsMdiContainer%2A> property to `true`.</span></span>  
  
2.  <span data-ttu-id="da2ef-110">Ajoutez un <xref:System.Windows.Forms.MenuStrip> à `Form1` et affectez la valeur `true` à la propriété <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> du <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="da2ef-110">Add a <xref:System.Windows.Forms.MenuStrip> to `Form1` and set the <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> property of the <xref:System.Windows.Forms.MenuStrip> to `true`.</span></span>  
  
3.  <span data-ttu-id="da2ef-111">Ajoutez un élément de menu de niveau supérieur au <xref:System.Windows.Forms.MenuStrip> de `Form1` et affectez la valeur `&File` à sa propriété <xref:System.Windows.Forms.Control.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="da2ef-111">Add a top-level menu item to the `Form1`<xref:System.Windows.Forms.MenuStrip> and set its <xref:System.Windows.Forms.Control.Text%2A> property to `&File`.</span></span>  
  
4.  <span data-ttu-id="da2ef-112">Ajoutez trois éléments de sous-menu à le `&File` élément de menu et le jeu de leurs <xref:System.Windows.Forms.ToolStripItem.Text%2A> propriétés `&Open`, `&Import from`, et `E&xit`.</span><span class="sxs-lookup"><span data-stu-id="da2ef-112">Add three submenu items to the `&File` menu item and set their <xref:System.Windows.Forms.ToolStripItem.Text%2A> properties to `&Open`, `&Import from`, and `E&xit`.</span></span>  
  
5.  <span data-ttu-id="da2ef-113">Ajouter deux éléments de sous-menu à le `&Import from` élément de sous-menu et ensemble leurs <xref:System.Windows.Forms.ToolStripItem.Text%2A> propriétés `&Word` et `&Excel`.</span><span class="sxs-lookup"><span data-stu-id="da2ef-113">Add two submenu items to the `&Import from` submenu item and set their <xref:System.Windows.Forms.ToolStripItem.Text%2A> properties to `&Word` and `&Excel`.</span></span>  
  
6.  <span data-ttu-id="da2ef-114">Ajoutez un formulaire au projet, ajoutez un <xref:System.Windows.Forms.MenuStrip> au formulaire et affectez la valeur `true` à la propriété <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> du <xref:System.Windows.Forms.MenuStrip> de `Form2`.</span><span class="sxs-lookup"><span data-stu-id="da2ef-114">Add a form to the project, add a <xref:System.Windows.Forms.MenuStrip> to the form, and set the <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> property of the `Form2`<xref:System.Windows.Forms.MenuStrip> to `true`.</span></span>  
  
7.  <span data-ttu-id="da2ef-115">Ajoutez un élément de menu de niveau supérieur au <xref:System.Windows.Forms.MenuStrip> de `Form2` et affectez la valeur `&File` à sa propriété <xref:System.Windows.Forms.ToolStripItem.Text%2A>.</span><span class="sxs-lookup"><span data-stu-id="da2ef-115">Add a top-level menu item to the `Form2`<xref:System.Windows.Forms.MenuStrip> and set its <xref:System.Windows.Forms.ToolStripItem.Text%2A> property to `&File`.</span></span>  
  
8.  <span data-ttu-id="da2ef-116">Ajouter des éléments de sous-menu à le `&File` menu de `Form2` dans l’ordre suivant : un <xref:System.Windows.Forms.ToolStripSeparator>, `&Save`, `&Close``and Save`et un autre <xref:System.Windows.Forms.ToolStripSeparator>.</span><span class="sxs-lookup"><span data-stu-id="da2ef-116">Add submenu items to the `&File` menu of `Form2` in the following order: a <xref:System.Windows.Forms.ToolStripSeparator>, `&Save`, `&Close``and Save`, and another <xref:System.Windows.Forms.ToolStripSeparator>.</span></span>  
  
9. <span data-ttu-id="da2ef-117">Définir le <xref:System.Windows.Forms.MergeAction> et <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> propriétés de la `Form2` les éléments de menu comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="da2ef-117">Set the <xref:System.Windows.Forms.MergeAction> and <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> properties of the `Form2` menu items as shown in the following table.</span></span>  
  
    |<span data-ttu-id="da2ef-118">Élément de menu Form2</span><span class="sxs-lookup"><span data-stu-id="da2ef-118">Form2 menu item</span></span>|<span data-ttu-id="da2ef-119">Valeur MergeAction</span><span class="sxs-lookup"><span data-stu-id="da2ef-119">MergeAction value</span></span>|<span data-ttu-id="da2ef-120">Valeur MergeIndex</span><span class="sxs-lookup"><span data-stu-id="da2ef-120">MergeIndex value</span></span>|  
    |---------------------|-----------------------|----------------------|  
    |<span data-ttu-id="da2ef-121">Fichier</span><span class="sxs-lookup"><span data-stu-id="da2ef-121">File</span></span>|<span data-ttu-id="da2ef-122">MatchOnly</span><span class="sxs-lookup"><span data-stu-id="da2ef-122">MatchOnly</span></span>|<span data-ttu-id="da2ef-123">-1</span><span class="sxs-lookup"><span data-stu-id="da2ef-123">-1</span></span>|  
    |<span data-ttu-id="da2ef-124">Séparateur</span><span class="sxs-lookup"><span data-stu-id="da2ef-124">Separator</span></span>|<span data-ttu-id="da2ef-125">Insert</span><span class="sxs-lookup"><span data-stu-id="da2ef-125">Insert</span></span>|<span data-ttu-id="da2ef-126">2</span><span class="sxs-lookup"><span data-stu-id="da2ef-126">2</span></span>|  
    |<span data-ttu-id="da2ef-127">Enregistrer</span><span class="sxs-lookup"><span data-stu-id="da2ef-127">Save</span></span>|<span data-ttu-id="da2ef-128">Insert</span><span class="sxs-lookup"><span data-stu-id="da2ef-128">Insert</span></span>|<span data-ttu-id="da2ef-129">3</span><span class="sxs-lookup"><span data-stu-id="da2ef-129">3</span></span>|  
    |<span data-ttu-id="da2ef-130">Enregistrer et fermer</span><span class="sxs-lookup"><span data-stu-id="da2ef-130">Save and Close</span></span>|<span data-ttu-id="da2ef-131">Insert</span><span class="sxs-lookup"><span data-stu-id="da2ef-131">Insert</span></span>|<span data-ttu-id="da2ef-132">4</span><span class="sxs-lookup"><span data-stu-id="da2ef-132">4</span></span>|  
    |<span data-ttu-id="da2ef-133">Séparateur</span><span class="sxs-lookup"><span data-stu-id="da2ef-133">Separator</span></span>|<span data-ttu-id="da2ef-134">Insert</span><span class="sxs-lookup"><span data-stu-id="da2ef-134">Insert</span></span>|<span data-ttu-id="da2ef-135">5</span><span class="sxs-lookup"><span data-stu-id="da2ef-135">5</span></span>|  
  
10. <span data-ttu-id="da2ef-136">Créez un gestionnaire d'événements pour l'événement <xref:System.Windows.Forms.Control.Click> du <xref:System.Windows.Forms.ToolStripMenuItem> de `&Open`.</span><span class="sxs-lookup"><span data-stu-id="da2ef-136">Create an event handler for the <xref:System.Windows.Forms.Control.Click> event of the `&Open`<xref:System.Windows.Forms.ToolStripMenuItem>.</span></span>  
  
11. <span data-ttu-id="da2ef-137">Dans le gestionnaire d'événements, insérez du code semblable à l'exemple de code suivant pour créer et afficher de nouvelles instances de `Form2` en tant qu'enfants MDI de `Form1`.</span><span class="sxs-lookup"><span data-stu-id="da2ef-137">Within the event handler, insert code similar to the following code example to create and display new instances of `Form2` as MDI children of `Form1`.</span></span>  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(ByVal sender As System.Object, _  
    ByVal e As System.EventArgs) Handles openToolStripMenuItem.Click  
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
  
12. <span data-ttu-id="da2ef-138">Insérez du code similaire à l'exemple de code suivant dans le `&Open`<xref:System.Windows.Forms.ToolStripMenuItem> pour inscrire le gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="da2ef-138">Place code similar to the following code example in the `&Open`<xref:System.Windows.Forms.ToolStripMenuItem> to register the event handler.</span></span>  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(sender As Object, e As _  
    EventArgs) Handles openToolStripMenuItem.Click  
    ```  
  
    ```csharp  
    this.openToolStripMenuItem.Click += new System.EventHandler(this.openToolStripMenuItem_Click);  
    ```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="da2ef-139">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="da2ef-139">Compiling the Code</span></span>  
 <span data-ttu-id="da2ef-140">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="da2ef-140">This example requires:</span></span>  
  
-   <span data-ttu-id="da2ef-141">deux <xref:System.Windows.Forms.Form> contrôles nommés `Form1` et `Form2` ;</span><span class="sxs-lookup"><span data-stu-id="da2ef-141">Two <xref:System.Windows.Forms.Form> controls named `Form1` and `Form2`.</span></span>  
  
-   <span data-ttu-id="da2ef-142">un contrôle <xref:System.Windows.Forms.MenuStrip> sur `Form1` nommé `menuStrip1` et un contrôle <xref:System.Windows.Forms.MenuStrip> sur `Form2` nommé `menuStrip2` ;</span><span class="sxs-lookup"><span data-stu-id="da2ef-142">A <xref:System.Windows.Forms.MenuStrip> control on `Form1` named `menuStrip1`, and a <xref:System.Windows.Forms.MenuStrip> control on `Form2` named `menuStrip2`.</span></span>  
  
-   <span data-ttu-id="da2ef-143">des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="da2ef-143">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da2ef-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da2ef-144">See Also</span></span>  
 [<span data-ttu-id="da2ef-145">Guide pratique pour créer des formulaires MDI parents</span><span class="sxs-lookup"><span data-stu-id="da2ef-145">How to: Create MDI Parent Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-mdi-parent-forms.md)  
 [<span data-ttu-id="da2ef-146">Guide pratique pour créer des formulaires MDI enfants</span><span class="sxs-lookup"><span data-stu-id="da2ef-146">How to: Create MDI Child Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-mdi-child-forms.md)  
 [<span data-ttu-id="da2ef-147">Vue d'ensemble du contrôle MenuStrip</span><span class="sxs-lookup"><span data-stu-id="da2ef-147">MenuStrip Control Overview</span></span>](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
