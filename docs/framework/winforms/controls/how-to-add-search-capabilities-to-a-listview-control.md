---
title: 'Procédure : ajouter des fonctionnalités de recherche à un contrôle ListView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- lists [Windows Forms], enabling searching
- list views [Windows Forms], enabling searching
- ListView control [Windows Forms], adding search capabilities
- searching [Windows Forms], adding search capabilities to ListView control
ms.assetid: 557782d9-b705-4bab-b496-9938afddac82
ms.openlocfilehash: c1c59c3d4bb5d0d35103371575ebdd49d3559bbe
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108548"
---
# <a name="how-to-add-search-capabilities-to-a-listview-control"></a><span data-ttu-id="c8b73-102">Procédure : ajouter des fonctionnalités de recherche à un contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="c8b73-102">How to: Add Search Capabilities to a ListView Control</span></span>
<span data-ttu-id="c8b73-103">Souvent, lorsque vous travaillez avec une longue liste d’éléments dans un <xref:System.Windows.Forms.ListView> contrôle, que vous souhaitez proposer des fonctionnalités de recherche à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c8b73-103">Oftentimes when working with a large list of items in a <xref:System.Windows.Forms.ListView> control, you want to offer search capabilities to the user.</span></span> <span data-ttu-id="c8b73-104">Le <xref:System.Windows.Forms.ListView> contrôle offre cette fonctionnalité de deux manières différentes : correspondance de texte et la recherche d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="c8b73-104">The <xref:System.Windows.Forms.ListView> control offers this capability in two different ways: text matching and location searching.</span></span>  
  
 <span data-ttu-id="c8b73-105">Le <xref:System.Windows.Forms.ListView.FindItemWithText%2A> méthode vous permet d’effectuer une recherche de texte sur un <xref:System.Windows.Forms.ListView> dans la vue liste ou détails, donné une chaîne de recherche et d’un début facultatif et d’index de fin.</span><span class="sxs-lookup"><span data-stu-id="c8b73-105">The <xref:System.Windows.Forms.ListView.FindItemWithText%2A> method allows you to perform a text search on a <xref:System.Windows.Forms.ListView> in list or details view, given a search string and an optional starting and ending index.</span></span> <span data-ttu-id="c8b73-106">En revanche, le <xref:System.Windows.Forms.ListView.FindNearestItem%2A> méthode permet de rechercher un élément dans un <xref:System.Windows.Forms.ListView> en mode icône ou une vignette, étant donné un ensemble de coordonnées x et y et une direction à rechercher.</span><span class="sxs-lookup"><span data-stu-id="c8b73-106">In contrast, the <xref:System.Windows.Forms.ListView.FindNearestItem%2A> method allows you to find an item in a <xref:System.Windows.Forms.ListView> in icon or tile view, given a set of x- and y-coordinates and a direction to search.</span></span>  
  
### <a name="to-find-an-item-using-text"></a><span data-ttu-id="c8b73-107">Pour rechercher un élément à l’aide de texte</span><span class="sxs-lookup"><span data-stu-id="c8b73-107">To find an item using text</span></span>  
  
1.  <span data-ttu-id="c8b73-108">Créer un <xref:System.Windows.Forms.ListView> avec la <xref:System.Windows.Forms.ListView.View%2A> propriété définie sur <xref:System.Windows.Forms.View.Details> ou <xref:System.Windows.Forms.View.List>, puis remplissez le <xref:System.Windows.Forms.ListView> avec des éléments.</span><span class="sxs-lookup"><span data-stu-id="c8b73-108">Create a <xref:System.Windows.Forms.ListView> with the <xref:System.Windows.Forms.ListView.View%2A> property set to <xref:System.Windows.Forms.View.Details> or <xref:System.Windows.Forms.View.List>, and then populate the <xref:System.Windows.Forms.ListView> with items.</span></span>  
  
2.  <span data-ttu-id="c8b73-109">Appelez le <xref:System.Windows.Forms.ListView.FindItemWithText%2A> méthode, en passant le texte de l’élément que vous souhaitez obtenir.</span><span class="sxs-lookup"><span data-stu-id="c8b73-109">Call the <xref:System.Windows.Forms.ListView.FindItemWithText%2A> method, passing the text of the item you would like to find.</span></span>  
  
3.  <span data-ttu-id="c8b73-110">L’exemple de code suivant montre comment créer un base <xref:System.Windows.Forms.ListView>, remplir avec des éléments et utiliser la saisie de texte à partir de l’utilisateur pour rechercher un élément dans la liste.</span><span class="sxs-lookup"><span data-stu-id="c8b73-110">The following code example demonstrates how to create a basic <xref:System.Windows.Forms.ListView>, populate it with items, and use text input from the user to find an item in the list.</span></span>  
  
 [!code-cpp[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/cpp/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.ListViewFindItems#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/VB/form1.vb#1)]  
  
### <a name="to-find-an-item-using-x--and-y-coordinates"></a><span data-ttu-id="c8b73-111">Pour rechercher un élément à l’aide des coordonnées x et y</span><span class="sxs-lookup"><span data-stu-id="c8b73-111">To find an item using x- and y-coordinates</span></span>  
  
1.  <span data-ttu-id="c8b73-112">Créer un <xref:System.Windows.Forms.ListView> avec la <xref:System.Windows.Forms.View> propriété définie sur <xref:System.Windows.Forms.View.SmallIcon> ou <xref:System.Windows.Forms.View.LargeIcon>, puis remplissez le <xref:System.Windows.Forms.ListView> avec des éléments.</span><span class="sxs-lookup"><span data-stu-id="c8b73-112">Create a <xref:System.Windows.Forms.ListView> with the <xref:System.Windows.Forms.View> property set to <xref:System.Windows.Forms.View.SmallIcon> or <xref:System.Windows.Forms.View.LargeIcon>, and then populate the <xref:System.Windows.Forms.ListView> with items.</span></span>  
  
2.  <span data-ttu-id="c8b73-113">Appelez le <xref:System.Windows.Forms.ListView.FindNearestItem%2A> méthode, en passant les coordonnées x - et y-souhaitée et la direction que vous souhaitez rechercher.</span><span class="sxs-lookup"><span data-stu-id="c8b73-113">Call the <xref:System.Windows.Forms.ListView.FindNearestItem%2A> method, passing the desired x- and y-coordinates and the direction you would like to search.</span></span>  
  
3.  <span data-ttu-id="c8b73-114">L’exemple de code suivant montre comment créer une icône de base <xref:System.Windows.Forms.ListView>, remplir avec des éléments, puis capturez la <xref:System.Windows.Forms.Control.MouseDown> événements pour rechercher l’élément le plus proche dans la direction verticale.</span><span class="sxs-lookup"><span data-stu-id="c8b73-114">The following code example demonstrates how to create a basic icon <xref:System.Windows.Forms.ListView>, populate it with items, and capture the <xref:System.Windows.Forms.Control.MouseDown> event to find the nearest item in the up direction.</span></span>  
  
 [!code-cpp[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/cpp/form1.cpp#2)]
 [!code-csharp[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/CS/form1.cs#2)]
 [!code-vb[System.Windows.Forms.ListViewFindItems#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewFindItems/VB/form1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="c8b73-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8b73-115">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.FindItemWithText%2A>
- <xref:System.Windows.Forms.ListView.FindNearestItem%2A>
- [<span data-ttu-id="c8b73-116">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="c8b73-116">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="c8b73-117">Vue d’ensemble du contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="c8b73-117">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="c8b73-118">Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c8b73-118">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
