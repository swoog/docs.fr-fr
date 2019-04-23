---
title: Architecture du contrôle DataGridView (Windows Forms)
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], architecture
ms.assetid: 1c6cabf0-02ee-4bbc-9574-b54bb7f5b19e
ms.openlocfilehash: 892168ec282fbf168c43515e0718fe5486a345a8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59130258"
---
# <a name="datagridview-control-architecture-windows-forms"></a><span data-ttu-id="36792-102">Architecture du contrôle DataGridView (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="36792-102">DataGridView Control Architecture (Windows Forms)</span></span>
<span data-ttu-id="36792-103">Le <xref:System.Windows.Forms.DataGridView> contrôle et ses classes connexes sont conçus pour être un système flexible et extensible pour afficher et modifier des données tabulaires.</span><span class="sxs-lookup"><span data-stu-id="36792-103">The <xref:System.Windows.Forms.DataGridView> control and its related classes are designed to be a flexible, extensible system for displaying and editing tabular data.</span></span> <span data-ttu-id="36792-104">Ces classes sont toutes contenues dans le <xref:System.Windows.Forms?displayProperty=nameWithType> espace de noms et elles portent toutes le préfixe « DataGridView ».</span><span class="sxs-lookup"><span data-stu-id="36792-104">These classes are all contained in the <xref:System.Windows.Forms?displayProperty=nameWithType> namespace, and they are all named with the "DataGridView" prefix.</span></span>  
  
## <a name="architecture-elements"></a><span data-ttu-id="36792-105">Éléments d'architecture</span><span class="sxs-lookup"><span data-stu-id="36792-105">Architecture Elements</span></span>  
 <span data-ttu-id="36792-106">Le réplica principal <xref:System.Windows.Forms.DataGridView> dérivent des classes auxiliaires <xref:System.Windows.Forms.DataGridViewElement>.</span><span class="sxs-lookup"><span data-stu-id="36792-106">The primary <xref:System.Windows.Forms.DataGridView> companion classes derive from <xref:System.Windows.Forms.DataGridViewElement>.</span></span> <span data-ttu-id="36792-107">Le modèle objet suivant illustre la <xref:System.Windows.Forms.DataGridViewElement> hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="36792-107">The following object model illustrates the <xref:System.Windows.Forms.DataGridViewElement> inheritance hierarchy.</span></span>  
  
 ![Diagramme qui montre la hiérarchie du modèle objet DataGridViewElement.](./media/datagridview-control-architecture-windows-forms/datagridviewelement-object-model.gif)  
  
 <span data-ttu-id="36792-109">Le <xref:System.Windows.Forms.DataGridViewElement> classe fournit une référence au parent <xref:System.Windows.Forms.DataGridView> contrôler et a un <xref:System.Windows.Forms.DataGridViewElement.State%2A> propriété, qui contient une valeur qui représente une combinaison de valeurs à partir de la <xref:System.Windows.Forms.DataGridViewElementStates> énumération.</span><span class="sxs-lookup"><span data-stu-id="36792-109">The <xref:System.Windows.Forms.DataGridViewElement> class provides a reference to the parent <xref:System.Windows.Forms.DataGridView> control and has a <xref:System.Windows.Forms.DataGridViewElement.State%2A> property, which holds a value that represents a combination of values from the <xref:System.Windows.Forms.DataGridViewElementStates> enumeration.</span></span>  
  
 <span data-ttu-id="36792-110">Les sections suivantes décrivent les <xref:System.Windows.Forms.DataGridView> classes plus en détail auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="36792-110">The following sections describe the <xref:System.Windows.Forms.DataGridView> companion classes in more detail.</span></span>  
  
### <a name="datagridviewelementstates"></a><span data-ttu-id="36792-111">DataGridViewElementStates</span><span class="sxs-lookup"><span data-stu-id="36792-111">DataGridViewElementStates</span></span>  
 <span data-ttu-id="36792-112">Le <xref:System.Windows.Forms.DataGridViewElementStates> énumération contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="36792-112">The <xref:System.Windows.Forms.DataGridViewElementStates> enumeration contains the following values:</span></span>  
  
