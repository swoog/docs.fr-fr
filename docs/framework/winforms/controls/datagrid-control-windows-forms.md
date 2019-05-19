---
title: DataGrid, contrôle (Windows Forms)
ms.date: 03/30/2017
helpviewer_keywords:
- datasets [Windows Forms], user interface
- DataGrid control [Windows Forms]
- datasets [Windows Forms], displaying in DataGrid control
- displaying data [Windows Forms], on forms
- data [Windows Forms], displaying on Windows Forms
ms.assetid: 1d9d5683-43d2-42dd-b6c3-e43f4cf0de99
ms.openlocfilehash: 5a69605901eef7366c7a9ff9930e5f4ec6cece23
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65878771"
---
# <a name="datagrid-control-windows-forms"></a><span data-ttu-id="77c80-102">DataGrid, contrôle (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="77c80-102">DataGrid Control (Windows Forms)</span></span>
> [!NOTE]
>  <span data-ttu-id="77c80-103">Le contrôle <xref:System.Windows.Forms.DataGridView> remplace le contrôle `DataGrid` et lui ajoute des fonctionnalités ; toutefois, le contrôle `DataGrid` est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.</span><span class="sxs-lookup"><span data-stu-id="77c80-103">The <xref:System.Windows.Forms.DataGridView> control replaces and adds functionality to the `DataGrid` control; however, the `DataGrid` control is retained for both backward compatibility and future use, if you choose.</span></span> <span data-ttu-id="77c80-104">Pour plus d’informations, consultez [Différences entre les contrôles DataGridView et DataGrid Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span><span class="sxs-lookup"><span data-stu-id="77c80-104">For more information, see [Differences Between the Windows Forms DataGridView and DataGrid Controls](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span></span>  
  
 <span data-ttu-id="77c80-105">Les formulaires Windows `DataGrid` contrôle fournit une interface utilisateur pour les jeux de données ADO.NET, affichant les données tabulaires et permettant les mises à jour de la source de données.</span><span class="sxs-lookup"><span data-stu-id="77c80-105">The Windows Forms `DataGrid` control provides a user interface to ADO.NET datasets, displaying tabular data and enabling updates to the data source.</span></span>  
  
 <span data-ttu-id="77c80-106">Quand le contrôle `DataGrid` est défini sur une source de données valide, il est automatiquement rempli, et des colonnes et des lignes sont créées en fonction de la forme des données.</span><span class="sxs-lookup"><span data-stu-id="77c80-106">When the `DataGrid` control is set to a valid data source, the control is automatically populated, creating columns and rows based on the shape of the data.</span></span> <span data-ttu-id="77c80-107">Le contrôle `DataGrid` peut être utilisé pour afficher une seule table ou les relations hiérarchiques entre un ensemble de tables.</span><span class="sxs-lookup"><span data-stu-id="77c80-107">The `DataGrid` control can be used to display either a single table or the hierarchical relationships between a set of tables.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="77c80-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="77c80-108">In This Section</span></span>  
 [<span data-ttu-id="77c80-109">Vue d’ensemble du contrôle DataGrid</span><span class="sxs-lookup"><span data-stu-id="77c80-109">DataGrid Control Overview</span></span>](datagrid-control-overview-windows-forms.md)  
 <span data-ttu-id="77c80-110">Décrit les fonctionnalités de base du contrôle `DataGrid`.</span><span class="sxs-lookup"><span data-stu-id="77c80-110">Describes the basic features of the `DataGrid` control.</span></span>  
  
 [<span data-ttu-id="77c80-111">Guide pratique pour Ajouter des Tables et des colonnes au contrôle DataGrid Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="77c80-111">How to: Add Tables and Columns to the Windows Forms DataGrid Control Using the Designer</span></span>](add-tables-and-columns-to-wf-datagrid-control-using-the-designer.md)  
 <span data-ttu-id="77c80-112">Décrit comment ajouter des tables et des colonnes au contrôle `DataGrid` à l’aide du concepteur.</span><span class="sxs-lookup"><span data-stu-id="77c80-112">Describes how to add tables and columns to the `DataGrid` control using the designer.</span></span>  
  
 [<span data-ttu-id="77c80-113">Guide pratique pour Ajouter des Tables et des colonnes au contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-113">How to: Add Tables and Columns to the Windows Forms DataGrid Control</span></span>](how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control.md)  
 <span data-ttu-id="77c80-114">Décrit comment ajouter des tables et des colonnes au contrôle `DataGrid` par programmation.</span><span class="sxs-lookup"><span data-stu-id="77c80-114">Describes how to add tables and columns to the `DataGrid` control programmatically.</span></span>  
  
 [<span data-ttu-id="77c80-115">Guide pratique pour Lier le contrôle DataGrid Windows Forms à une Source de données à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="77c80-115">How to: Bind the Windows Forms DataGrid Control to a Data Source Using the Designer</span></span>](bind-wf-datagrid-control-to-a-data-source-using-the-designer.md)  
 <span data-ttu-id="77c80-116">Décrit comment lier un dataset ADO.NET à la `DataGrid` contrôler à l’aide du concepteur.</span><span class="sxs-lookup"><span data-stu-id="77c80-116">Describes how to bind an ADO.NET dataset to the `DataGrid` control using the designer.</span></span>  
  
 [<span data-ttu-id="77c80-117">Guide pratique pour Lier le contrôle DataGrid Windows Forms à une Source de données</span><span class="sxs-lookup"><span data-stu-id="77c80-117">How to: Bind the Windows Forms DataGrid Control to a Data Source</span></span>](how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md)  
 <span data-ttu-id="77c80-118">Décrit comment lier un dataset ADO.NET à la `DataGrid` contrôle.</span><span class="sxs-lookup"><span data-stu-id="77c80-118">Describes how to bind an ADO.NET dataset to the `DataGrid` control.</span></span>  
  
 [<span data-ttu-id="77c80-119">Guide pratique pour Modification des données affichées au moment de l’exécution dans le contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-119">How to: Change Displayed Data at Run Time in the Windows Forms DataGrid Control</span></span>](change-displayed-data-at-run-time-wf-datagrid-control.md)  
 <span data-ttu-id="77c80-120">Décrit comment modifier des données par programmation dans le contrôle `DataGrid`.</span><span class="sxs-lookup"><span data-stu-id="77c80-120">Describes how to change data programmatically in the `DataGrid` control.</span></span>  
  
 [<span data-ttu-id="77c80-121">Guide pratique pour Créer des listes maître / détails avec le contrôle de DataGrid Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="77c80-121">How to: Create Master-Details Lists with the Windows Forms DataGrid Control Using the Designer</span></span>](create-master-details-lists-with-wf-datagrid-control-using-the-designer.md)  
 <span data-ttu-id="77c80-122">Décrit comment afficher deux tables liées par une relation parent/enfant, dans deux contrôles `DataGrid` distincts à l’aide du concepteur.</span><span class="sxs-lookup"><span data-stu-id="77c80-122">Describes how to display two tables, tied together with a parent/child relationship, in two separate `DataGrid` controls using the designer.</span></span>  
  
 <span data-ttu-id="77c80-123">Procédure : Créer des listes maître / détails avec le contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-123">How to: Create Master-Details Lists with the Windows Forms DataGrid Control</span></span>  
 <span data-ttu-id="77c80-124">Décrit comment afficher deux tables liées par une relation parent/enfant, dans deux contrôles `DataGrid` distincts.</span><span class="sxs-lookup"><span data-stu-id="77c80-124">Describes how to display two tables, tied together with a parent/child relationship, in two separate `DataGrid` controls.</span></span>  
  
 [<span data-ttu-id="77c80-125">Guide pratique pour Supprimer ou masquer des colonnes dans le contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-125">How to: Delete or Hide Columns in the Windows Forms DataGrid Control</span></span>](how-to-delete-or-hide-columns-in-the-windows-forms-datagrid-control.md)  
 <span data-ttu-id="77c80-126">Décrit comment supprimer des colonnes dans le contrôle `DataGrid`.</span><span class="sxs-lookup"><span data-stu-id="77c80-126">Describes how to remove columns in the `DataGrid` control.</span></span>  
  
 [<span data-ttu-id="77c80-127">Guide pratique pour Mettre en forme le contrôle de DataGrid Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="77c80-127">How to: Format the Windows Forms DataGrid Control Using the Designer</span></span>](how-to-format-the-windows-forms-datagrid-control-using-the-designer.md)  
 <span data-ttu-id="77c80-128">Décrit comment modifier les propriétés relatives à l’apparence du contrôle `DataGrid` à l’aide du concepteur.</span><span class="sxs-lookup"><span data-stu-id="77c80-128">Describes how to change the appearance-related properties of the `DataGrid` control using the designer.</span></span>  
  
 [<span data-ttu-id="77c80-129">Guide pratique pour Mettre en forme le contrôle de DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-129">How to: Format the Windows Forms DataGrid Control</span></span>](how-to-format-the-windows-forms-datagrid-control.md)  
 <span data-ttu-id="77c80-130">Décrit comment modifier les propriétés relatives à l’apparence du contrôle `DataGrid`.</span><span class="sxs-lookup"><span data-stu-id="77c80-130">Describes how to change the appearance-related properties of the `DataGrid` control.</span></span>  
  
 [<span data-ttu-id="77c80-131">Raccourcis clavier du contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-131">Keyboard Shortcuts for the Windows Forms DataGrid Control</span></span>](keyboard-shortcuts-for-the-windows-forms-datagrid-control.md)  
 <span data-ttu-id="77c80-132">Répertorie les raccourcis pour naviguer dans le contrôle `DataGrid`.</span><span class="sxs-lookup"><span data-stu-id="77c80-132">Lists shortcuts for navigating through the `DataGrid` control.</span></span>  
  
 [<span data-ttu-id="77c80-133">Guide pratique pour Répondre aux clics dans le contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-133">How to: Respond to Clicks in the Windows Forms DataGrid Control</span></span>](how-to-respond-to-clicks-in-the-windows-forms-datagrid-control.md)  
 <span data-ttu-id="77c80-134">Décrit comment déterminer sur quelle cellule l’utilisateur a cliqué dans le contrôle `DataGrid`.</span><span class="sxs-lookup"><span data-stu-id="77c80-134">Describes how to determine which cell a user has clicked in the `DataGrid` control.</span></span>  
  
 [<span data-ttu-id="77c80-135">Guide pratique pour Valider les entrées avec le contrôle DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-135">How to: Validate Input with the Windows Forms DataGrid Control</span></span>](how-to-validate-input-with-the-windows-forms-datagrid-control.md)  
 <span data-ttu-id="77c80-136">Décrit comment valider des entrées dans le dataset lié au contrôle `DataGrid`.</span><span class="sxs-lookup"><span data-stu-id="77c80-136">Describes how to validate input in the dataset bound to the `DataGrid` control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="77c80-137">Référence</span><span class="sxs-lookup"><span data-stu-id="77c80-137">Reference</span></span>  
 <xref:System.Windows.Forms.DataGrid>  
 <span data-ttu-id="77c80-138">Fournit une vue d’ensemble de la <xref:System.Windows.Forms.DataGrid> classe.</span><span class="sxs-lookup"><span data-stu-id="77c80-138">Provides an overview of the <xref:System.Windows.Forms.DataGrid> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGrid.DataSource%2A>  
 <span data-ttu-id="77c80-139">Fournit des détails sur l’utilisation de cette propriété pour lier le <xref:System.Windows.Forms.DataGrid> contrôle aux données.</span><span class="sxs-lookup"><span data-stu-id="77c80-139">Provides details about using this property to bind the <xref:System.Windows.Forms.DataGrid> control to data.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="77c80-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77c80-140">Related Sections</span></span>  
 [<span data-ttu-id="77c80-141">Liaison de données Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-141">Windows Forms Data Binding</span></span>](../windows-forms-data-binding.md)  
 <span data-ttu-id="77c80-142">Fournit des liens vers des rubriques sur la liaison de données dans les Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="77c80-142">Provides links to topics on data binding in Windows Forms.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77c80-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77c80-143">See also</span></span>

- [<span data-ttu-id="77c80-144">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="77c80-144">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
- [<span data-ttu-id="77c80-145">Différences entre les contrôles DataGridView et DataGrid Windows Forms</span><span class="sxs-lookup"><span data-stu-id="77c80-145">Differences Between the Windows Forms DataGridView and DataGrid Controls</span></span>](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md)
