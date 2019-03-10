---
title: Affichage des données dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- data [Windows Forms], displaying in tabular format
- data grids [Windows Forms], displaying data
- displaying data [Windows Forms], data grids
- DataGridView control [Windows Forms], displaying data
ms.assetid: b170b52a-2ebd-4948-ac2f-e52d494cebb2
ms.openlocfilehash: d35fd2d17ce8d1b3c4759da1bab2370c450d2fbf
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703264"
---
# <a name="displaying-data-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="77170-102">Affichage des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-102">Displaying Data in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="77170-103">Le `DataGridView` contrôle est utilisé pour afficher des données à partir de diverses sources de données externes.</span><span class="sxs-lookup"><span data-stu-id="77170-103">The `DataGridView` control is used to display data from a variety of external data sources.</span></span> <span data-ttu-id="77170-104">Vous pouvez également ajouter des lignes et des colonnes au contrôle et manuellement le remplir avec des données.</span><span class="sxs-lookup"><span data-stu-id="77170-104">Alternatively, you can add rows and columns to the control and manually populate it with data.</span></span>  
  
 <span data-ttu-id="77170-105">Lorsque vous liez le contrôle à une source de données, vous pouvez générer des colonnes automatiquement en fonction du schéma de la source de données.</span><span class="sxs-lookup"><span data-stu-id="77170-105">When you bind the control to a data source, you can generate columns automatically based on the schema of the data source.</span></span> <span data-ttu-id="77170-106">Si ces colonnes n’apparaissent pas comme vous le souhaitez, vous pouvez masquer, supprimer ou les réorganiser.</span><span class="sxs-lookup"><span data-stu-id="77170-106">If these columns do not appear just as you want them to, you can hide, remove, or rearrange them.</span></span> <span data-ttu-id="77170-107">Vous pouvez également ajouter des colonnes indépendantes pour afficher des données supplémentaires qui ne provient pas de la source de données.</span><span class="sxs-lookup"><span data-stu-id="77170-107">You can also add unbound columns to display supplemental data that does not come from the data source.</span></span>  
  
 <span data-ttu-id="77170-108">En outre, vous pouvez afficher vos données à l’aide de formats standard (par exemple, le format de devise), ou vous pouvez personnaliser l’affichage pour présenter vos données, toutefois, vous devez (par exemple, la couleur d’arrière-plan pour les nombres négatifs, ou en remplaçant les valeurs de chaîne de mise en forme avec les images correspondantes).</span><span class="sxs-lookup"><span data-stu-id="77170-108">Additionally, you can display your data using standard formats (such as currency format), or you can customize the display formatting to present your data however you need to (such as changing the background color for negative numbers, or replacing string values with corresponding images).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="77170-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="77170-109">In This Section</span></span>  
 [<span data-ttu-id="77170-110">Modes d’affichage des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-110">Data Display Modes in the Windows Forms DataGridView Control</span></span>](data-display-modes-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="77170-111">Décrit les options pour remplir le contrôle de données.</span><span class="sxs-lookup"><span data-stu-id="77170-111">Describes the options for populating the control with data.</span></span>  
  
 [<span data-ttu-id="77170-112">Mise en forme de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-112">Data Formatting in the Windows Forms DataGridView Control</span></span>](data-formatting-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="77170-113">Décrit les options de mise en forme des valeurs d’affichage de cellule.</span><span class="sxs-lookup"><span data-stu-id="77170-113">Describes the options for formatting cell display values.</span></span>  
  
 [<span data-ttu-id="77170-114">Procédure pas à pas : Création d’un indépendant Windows Forms DataGridView Control</span><span class="sxs-lookup"><span data-stu-id="77170-114">Walkthrough: Creating an Unbound Windows Forms DataGridView Control</span></span>](walkthrough-creating-an-unbound-windows-forms-datagridview-control.md)  
 <span data-ttu-id="77170-115">Décrit comment remplir manuellement le contrôle de données.</span><span class="sxs-lookup"><span data-stu-id="77170-115">Describes how to manually populate the control with data.</span></span>  
  
 [<span data-ttu-id="77170-116">Guide pratique pour Lier des données au contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-116">How to: Bind Data to the Windows Forms DataGridView Control</span></span>](how-to-bind-data-to-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="77170-117">Explique comment remplir le contrôle de données en le liant à un `BindingSource` qui contient des informations extraites d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="77170-117">Describes how to populate the control with data by binding it to a `BindingSource` that contains information pulled from a database.</span></span>  
  
 [<span data-ttu-id="77170-118">Guide pratique pour Générer automatiquement des colonnes dans un contrôle de DataGridView lié aux données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-118">How to: Autogenerate Columns in a Data-Bound Windows Forms DataGridView Control</span></span>](autogenerate-columns-in-a-data-bound-wf-datagridview-control.md)  
 <span data-ttu-id="77170-119">Décrit comment générer automatiquement des colonnes basées sur une source de données liée.</span><span class="sxs-lookup"><span data-stu-id="77170-119">Describes how to automatically generate columns based on a bound data source.</span></span>  
  
 [<span data-ttu-id="77170-120">Guide pratique pour Supprimer les colonnes générées automatiquement à partir d’un contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-120">How to: Remove Autogenerated Columns from a Windows Forms DataGridView Control</span></span>](remove-autogenerated-columns-from-a-wf-datagridview-control.md)  
 <span data-ttu-id="77170-121">Décrit comment masquer ou supprimer des colonnes générées automatiquement à partir d’une source de données liée.</span><span class="sxs-lookup"><span data-stu-id="77170-121">Describes how to hide or delete columns generated automatically from a bound data source.</span></span>  
  
 [<span data-ttu-id="77170-122">Guide pratique pour Modifier l’ordre des colonnes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-122">How to: Change the Order of Columns in the Windows Forms DataGridView Control</span></span>](how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="77170-123">Décrit comment réorganiser les colonnes générées automatiquement à partir d’une source de données liée.</span><span class="sxs-lookup"><span data-stu-id="77170-123">Describes how to rearrange columns generated automatically from a bound data source.</span></span>  
  
 [<span data-ttu-id="77170-124">Guide pratique pour Ajouter une colonne indépendante à un contrôle de DataGridView lié aux données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-124">How to: Add an Unbound Column to a Data-Bound Windows Forms DataGridView Control</span></span>](unbound-column-to-a-data-bound-datagridview.md)  
 <span data-ttu-id="77170-125">Décrit comment compléter les données à partir d’une source de données liée en affichant des colonnes supplémentaires non liées.</span><span class="sxs-lookup"><span data-stu-id="77170-125">Describes how to supplement data from a bound data source by displaying additional, unbound columns.</span></span>  
  
 [<span data-ttu-id="77170-126">Guide pratique pour Lier des objets aux contrôles DataGridView de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-126">How to: Bind Objects to Windows Forms DataGridView Controls</span></span>](how-to-bind-objects-to-windows-forms-datagridview-controls.md)  
 <span data-ttu-id="77170-127">Décrit comment lier le contrôle à une collection d’objets arbitraires afin que chaque objet s’affiche dans sa propre ligne.</span><span class="sxs-lookup"><span data-stu-id="77170-127">Describes how to bind the control to a collection of arbitrary objects so that each object is displayed in its own row.</span></span>  
  
 [<span data-ttu-id="77170-128">Guide pratique pour Accéder aux objets liés à des Windows Forms DataGridView lignes</span><span class="sxs-lookup"><span data-stu-id="77170-128">How to: Access Objects Bound to Windows Forms DataGridView Rows</span></span>](how-to-access-objects-bound-to-windows-forms-datagridview-rows.md)  
 <span data-ttu-id="77170-129">Décrit comment récupérer un objet lié à une ligne particulière du contrôle.</span><span class="sxs-lookup"><span data-stu-id="77170-129">Describes how to retrieve an object bound to a particular row of the control.</span></span>  
  
 [<span data-ttu-id="77170-130">Procédure pas à pas : Création d’un formulaire maître/détail utilisant deux contrôles de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-130">Walkthrough: Creating a Master/Detail Form Using Two Windows Forms DataGridView Controls</span></span>](creating-a-master-detail-form-using-two-datagridviews.md)  
 <span data-ttu-id="77170-131">Décrit comment afficher des données à partir de deux tables de base de données associée afin que les valeurs indiquées dans un `DataGridView` contrôle dépendent de la ligne actuellement sélectionnée dans un autre contrôle.</span><span class="sxs-lookup"><span data-stu-id="77170-131">Describes how to display data from two related database tables so that the values shown in one `DataGridView` control depend on the currently selected row in another control.</span></span>  
  
 [<span data-ttu-id="77170-132">Guide pratique pour Personnaliser la mise en forme des données dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-132">How to: Customize Data Formatting in the Windows Forms DataGridView Control</span></span>](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="77170-133">Décrit comment gérer les <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> pour modifier l’apparence des cellules en fonction de leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="77170-133">Describes how to handle the <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> event to change the appearance of cells depending on their values.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="77170-134">Référence</span><span class="sxs-lookup"><span data-stu-id="77170-134">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="77170-135">Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="77170-135">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.DataSource%2A?displayProperty=nameWithType>  
 <span data-ttu-id="77170-136">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="77170-136">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.DataSource%2A> property.</span></span>  
  
 <xref:System.Windows.Forms.BindingSource>  
 <span data-ttu-id="77170-137">Fournit la documentation de référence pour le composant <xref:System.Windows.Forms.BindingSource>.</span><span class="sxs-lookup"><span data-stu-id="77170-137">Provides reference documentation for the <xref:System.Windows.Forms.BindingSource> component.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="77170-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77170-138">Related Sections</span></span>  
 [<span data-ttu-id="77170-139">Saisie de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-139">Data Entry in the Windows Forms DataGridView Control</span></span>](data-entry-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="77170-140">Fournit des rubriques qui décrivent comment modifier la façon dont les utilisateurs ajoutent et modifient des données dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="77170-140">Provides topics that describe how to change the way users add and modify data in the control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77170-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77170-141">See also</span></span>
- [<span data-ttu-id="77170-142">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="77170-142">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
- [<span data-ttu-id="77170-143">Types de colonnes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77170-143">Column Types in the Windows Forms DataGridView Control</span></span>](column-types-in-the-windows-forms-datagridview-control.md)