-   <xref:System.Windows.Forms.DataGridViewElementStates.None>  
  
-   <xref:System.Windows.Forms.DataGridViewElementStates.Frozen>  
  
-   <xref:System.Windows.Forms.DataGridViewElementStates.ReadOnly>  
  
-   <xref:System.Windows.Forms.DataGridViewElementStates.Resizable>  
  
-   <xref:System.Windows.Forms.DataGridViewElementStates.ResizableSet>  
  
-   <xref:System.Windows.Forms.DataGridViewElementStates.Selected>  
  
-   <xref:System.Windows.Forms.DataGridViewElementStates.Visible>  
  
 <span data-ttu-id="36792-113">Les valeurs de cette énumération peuvent être combinées avec les opérateurs logiques au niveau du bit, donc le <xref:System.Windows.Forms.DataGridViewElement.State%2A> propriété peut exprimer plusieurs États en même temps.</span><span class="sxs-lookup"><span data-stu-id="36792-113">The values of this enumeration can be combined with the bitwise logical operators, so the <xref:System.Windows.Forms.DataGridViewElement.State%2A> property can express more than one state at once.</span></span> <span data-ttu-id="36792-114">Par exemple, un <xref:System.Windows.Forms.DataGridViewElement> peuvent être simultanément <xref:System.Windows.Forms.DataGridViewElementStates.Frozen>, <xref:System.Windows.Forms.DataGridViewElementStates.Selected>, et <xref:System.Windows.Forms.DataGridViewElementStates.Visible>.</span><span class="sxs-lookup"><span data-stu-id="36792-114">For example, a <xref:System.Windows.Forms.DataGridViewElement> can be simultaneously <xref:System.Windows.Forms.DataGridViewElementStates.Frozen>, <xref:System.Windows.Forms.DataGridViewElementStates.Selected>, and <xref:System.Windows.Forms.DataGridViewElementStates.Visible>.</span></span>  
  
### <a name="cells-and-bands"></a><span data-ttu-id="36792-115">Cellules et les bandes</span><span class="sxs-lookup"><span data-stu-id="36792-115">Cells and Bands</span></span>  
 <span data-ttu-id="36792-116">Le <xref:System.Windows.Forms.DataGridView> contrôle comprend deux types d’objets fondamentaux : cellules et les bandes.</span><span class="sxs-lookup"><span data-stu-id="36792-116">The <xref:System.Windows.Forms.DataGridView> control comprises two fundamental kinds of objects: cells and bands.</span></span> <span data-ttu-id="36792-117">Toutes les cellules dérivent la <xref:System.Windows.Forms.DataGridViewCell> classe de base.</span><span class="sxs-lookup"><span data-stu-id="36792-117">All cells derive from the <xref:System.Windows.Forms.DataGridViewCell> base class.</span></span> <span data-ttu-id="36792-118">Les deux types des bandes, <xref:System.Windows.Forms.DataGridViewColumn> et <xref:System.Windows.Forms.DataGridViewRow>, tous deux sont dérivés de la <xref:System.Windows.Forms.DataGridViewBand> classe de base.</span><span class="sxs-lookup"><span data-stu-id="36792-118">The two kinds of bands, <xref:System.Windows.Forms.DataGridViewColumn> and <xref:System.Windows.Forms.DataGridViewRow>, both derive from the <xref:System.Windows.Forms.DataGridViewBand> base class.</span></span>  
  
 <span data-ttu-id="36792-119">Le <xref:System.Windows.Forms.DataGridView> contrôle interagit avec plusieurs classes, mais sont les plus couramment rencontrés <xref:System.Windows.Forms.DataGridViewCell>, <xref:System.Windows.Forms.DataGridViewColumn>, et <xref:System.Windows.Forms.DataGridViewRow>.</span><span class="sxs-lookup"><span data-stu-id="36792-119">The <xref:System.Windows.Forms.DataGridView> control interoperates with several classes, but the most commonly encountered are <xref:System.Windows.Forms.DataGridViewCell>, <xref:System.Windows.Forms.DataGridViewColumn>, and <xref:System.Windows.Forms.DataGridViewRow>.</span></span>  
  
