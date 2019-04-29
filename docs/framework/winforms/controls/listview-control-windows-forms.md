---
title: ListView, contrôle (Windows Forms)
ms.date: 03/30/2017
helpviewer_keywords:
- lists
- checked list items [Windows Forms], Windows Forms controls
- user interface [Windows Forms], creating
- lists [Windows Forms], items with icons
- icons [Windows Forms], listing with items
- list views
- ListView control [Windows Forms]
- list controls [Windows Forms], List view
ms.assetid: 9f71cf5c-82da-488a-a04e-ef52c0817187
ms.openlocfilehash: d826fe0a64ad226db62e01259b0466f7f495f8e0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61757873"
---
# <a name="listview-control-windows-forms"></a><span data-ttu-id="45262-102">ListView, contrôle (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="45262-102">ListView Control (Windows Forms)</span></span>
<span data-ttu-id="45262-103">Le contrôle `ListView` Windows Forms affiche une liste d'éléments avec des icônes.</span><span class="sxs-lookup"><span data-stu-id="45262-103">The Windows Forms `ListView` control displays a list of items with icons.</span></span> <span data-ttu-id="45262-104">Vous pouvez utiliser un affichage de liste pour créer une interface utilisateur comme le volet droit de l'Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="45262-104">You can use a list view to create a user interface like the right pane of Windows Explorer.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="45262-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="45262-105">In This Section</span></span>  
 [<span data-ttu-id="45262-106">Vue d’ensemble du contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="45262-106">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)  
 <span data-ttu-id="45262-107">Décrit ce contrôle et ses principales fonctionnalités et propriétés.</span><span class="sxs-lookup"><span data-stu-id="45262-107">Describes this control and its key features and properties.</span></span>  
  
 [<span data-ttu-id="45262-108">Guide pratique pour Ajouter et supprimer des éléments avec le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-108">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)  
 <span data-ttu-id="45262-109">Décrit comment ajouter ou supprimer des éléments dans un affichage de liste.</span><span class="sxs-lookup"><span data-stu-id="45262-109">Describes how to add or remove items from a list view.</span></span>  
  
 [<span data-ttu-id="45262-110">Guide pratique pour Ajouter des colonnes au contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-110">How to: Add Columns to the Windows Forms ListView Control</span></span>](how-to-add-columns-to-the-windows-forms-listview-control.md)  
 <span data-ttu-id="45262-111">Décrit comment créer des colonnes pour afficher des informations sur chaque élément de la liste.</span><span class="sxs-lookup"><span data-stu-id="45262-111">Describes how to create columns in order to display information about each list item.</span></span>  
  
 [<span data-ttu-id="45262-112">Guide pratique pour Afficher des icônes pour le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-112">How to: Display Icons for the Windows Forms ListView Control</span></span>](how-to-display-icons-for-the-windows-forms-listview-control.md)  
 <span data-ttu-id="45262-113">Décrit comment associer un affichage de liste à une liste d'images appropriée pour l'affichage de petites ou grandes icônes.</span><span class="sxs-lookup"><span data-stu-id="45262-113">Describes how to associate a list view with an appropriate image list for displaying large or small icons.</span></span>  
  
 [<span data-ttu-id="45262-114">Guide pratique pour Afficher des sous-éléments en colonnes avec le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-114">How to: Display Subitems in Columns with the Windows Forms ListView Control</span></span>](how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)  
 <span data-ttu-id="45262-115">Décrit comment afficher des informations sur chaque élément de la liste dans des colonnes.</span><span class="sxs-lookup"><span data-stu-id="45262-115">Describes how to display information about each list item in columns.</span></span>  
  
 [<span data-ttu-id="45262-116">Guide pratique pour Sélectionnez un élément dans le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-116">How to: Select an Item in the Windows Forms ListView Control</span></span>](how-to-select-an-item-in-the-windows-forms-listview-control.md)  
 <span data-ttu-id="45262-117">Décrit comment sélectionner un élément par programmation.</span><span class="sxs-lookup"><span data-stu-id="45262-117">Describes how to programmatically select an item.</span></span>  
  
 [<span data-ttu-id="45262-118">Guide pratique pour Grouper des éléments dans un contrôle de ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-118">How to: Group Items in a Windows Forms ListView Control</span></span>](how-to-group-items-in-a-windows-forms-listview-control.md)  
 <span data-ttu-id="45262-119">Décrit comment créer des groupes pour l'affichage par catégorie et comment assigner des éléments à chaque groupe.</span><span class="sxs-lookup"><span data-stu-id="45262-119">Describes how to create groups for categorized display and how to assign items to each group.</span></span>  
  
 <span data-ttu-id="45262-120">Cette fonctionnalité est disponible uniquement pour [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)].</span><span class="sxs-lookup"><span data-stu-id="45262-120">This feature is available only for [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)].</span></span>  
  
 [<span data-ttu-id="45262-121">Guide pratique pour Activer l’affichage en mosaïque dans un contrôle de ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-121">How to: Enable Tile View in a Windows Forms ListView Control</span></span>](how-to-enable-tile-view-in-a-windows-forms-listview-control.md)  
 <span data-ttu-id="45262-122">Décrit comment afficher les éléments sous forme de vignettes, chacune d'elles composée d'une grande icône et de plusieurs lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="45262-122">Describes how to display items as tiles, each of which is comprised of a large icon and multiple lines of text.</span></span>  
  
 <span data-ttu-id="45262-123">Cette fonctionnalité est disponible uniquement pour [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)].</span><span class="sxs-lookup"><span data-stu-id="45262-123">This feature is available only for [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)].</span></span>  
  
 [<span data-ttu-id="45262-124">Guide pratique pour Afficher une marque d’Insertion dans un contrôle de ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-124">How to: Display an Insertion Mark in a Windows Forms ListView Control</span></span>](how-to-display-an-insertion-mark-in-a-windows-forms-listview-control.md)  
 <span data-ttu-id="45262-125">Décrit comment implémenter les commentaires utilisateur pour les opérations de glisser-déplacer dans lesquelles une marque d'insertion indique l'emplacement cible pour chaque position du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="45262-125">Describes how to implement user-feedback for drag-and-drop operations in which an insertion mark indicates the drop location for each mouse-pointer position.</span></span>  
  
 <span data-ttu-id="45262-126">Cette fonctionnalité est disponible uniquement pour [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)].</span><span class="sxs-lookup"><span data-stu-id="45262-126">This feature is available only for [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)].</span></span>  
  
 [<span data-ttu-id="45262-127">Guide pratique pour Ajouter des fonctionnalités de recherche à un contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="45262-127">How to: Add Search Capabilities to a ListView Control</span></span>](how-to-add-search-capabilities-to-a-listview-control.md)  
 <span data-ttu-id="45262-128">Décrit comment rechercher un élément par programmation à l'aide de coordonnées d'écran ou de la recherche de texte.</span><span class="sxs-lookup"><span data-stu-id="45262-128">Describes how to programmatically find an item using either text search or screen coordinates.</span></span>  
  
- [<span data-ttu-id="45262-129">Guide pratique pour Activer l’affichage en mosaïque dans un contrôle de ListView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="45262-129">How to: Enable Tile View in a Windows Forms ListView Control Using the Designer</span></span>](enable-tile-view-in-a-wf-listview-control-using-the-designer.md)  
  
- [<span data-ttu-id="45262-130">Guide pratique pour Ajouter et supprimer des éléments avec le contrôle de ListView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="45262-130">How to: Add and Remove Items with the Windows Forms ListView Control Using the Designer</span></span>](add-and-remove-items-with-wf-listview-control-using-the-designer.md)  
  
- [<span data-ttu-id="45262-131">Guide pratique pour Ajouter des colonnes au contrôle ListView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="45262-131">How to: Add Columns to the Windows Forms ListView Control Using the Designer</span></span>](how-to-add-columns-to-the-windows-forms-listview-control-using-the-designer.md)  
  
- [<span data-ttu-id="45262-132">Guide pratique pour Grouper des éléments dans un contrôle de ListView Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="45262-132">How to: Group Items in a Windows Forms ListView Control Using the Designer</span></span>](how-to-group-items-in-a-windows-forms-listview-control-using-the-designer.md)  
  
- [<span data-ttu-id="45262-133">Procédure pas à pas : Création d’une Interface de Style Explorateur avec les contrôles TreeView à l’aide du Concepteur de ListView</span><span class="sxs-lookup"><span data-stu-id="45262-133">Walkthrough: Creating an Explorer Style Interface with the ListView and TreeView Controls Using the Designer</span></span>](creating-an-explorer-style-interface-with-the-listview-and-treeview.md)  
  
## <a name="reference"></a><span data-ttu-id="45262-134">Référence</span><span class="sxs-lookup"><span data-stu-id="45262-134">Reference</span></span>  
 <span data-ttu-id="45262-135">Classe <xref:System.Windows.Forms.ListView></span><span class="sxs-lookup"><span data-stu-id="45262-135"><xref:System.Windows.Forms.ListView> class</span></span>  
 <span data-ttu-id="45262-136">Décrit cette classe et fournit des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="45262-136">Describes this class and has links to all its members.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="45262-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45262-137">Related Sections</span></span>  
 [<span data-ttu-id="45262-138">Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="45262-138">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](add-custom-information-to-a-treeview-or-listview-control-wf.md)  
 <span data-ttu-id="45262-139">Décrit comment hériter d’un élément dans un affichage de liste ou d’un nœud dans une arborescence pour ajouter des champs, des méthodes ou des constructeurs dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="45262-139">Describes how to inherit from an item in a list view or a node in a tree view in order to add any fields, methods, or constructors you need.</span></span>  
  
 [<span data-ttu-id="45262-140">ImageList, composant</span><span class="sxs-lookup"><span data-stu-id="45262-140">ImageList Component</span></span>](imagelist-component-windows-forms.md)  
 <span data-ttu-id="45262-141">Explique ce qu'est une liste d'images et ses principales fonctionnalités et propriétés.</span><span class="sxs-lookup"><span data-stu-id="45262-141">Explains what an image list is and its key features and properties.</span></span>  
  
 [<span data-ttu-id="45262-142">Guide pratique pour Créer une Interface utilisateur à plusieurs volets avec des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-142">How to: Create a Multipane User Interface with Windows Forms</span></span>](how-to-create-a-multipane-user-interface-with-windows-forms.md)  
 <span data-ttu-id="45262-143">Fournit des instructions pour disposer un Windows Form avec plusieurs volets.</span><span class="sxs-lookup"><span data-stu-id="45262-143">Gives instructions for laying out a Windows Form with multiple panes.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45262-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45262-144">See also</span></span>

- [<span data-ttu-id="45262-145">Contrôles à utiliser dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="45262-145">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
