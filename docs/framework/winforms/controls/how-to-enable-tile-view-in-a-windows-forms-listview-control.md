---
title: 'Procédure : activer le mode Mosaïque dans un contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tile view feature
- tiling
- Windows Forms, controls
- ListView control [Windows Forms], tile view
ms.assetid: c20e67a3-2d94-413d-9fcf-ecbd0fe251da
ms.openlocfilehash: 14eb21fa0285275e510b865c5cee7d1fc82fd0fd
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59326994"
---
# <a name="how-to-enable-tile-view-in-a-windows-forms-listview-control"></a><span data-ttu-id="fa5a7-102">Procédure : activer le mode Mosaïque dans un contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fa5a7-102">How to: Enable Tile View in a Windows Forms ListView Control</span></span>
<span data-ttu-id="fa5a7-103">Avec la fonctionnalité d'affichage en mosaïque du contrôle <xref:System.Windows.Forms.ListView>, vous pouvez fournir un équilibre visuel entre les informations graphiques et textuelles.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-103">With the tile view feature of the <xref:System.Windows.Forms.ListView> control, you can provide a visual balance between graphical and textual information.</span></span> <span data-ttu-id="fa5a7-104">Les informations textuelles affichées pour un élément dans l'affichage en mosaïque sont identiques aux informations de colonne définies pour le mode Détails.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-104">The textual information displayed for an item in tile view is the same as the column information defined for details view.</span></span> <span data-ttu-id="fa5a7-105">L'affichage en mosaïque fonctionne en association avec les fonctionnalités de regroupement ou de marques d'insertion du contrôle <xref:System.Windows.Forms.ListView>.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-105">Tile view works in combination with either the grouping or insertion mark features in the <xref:System.Windows.Forms.ListView> control.</span></span>  
  
 <span data-ttu-id="fa5a7-106">L'affichage en mosaïque utilise une icône de 32 x 32 pixels et plusieurs lignes de texte, comme illustré dans les images suivantes.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-106">The tile view uses a 32 x 32 pixel icon and several lines of text, as shown in the following images.</span></span>  
  
 <span data-ttu-id="fa5a7-107">![Affichage en mosaïque dans un contrôle ListView](./media/how-to-enable-tile-view-in-a-windows-forms-listview-control/tile-view-in-listview-control.gif "vignette vue icônes et du texte")</span><span class="sxs-lookup"><span data-stu-id="fa5a7-107">![Tile View in a ListView Control](./media/how-to-enable-tile-view-in-a-windows-forms-listview-control/tile-view-in-listview-control.gif "Tile view icons and text")</span></span>  
 
 <span data-ttu-id="fa5a7-108">Pour activer l'affichage en mosaïque, affectez la valeur <xref:System.Windows.Forms.View.Tile> à la propriété <xref:System.Windows.Forms.ListView.View%2A>.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-108">To enable tile view, set the <xref:System.Windows.Forms.ListView.View%2A> property to <xref:System.Windows.Forms.View.Tile>.</span></span> <span data-ttu-id="fa5a7-109">Vous pouvez ajuster la taille des mosaïques en définissant la propriété <xref:System.Windows.Forms.ListView.TileSize%2A> et le nombre de lignes de texte affichées dans la mosaïque en ajustant la collection <xref:System.Windows.Forms.ListView.Columns%2A>.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-109">You can adjust the size of the tiles by setting the <xref:System.Windows.Forms.ListView.TileSize%2A> property, and the number of text lines displayed in the tile by adjusting the <xref:System.Windows.Forms.ListView.Columns%2A> collection.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fa5a7-110">L'affichage en mosaïque est disponible uniquement sur [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] quand votre application appelle la méthode <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-110">The tile view is available only on [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] when your application calls the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="fa5a7-111">Sur les systèmes d'exploitation antérieurs, tout code lié à l'affichage en mosaïque n'a aucun effet et le contrôle <xref:System.Windows.Forms.ListView> s'affiche en mode Grandes icônes.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-111">On earlier operating systems, any code related to the tile view has no effect, and the <xref:System.Windows.Forms.ListView> control displays in the large icon view.</span></span> <span data-ttu-id="fa5a7-112">Pour plus d'informations, consultez <xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-112">For more information, see <xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>.</span></span>  
  
### <a name="to-set-tile-view-programmatically"></a><span data-ttu-id="fa5a7-113">Pour définir l'affichage en mosaïque par programmation</span><span class="sxs-lookup"><span data-stu-id="fa5a7-113">To set tile view programmatically</span></span>  
  
1. <span data-ttu-id="fa5a7-114">Utilisez l'énumération <xref:System.Windows.Forms.View> du contrôle <xref:System.Windows.Forms.ListView>.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-114">Use the <xref:System.Windows.Forms.View> enumeration of the <xref:System.Windows.Forms.ListView> control.</span></span>  
  
    ```vb  
    ListView1.View = View.Tile  
    ```  
  
    ```csharp  
    listView1.View = View.Tile;  
    ```  
  
## <a name="example"></a><span data-ttu-id="fa5a7-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="fa5a7-115">Example</span></span>  
 <span data-ttu-id="fa5a7-116">L'exemple de code complet suivant illustre l'affichage en mosaïque avec des mosaïques modifiées pour afficher trois lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-116">The following complete code example demonstrates Tile view with tiles modified to show three lines of text.</span></span> <span data-ttu-id="fa5a7-117">La taille des mosaïques a été ajustée pour empêcher le retour à la ligne.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-117">The tile size has been adjusted to prevent line-wrapping.</span></span>  
  
 [!code-cpp[System.Windows.Forms.ListView.Tiling#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/CPP/listviewtilingexample.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListView.Tiling#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/CS/listviewtilingexample.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Tiling#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/VB/listviewtilingexample.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="fa5a7-118">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="fa5a7-118">Compiling the Code</span></span>  
 <span data-ttu-id="fa5a7-119">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="fa5a7-119">This example requires:</span></span>  
  
-   <span data-ttu-id="fa5a7-120">des références aux assemblys System et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-120">References to the System and System.Windows.Forms assemblies.</span></span>  
  
-   <span data-ttu-id="fa5a7-121">un fichier d'icône nommé book.ico dans le même répertoire que le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-121">An icon file named book.ico in the same directory as the executable file.</span></span>  
  
 <span data-ttu-id="fa5a7-122">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="fa5a7-122">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="fa5a7-123">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="fa5a7-123">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa5a7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa5a7-124">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.TileSize%2A>
- [<span data-ttu-id="fa5a7-125">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="fa5a7-125">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="fa5a7-126">Vue d’ensemble du contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="fa5a7-126">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