### <a name="datagridviewcell"></a><span data-ttu-id="36792-120">DataGridViewCell</span><span class="sxs-lookup"><span data-stu-id="36792-120">DataGridViewCell</span></span>  
 <span data-ttu-id="36792-121">La cellule est l’unité fondamentale d’interaction pour le <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="36792-121">The cell is the fundamental unit of interaction for the <xref:System.Windows.Forms.DataGridView>.</span></span> <span data-ttu-id="36792-122">Affichage est centré sur les cellules et saisie de données est souvent effectuée via les cellules.</span><span class="sxs-lookup"><span data-stu-id="36792-122">Display is centered on cells, and data entry is often performed through cells.</span></span> <span data-ttu-id="36792-123">Vous pouvez accéder à des cellules à l’aide de la <xref:System.Windows.Forms.DataGridViewRow.Cells%2A> collection de la <xref:System.Windows.Forms.DataGridViewRow> classe et vous pouvez accéder les cellules sélectionnées à l’aide de la <xref:System.Windows.Forms.DataGridView.SelectedCells%2A> collection de la <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="36792-123">You can access cells by using the <xref:System.Windows.Forms.DataGridViewRow.Cells%2A> collection of the <xref:System.Windows.Forms.DataGridViewRow> class, and you can access the selected cells by using the <xref:System.Windows.Forms.DataGridView.SelectedCells%2A> collection of the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="36792-124">Le modèle objet suivant illustre cette utilisation et montre la <xref:System.Windows.Forms.DataGridViewCell> hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="36792-124">The following object model illustrates this usage and shows the <xref:System.Windows.Forms.DataGridViewCell> inheritance hierarchy.</span></span>  
  
 ![Diagramme qui montre la hiérarchie du modèle objet DataGridViewCell.](./media/datagridview-control-architecture-windows-forms/datagridviewcell-object-model.gif)  
  
 <span data-ttu-id="36792-126">Le <xref:System.Windows.Forms.DataGridViewCell> type est une classe de base abstraite dont dérivent tous les types de cellule.</span><span class="sxs-lookup"><span data-stu-id="36792-126">The <xref:System.Windows.Forms.DataGridViewCell> type is an abstract base class, from which all cell types derive.</span></span> <span data-ttu-id="36792-127"><xref:System.Windows.Forms.DataGridViewCell> et ses types dérivés ne sont pas des contrôles Windows Forms, mais certains contrôles de Windows Forms hôtes.</span><span class="sxs-lookup"><span data-stu-id="36792-127"><xref:System.Windows.Forms.DataGridViewCell> and its derived types are not Windows Forms controls, but some host Windows Forms controls.</span></span> <span data-ttu-id="36792-128">Toute fonctionnalité d’édition pris en charge par une cellule est généralement gérée par un contrôle hébergé.</span><span class="sxs-lookup"><span data-stu-id="36792-128">Any editing functionality supported by a cell is typically handled by a hosted control.</span></span>  
  
 <span data-ttu-id="36792-129"><xref:System.Windows.Forms.DataGridViewCell> objets ne contrôlent pas de leur propre apparence et les fonctionnalités de peinture de la même façon que les contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="36792-129"><xref:System.Windows.Forms.DataGridViewCell> objects do not control their own appearance and painting features in the same way as Windows Forms controls.</span></span> <span data-ttu-id="36792-130">Au lieu de cela, le <xref:System.Windows.Forms.DataGridView> est responsable de l’apparence de son <xref:System.Windows.Forms.DataGridViewCell> objets.</span><span class="sxs-lookup"><span data-stu-id="36792-130">Instead, the <xref:System.Windows.Forms.DataGridView> is responsible for the appearance of its <xref:System.Windows.Forms.DataGridViewCell> objects.</span></span> <span data-ttu-id="36792-131">Vous pouvez affecter de manière significative l’apparence et le comportement des cellules en interagissant avec le <xref:System.Windows.Forms.DataGridView> événements et les propriétés du contrôle.</span><span class="sxs-lookup"><span data-stu-id="36792-131">You can significantly affect the appearance and behavior of cells by interacting with the <xref:System.Windows.Forms.DataGridView> control's properties and events.</span></span> <span data-ttu-id="36792-132">Lorsque vous avez des exigences particulières pour les personnalisations qui ne sont pas les fonctionnalités de la <xref:System.Windows.Forms.DataGridView> contrôle, vous pouvez implémenter votre propre classe qui dérive de <xref:System.Windows.Forms.DataGridViewCell> ou une de ses classes enfants.</span><span class="sxs-lookup"><span data-stu-id="36792-132">When you have special requirements for customizations that are beyond the capabilities of the <xref:System.Windows.Forms.DataGridView> control, you can implement your own class that derives from <xref:System.Windows.Forms.DataGridViewCell> or one of its child classes.</span></span>  
  
 <span data-ttu-id="36792-133">La liste suivante présente les classes dérivées de <xref:System.Windows.Forms.DataGridViewCell>:</span><span class="sxs-lookup"><span data-stu-id="36792-133">The following list shows the classes derived from <xref:System.Windows.Forms.DataGridViewCell>:</span></span>  
  
