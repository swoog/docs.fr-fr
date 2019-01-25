---
title: Utilisation du concepteur avec le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- tables [Windows Forms]
- DataGridView control [Windows Forms], designer support
- formatting [Windows Forms]
ms.assetid: b66057a6-5983-4864-b4e7-8cbc88a7010c
ms.openlocfilehash: 588db8b2f66bbfd58ea6197a7b5a65bb8ecbfd19
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644809"
---
# <a name="using-the-designer-with-the-windows-forms-datagridview-control"></a><span data-ttu-id="f69c5-102">Utilisation du concepteur avec le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f69c5-102">Using the Designer with the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="f69c5-103">Visual Studio fournit la prise en charge du concepteur pour le `DataGridView` contrôle qui vous permet d’effectuer de nombreuses tâches d’installation sans écrire de code.</span><span class="sxs-lookup"><span data-stu-id="f69c5-103">Visual Studio provides designer support for the `DataGridView` control that enables you to perform many setup tasks without writing code.</span></span> <span data-ttu-id="f69c5-104">Ces tâches comprennent la liaison utilisé par le contrôle à une source de données, modification des colonnes pour afficher des données et ajuster l’apparence et le comportement de base du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f69c5-104">These tasks include binding the control to a data source, modifying the columns used to display data, and adjusting the appearance and basic behavior of the control.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f69c5-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f69c5-105">In This Section</span></span>  
 [<span data-ttu-id="f69c5-106">Guide pratique pour Ajouter et supprimer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-106">How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/add-and-remove-columns-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-107">Décrit comment utiliser le **Add Columns** et **modifier les colonnes** boîtes de dialogue pour remplir et modifier la collection de colonnes.</span><span class="sxs-lookup"><span data-stu-id="f69c5-107">Describes how to use the **Add Columns** and **Edit Columns** dialog boxes to populate and modify the columns collection.</span></span>  
  
 [<span data-ttu-id="f69c5-108">Guide pratique pour Lier des données pour le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-108">How to: Bind Data to the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/bind-data-to-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-109">Décrit comment utiliser le **choisir la Source de données** option sur la balise active du contrôle pour vous connecter aux données.</span><span class="sxs-lookup"><span data-stu-id="f69c5-109">Describes how to use the **Choose Data Source** option on the control's smart tag to connect to data.</span></span>  
  
 [<span data-ttu-id="f69c5-110">Guide pratique pour Modifier l’ordre des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-110">How to: Change the Order of Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/change-the-order-of-columns-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-111">Décrit comment utiliser le **modifier les colonnes** réorganiser les colonnes de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f69c5-111">Describes how to use the **Edit Columns** dialog box to rearrange columns.</span></span>  
  
 [<span data-ttu-id="f69c5-112">Guide pratique pour Modifier le Type d’une colonne de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-112">How to: Change the Type of a Windows Forms DataGridView Column Using the Designer</span></span>](../../../../docs/framework/winforms/controls/change-the-type-of-a-wf-datagridview-column-using-the-designer.md)  
 <span data-ttu-id="f69c5-113">Décrit comment utiliser le **modifier les colonnes** boîte de dialogue pour modifier les types de colonne.</span><span class="sxs-lookup"><span data-stu-id="f69c5-113">Describes how to use the **Edit Columns** dialog box to change column types.</span></span>  
  
 [<span data-ttu-id="f69c5-114">Guide pratique pour Activer la réorganisation des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-114">How to: Enable Column Reordering in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/enable-column-reordering-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-115">Décrit comment utiliser des balises actives du contrôle pour permettre aux utilisateurs de réorganiser les colonnes.</span><span class="sxs-lookup"><span data-stu-id="f69c5-115">Describes how to use the control's smart tag to enable users to rearrange columns.</span></span>  
  
 [<span data-ttu-id="f69c5-116">Guide pratique pour Figer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-116">How to: Freeze Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/freeze-columns-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-117">Décrit comment utiliser le **modifier les colonnes** boîte de dialogue pour empêcher le défilement de colonnes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f69c5-117">Describes how to use the **Edit Columns** dialog box to prevent specific columns from scrolling.</span></span>  
  
 [<span data-ttu-id="f69c5-118">Guide pratique pour Masquer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-118">How to: Hide Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/hide-columns-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-119">Décrit comment utiliser le **modifier les colonnes** boîte de dialogue pour masquer des colonnes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f69c5-119">Describes how to use the **Edit Columns** dialog box to hide specific columns.</span></span>  
  
 [<span data-ttu-id="f69c5-120">Guide pratique pour Rendre les colonnes en lecture seule dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-120">How to: Make Columns Read-Only in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/make-columns-read-only-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-121">Décrit comment utiliser le **modifier les colonnes** boîte de dialogue pour empêcher les utilisateurs de modifier les valeurs dans des colonnes spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f69c5-121">Describes how to use the **Edit Columns** dialog box to prevent users from editing values in specific columns.</span></span>  
  
 [<span data-ttu-id="f69c5-122">Guide pratique pour Empêcher l’ajout de ligne et la suppression dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-122">How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/prevent-row-addition-and-deletion-in-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-123">Décrit comment utiliser des balises actives du contrôle pour empêcher les utilisateurs d’ajouter ou supprimer des lignes.</span><span class="sxs-lookup"><span data-stu-id="f69c5-123">Describes how to use the control's smart tag to prevent users from adding or deleting rows.</span></span>  
  
 [<span data-ttu-id="f69c5-124">Guide pratique pour Définir les Styles de ligne en alternance pour le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-124">How to: Set Alternating Row Styles for the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/set-alternating-row-styles-for-the-datagrid-using-the-designer.md)  
 <span data-ttu-id="f69c5-125">Décrit comment utiliser le **Générateur CellStyle** boîte de dialogue pour créer une apparence de type livre comptable dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f69c5-125">Describes how to use the **CellStyle Builder** dialog box to create a ledger-like appearance in the control.</span></span>  
  
 [<span data-ttu-id="f69c5-126">Guide pratique pour Définir des Styles de cellules par défaut et les Formats de données pour le contrôle de DataGridView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="f69c5-126">How to: Set Default Cell Styles and Data Formats for the Windows Forms DataGridView Control Using the Designer</span></span>](../../../../docs/framework/winforms/controls/default-cell-styles-datagridview.md)  
 <span data-ttu-id="f69c5-127">Décrit comment utiliser le **Générateur CellStyle** boîte de dialogue pour configurer l’apparence de base et l’affichage de données met en forme pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f69c5-127">Describes how to use the **CellStyle Builder** dialog box to set up the basic appearance and data-display formats for the control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="f69c5-128">Référence</span><span class="sxs-lookup"><span data-stu-id="f69c5-128">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="f69c5-129">Fournit la documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="f69c5-129">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f69c5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f69c5-130">See also</span></span>
- [<span data-ttu-id="f69c5-131">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="f69c5-131">DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)
