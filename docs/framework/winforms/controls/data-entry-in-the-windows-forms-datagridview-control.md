---
title: Saisie de données dans le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], data entry
- data entry [Windows Forms], dataGridView control
- data grids [Windows Forms], data entry
ms.assetid: 4a6d4676-d4e7-4b0e-9c22-50ce65ffe0d6
ms.openlocfilehash: e3022ceddd9fab5610a0856b5e3273d8c046a5fa
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57719735"
---
# <a name="data-entry-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="26fa8-102">Saisie de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26fa8-102">Data Entry in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="26fa8-103">Le `DataGridView` contrôle fournit plusieurs fonctionnalités qui permettent de vous changer la façon dont les utilisateurs ajouter ou modifient des données dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="26fa8-103">The `DataGridView` control provides several features that let you change how users add or modify data in the control.</span></span> <span data-ttu-id="26fa8-104">Par exemple, vous pouvez rendre saisie de données plus efficaces en fournissant des valeurs par défaut pour les nouvelles lignes et en avertissant les utilisateurs lorsque des erreurs se produisent.</span><span class="sxs-lookup"><span data-stu-id="26fa8-104">For example, you can make data entry more efficient by providing default values for new rows and by alerting users when errors occur.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="26fa8-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="26fa8-105">In This Section</span></span>  
 [<span data-ttu-id="26fa8-106">Guide pratique pour Spécifier le Mode édition pour le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26fa8-106">How to: Specify the Edit Mode for the Windows Forms DataGridView Control</span></span>](how-to-specify-the-edit-mode-for-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="26fa8-107">Décrit comment modifier la façon dont les utilisateurs démarrent la modification des cellules.</span><span class="sxs-lookup"><span data-stu-id="26fa8-107">Describes how to change the way users start editing cells.</span></span>  
  
 [<span data-ttu-id="26fa8-108">Guide pratique pour Spécifiez les valeurs par défaut pour les nouvelles lignes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26fa8-108">How to: Specify Default Values for New Rows in the Windows Forms DataGridView Control</span></span>](specify-default-values-for-new-rows-in-the-datagrid.md)  
 <span data-ttu-id="26fa8-109">Décrit comment préremplir la ligne pour les nouveaux enregistrements gagner du temps de saisie de données.</span><span class="sxs-lookup"><span data-stu-id="26fa8-109">Describes how to prepopulate the row for new records to save data-entry time.</span></span>  
  
 [<span data-ttu-id="26fa8-110">Utilisation de la ligne pour les nouveaux enregistrements dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26fa8-110">Using the Row for New Records in the Windows Forms DataGridView Control</span></span>](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="26fa8-111">Décrit la ligne pour les nouveaux enregistrements en détail, y compris des informations sur son masquage, sur la personnalisation de son apparence et sur sa relation avec la <xref:System.Windows.Forms.DataGridView.Rows%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="26fa8-111">Describes the row for new records in detail, including information on hiding it, on customizing its appearance, and on how it relates to the <xref:System.Windows.Forms.DataGridView.Rows%2A> collection.</span></span>  
  
 [<span data-ttu-id="26fa8-112">Procédure pas à pas : Validation des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26fa8-112">Walkthrough: Validating Data in the Windows Forms DataGridView Control</span></span>](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="26fa8-113">Décrit comment valider l’entrée utilisateur pour éviter les erreurs de mise en forme de saisie de données.</span><span class="sxs-lookup"><span data-stu-id="26fa8-113">Describes how to validate user input to prevent data-entry formatting errors.</span></span>  
  
 [<span data-ttu-id="26fa8-114">Procédure pas à pas : Gestion des erreurs qui se produisent lors de la saisie de données dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26fa8-114">Walkthrough: Handling Errors that Occur During Data Entry in the Windows Forms DataGridView Control</span></span>](handling-errors-that-occur-during-data-entry-in-the-datagrid.md)  
 <span data-ttu-id="26fa8-115">Décrit comment gérer les erreurs de saisie de données qui proviennent de la source de données lorsque l’utilisateur tente de valider une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="26fa8-115">Describes how to handle data-entry errors that originate from the data source when the user attempts to commit a new value.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="26fa8-116">Référence</span><span class="sxs-lookup"><span data-stu-id="26fa8-116">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="26fa8-117">Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="26fa8-117">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.EditMode%2A?displayProperty=nameWithType>  
 <span data-ttu-id="26fa8-118">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.EditMode%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="26fa8-118">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.EditMode%2A> property.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded?displayProperty=nameWithType>  
 <span data-ttu-id="26fa8-119">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> événement.</span><span class="sxs-lookup"><span data-stu-id="26fa8-119">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> event.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.DataError?displayProperty=nameWithType>  
 <span data-ttu-id="26fa8-120">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.DataError> événement.</span><span class="sxs-lookup"><span data-stu-id="26fa8-120">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.DataError> event.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.CellValidating?displayProperty=nameWithType>  
 <span data-ttu-id="26fa8-121">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.CellValidating> événement.</span><span class="sxs-lookup"><span data-stu-id="26fa8-121">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.CellValidating> event.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="26fa8-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26fa8-122">Related Sections</span></span>  
 [<span data-ttu-id="26fa8-123">Affichage des données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26fa8-123">Displaying Data in the Windows Forms DataGridView Control</span></span>](displaying-data-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="26fa8-124">Fournit des rubriques qui décrivent comment remplir le contrôle de données manuellement ou à partir de la source de données externe.</span><span class="sxs-lookup"><span data-stu-id="26fa8-124">Provides topics that describe how to populate the control with data either manually or from an external data source.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26fa8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26fa8-125">See also</span></span>
- [<span data-ttu-id="26fa8-126">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="26fa8-126">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
- [<span data-ttu-id="26fa8-127">Types de colonnes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="26fa8-127">Column Types in the Windows Forms DataGridView Control</span></span>](column-types-in-the-windows-forms-datagridview-control.md)