-   <xref:System.Windows.Forms.DataGridViewTextBoxCell>  
  
-   <xref:System.Windows.Forms.DataGridViewButtonCell>  
  
-   <xref:System.Windows.Forms.DataGridViewLinkCell>  
  
-   <xref:System.Windows.Forms.DataGridViewCheckBoxCell>  
  
-   <xref:System.Windows.Forms.DataGridViewComboBoxCell>  
  
-   <xref:System.Windows.Forms.DataGridViewImageCell>  
  
-   <xref:System.Windows.Forms.DataGridViewHeaderCell>  
  
-   <xref:System.Windows.Forms.DataGridViewRowHeaderCell>  
  
-   <xref:System.Windows.Forms.DataGridViewColumnHeaderCell>  
  
-   <xref:System.Windows.Forms.DataGridViewTopLeftHeaderCell>  
  
-   <span data-ttu-id="36792-134">Vos types de cellule personnalisée</span><span class="sxs-lookup"><span data-stu-id="36792-134">Your custom cell types</span></span>  
  
### <a name="datagridviewcolumn"></a><span data-ttu-id="36792-135">DataGridViewColumn</span><span class="sxs-lookup"><span data-stu-id="36792-135">DataGridViewColumn</span></span>  
 <span data-ttu-id="36792-136">Le schéma de la <xref:System.Windows.Forms.DataGridView> magasin de données attaché du contrôle est exprimée dans le <xref:System.Windows.Forms.DataGridView> les colonnes du contrôle.</span><span class="sxs-lookup"><span data-stu-id="36792-136">The schema of the <xref:System.Windows.Forms.DataGridView> control's attached data store is expressed in the <xref:System.Windows.Forms.DataGridView> control's columns.</span></span> <span data-ttu-id="36792-137">Vous pouvez accéder à la <xref:System.Windows.Forms.DataGridView> les colonnes du contrôle à l’aide de la <xref:System.Windows.Forms.DataGridView.Columns%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="36792-137">You can access the <xref:System.Windows.Forms.DataGridView> control's columns by using the <xref:System.Windows.Forms.DataGridView.Columns%2A> collection.</span></span> <span data-ttu-id="36792-138">Vous pouvez accéder à des colonnes sélectionnées à l’aide de la <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="36792-138">You can access the selected columns by using the <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A> collection.</span></span> <span data-ttu-id="36792-139">Le modèle objet suivant illustre cette utilisation et montre la <xref:System.Windows.Forms.DataGridViewColumn> hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="36792-139">The following object model illustrates this usage and shows the <xref:System.Windows.Forms.DataGridViewColumn> inheritance hierarchy.</span></span>  
  
 ![Diagramme qui montre la hiérarchie du modèle objet DataGridViewColumn.](./media/datagridview-control-architecture-windows-forms/datagridviewcolumn-object-model.gif)  
  
 <span data-ttu-id="36792-141">Certains des types de cellule clés ont des types de colonne correspondants.</span><span class="sxs-lookup"><span data-stu-id="36792-141">Some of the key cell types have corresponding column types.</span></span> <span data-ttu-id="36792-142">Ils sont dérivés de la <xref:System.Windows.Forms.DataGridViewColumn> classe de base.</span><span class="sxs-lookup"><span data-stu-id="36792-142">These are derived from the <xref:System.Windows.Forms.DataGridViewColumn> base class.</span></span>  
  
 <span data-ttu-id="36792-143">La liste suivante présente les classes dérivées de <xref:System.Windows.Forms.DataGridViewColumn>:</span><span class="sxs-lookup"><span data-stu-id="36792-143">The following list shows the classes derived from <xref:System.Windows.Forms.DataGridViewColumn>:</span></span>  
  
-   <xref:System.Windows.Forms.DataGridViewButtonColumn>  
  
-   <xref:System.Windows.Forms.DataGridViewCheckBoxColumn>  
  
-   <xref:System.Windows.Forms.DataGridViewComboBoxColumn>  
  
-   <xref:System.Windows.Forms.DataGridViewImageColumn>  
  
-   <xref:System.Windows.Forms.DataGridViewTextBoxColumn>  
  
-   <xref:System.Windows.Forms.DataGridViewLinkColumn>  
  
-   <span data-ttu-id="36792-144">Vos types de colonnes personnalisées</span><span class="sxs-lookup"><span data-stu-id="36792-144">Your custom column types</span></span>  
  
### <a name="datagridview-editing-controls"></a><span data-ttu-id="36792-145">Contrôles d’édition DataGridView</span><span class="sxs-lookup"><span data-stu-id="36792-145">DataGridView Editing Controls</span></span>  
 <span data-ttu-id="36792-146">Cellules qui prennent en charge la fonctionnalité d’édition avancée généralement utilisent un contrôle hébergé qui est dérivé d’un contrôle Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="36792-146">Cells that support advanced editing functionality typically use a hosted control that is derived from a Windows Forms control.</span></span> <span data-ttu-id="36792-147">Ces contrôles implémentent également le <xref:System.Windows.Forms.IDataGridViewEditingControl> interface.</span><span class="sxs-lookup"><span data-stu-id="36792-147">These controls also implement the <xref:System.Windows.Forms.IDataGridViewEditingControl> interface.</span></span> <span data-ttu-id="36792-148">Le modèle objet suivant illustre l’utilisation de ces contrôles.</span><span class="sxs-lookup"><span data-stu-id="36792-148">The following object model illustrates the usage of these controls.</span></span>  
  
 ![Diagramme affichant la hiérarchie du modèle d’objet de contrôle d’édition DataGridView.](./media/datagridview-control-architecture-windows-forms/datagridviewediting-object-model.gif)  
  
 <span data-ttu-id="36792-150">Les contrôles d’éditions suivants sont fournis avec le <xref:System.Windows.Forms.DataGridView> contrôle :</span><span class="sxs-lookup"><span data-stu-id="36792-150">The following editing controls are provided with the <xref:System.Windows.Forms.DataGridView> control:</span></span>  
  
-   <xref:System.Windows.Forms.DataGridViewComboBoxEditingControl>  
  
-   <xref:System.Windows.Forms.DataGridViewTextBoxEditingControl>  
  
 <span data-ttu-id="36792-151">Pour plus d’informations sur la création de vos propres modification des contrôles, consultez [Comment : Héberger des contrôles dans les Windows Forms cellules DataGridView](how-to-host-controls-in-windows-forms-datagridview-cells.md).</span><span class="sxs-lookup"><span data-stu-id="36792-151">For information about creating your own editing controls, see [How to: Host Controls in Windows Forms DataGridView Cells](how-to-host-controls-in-windows-forms-datagridview-cells.md).</span></span>  
  
 <span data-ttu-id="36792-152">Le tableau suivant illustre la relation entre les types de cellules, les types de colonnes et les contrôles d’édition.</span><span class="sxs-lookup"><span data-stu-id="36792-152">The following table illustrates the relationship among cell types, column types, and editing controls.</span></span>  
  
|<span data-ttu-id="36792-153">Type de cellule</span><span class="sxs-lookup"><span data-stu-id="36792-153">Cell type</span></span>|<span data-ttu-id="36792-154">Contrôle hébergé</span><span class="sxs-lookup"><span data-stu-id="36792-154">Hosted control</span></span>|<span data-ttu-id="36792-155">Type de colonne</span><span class="sxs-lookup"><span data-stu-id="36792-155">Column type</span></span>|  
|---------------|--------------------|-----------------|  
|<xref:System.Windows.Forms.DataGridViewButtonCell>|<span data-ttu-id="36792-156">N/A</span><span class="sxs-lookup"><span data-stu-id="36792-156">n/a</span></span>|<xref:System.Windows.Forms.DataGridViewButtonColumn>|  
|<xref:System.Windows.Forms.DataGridViewCheckBoxCell>|<span data-ttu-id="36792-157">N/A</span><span class="sxs-lookup"><span data-stu-id="36792-157">n/a</span></span>|<xref:System.Windows.Forms.DataGridViewCheckBoxColumn>|  
|<xref:System.Windows.Forms.DataGridViewComboBoxCell>|<xref:System.Windows.Forms.DataGridViewComboBoxEditingControl>|<xref:System.Windows.Forms.DataGridViewComboBoxColumn>|  
|<xref:System.Windows.Forms.DataGridViewImageCell>|<span data-ttu-id="36792-158">N/A</span><span class="sxs-lookup"><span data-stu-id="36792-158">n/a</span></span>|<xref:System.Windows.Forms.DataGridViewImageColumn>|  
|<xref:System.Windows.Forms.DataGridViewLinkCell>|<span data-ttu-id="36792-159">N/A</span><span class="sxs-lookup"><span data-stu-id="36792-159">n/a</span></span>|<xref:System.Windows.Forms.DataGridViewLinkColumn>|  
|<xref:System.Windows.Forms.DataGridViewTextBoxCell>|<xref:System.Windows.Forms.DataGridViewTextBoxEditingControl>|<xref:System.Windows.Forms.DataGridViewTextBoxColumn>|  
  
### <a name="datagridviewrow"></a><span data-ttu-id="36792-160">DataGridViewRow</span><span class="sxs-lookup"><span data-stu-id="36792-160">DataGridViewRow</span></span>  
 <span data-ttu-id="36792-161">Le <xref:System.Windows.Forms.DataGridViewRow> affiche classe les données d’un enregistrement des champs à partir des données de magasin auquel le <xref:System.Windows.Forms.DataGridView> contrôle est attaché.</span><span class="sxs-lookup"><span data-stu-id="36792-161">The <xref:System.Windows.Forms.DataGridViewRow> class displays a record's data fields from the data store to which the <xref:System.Windows.Forms.DataGridView> control is attached.</span></span> <span data-ttu-id="36792-162">Vous pouvez accéder à la <xref:System.Windows.Forms.DataGridView> lignes du contrôle à l’aide de la <xref:System.Windows.Forms.DataGridView.Rows%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="36792-162">You can access the <xref:System.Windows.Forms.DataGridView> control's rows by using the <xref:System.Windows.Forms.DataGridView.Rows%2A> collection.</span></span> <span data-ttu-id="36792-163">Vous pouvez accéder à des lignes sélectionnées à l’aide de la <xref:System.Windows.Forms.DataGridView.SelectedRows%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="36792-163">You can access the selected rows by using the <xref:System.Windows.Forms.DataGridView.SelectedRows%2A> collection.</span></span> <span data-ttu-id="36792-164">Le modèle objet suivant illustre cette utilisation et montre la <xref:System.Windows.Forms.DataGridViewRow> hiérarchie d’héritage.</span><span class="sxs-lookup"><span data-stu-id="36792-164">The following object model illustrates this usage and shows the <xref:System.Windows.Forms.DataGridViewRow> inheritance hierarchy.</span></span>  
  
 ![Diagramme qui montre la hiérarchie du modèle objet DataGridViewRow.](./media/datagridview-control-architecture-windows-forms/datagridviewrow-object-model.gif)
  
 <span data-ttu-id="36792-166">Vous pouvez dériver vos propres types à partir de la <xref:System.Windows.Forms.DataGridViewRow> classe, bien que cela ne soit généralement pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="36792-166">You can derive your own types from the <xref:System.Windows.Forms.DataGridViewRow> class, although this will typically not be necessary.</span></span> <span data-ttu-id="36792-167">Le <xref:System.Windows.Forms.DataGridView> contrôle a plusieurs événements liés à la ligne et propriétés pour personnaliser le comportement de ses <xref:System.Windows.Forms.DataGridViewRow> objets.</span><span class="sxs-lookup"><span data-stu-id="36792-167">The <xref:System.Windows.Forms.DataGridView> control has several row-related events and properties for customizing the behavior of its <xref:System.Windows.Forms.DataGridViewRow> objects.</span></span>  
  
 <span data-ttu-id="36792-168">Si vous activez le <xref:System.Windows.Forms.DataGridView> du contrôle <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> propriété, une ligne spéciale pour l’ajout de nouvelles lignes apparaît en tant que la dernière ligne.</span><span class="sxs-lookup"><span data-stu-id="36792-168">If you enable the <xref:System.Windows.Forms.DataGridView> control's <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> property, a special row for adding new rows appears as the last row.</span></span> <span data-ttu-id="36792-169">Cette ligne fait partie de la <xref:System.Windows.Forms.DataGridView.Rows%2A> collection, mais il possède des fonctionnalités spéciales qui peuvent nécessiter votre attention.</span><span class="sxs-lookup"><span data-stu-id="36792-169">This row is part of the <xref:System.Windows.Forms.DataGridView.Rows%2A> collection, but it has special functionality that may require your attention.</span></span> <span data-ttu-id="36792-170">Pour plus d’informations, consultez [à l’aide de la ligne pour les nouveaux enregistrements dans le contrôle de DataGridView Windows Forms](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="36792-170">For more information, see [Using the Row for New Records in the Windows Forms DataGridView Control](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="36792-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36792-171">See also</span></span>

- [<span data-ttu-id="36792-172">Vue d’ensemble du contrôle DataGridView</span><span class="sxs-lookup"><span data-stu-id="36792-172">DataGridView Control Overview</span></span>](datagridview-control-overview-windows-forms.md)
- [<span data-ttu-id="36792-173">Personnalisation du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="36792-173">Customizing the Windows Forms DataGridView Control</span></span>](customizing-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="36792-174">Utilisation de la ligne pour les nouveaux enregistrements dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="36792-174">Using the Row for New Records in the Windows Forms DataGridView Control</span></span>](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)
