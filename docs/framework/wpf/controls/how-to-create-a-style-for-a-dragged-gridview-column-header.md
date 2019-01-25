---
title: 'Procédure : Créer un style pour un en-tête de colonne GridView déplacé'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 0b999645-0313-4b33-80b9-19ece08b5459
ms.openlocfilehash: dd347781451c9e574fed97c1a553c25bda1b8d7a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54545395"
---
# <a name="how-to-create-a-style-for-a-dragged-gridview-column-header"></a><span data-ttu-id="1174e-102">Procédure : Créer un style pour un en-tête de colonne GridView déplacé</span><span class="sxs-lookup"><span data-stu-id="1174e-102">How to: Create a Style for a Dragged GridView Column Header</span></span>
<span data-ttu-id="1174e-103">Cet exemple montre comment modifier l’apparence d’un glissé <xref:System.Windows.Controls.GridViewColumnHeader> lorsque l’utilisateur modifie la position d’une colonne.</span><span class="sxs-lookup"><span data-stu-id="1174e-103">This example shows how to change the appearance of a dragged <xref:System.Windows.Controls.GridViewColumnHeader> when the user changes the position of a column.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1174e-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1174e-104">Example</span></span>  
 <span data-ttu-id="1174e-105">Lorsque vous faites glisser un en-tête de colonne vers un autre emplacement dans un <xref:System.Windows.Controls.ListView> qui utilise <xref:System.Windows.Controls.GridView> comme mode d’affichage, la colonne se déplace vers la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="1174e-105">When you drag a column header to another location in a <xref:System.Windows.Controls.ListView> that uses <xref:System.Windows.Controls.GridView> for its view mode, the column moves to the new position.</span></span> <span data-ttu-id="1174e-106">Lorsque vous faites glisser l’en-tête de colonne, une copie flottante de l’en-tête s’affiche en plus de l’en-tête d’origine.</span><span class="sxs-lookup"><span data-stu-id="1174e-106">While you are dragging the column header, a floating copy of the header appears in addition to the original header.</span></span> <span data-ttu-id="1174e-107">Un en-tête de colonne dans un <xref:System.Windows.Controls.GridView> est représenté par un <xref:System.Windows.Controls.GridViewColumnHeader> objet.</span><span class="sxs-lookup"><span data-stu-id="1174e-107">A column header in a <xref:System.Windows.Controls.GridView> is represented by a <xref:System.Windows.Controls.GridViewColumnHeader> object.</span></span>  
  
 <span data-ttu-id="1174e-108">Pour personnaliser l’apparence des en-têtes flottants et d’origine, vous pouvez définir <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> pour modifier la <xref:System.Windows.Controls.GridViewColumnHeader> <xref:System.Windows.Style>.</span><span class="sxs-lookup"><span data-stu-id="1174e-108">To customize the appearance of both the floating and original headers, you can set <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> to modify the <xref:System.Windows.Controls.GridViewColumnHeader> <xref:System.Windows.Style>.</span></span> <span data-ttu-id="1174e-109">Ces <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> sont appliquées lorsque le <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> valeur de propriété est `true` et <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> valeur de propriété est <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating>.</span><span class="sxs-lookup"><span data-stu-id="1174e-109">These <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> are applied when the <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> property value is `true` and the <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> property value is <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating>.</span></span>  
  
 <span data-ttu-id="1174e-110">Lorsque l’utilisateur appuie sur le bouton de la souris et le maintient enfoncé quand la souris s’arrête sur la <xref:System.Windows.Controls.GridViewColumnHeader>, le <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> modification de la valeur de propriété à `true`.</span><span class="sxs-lookup"><span data-stu-id="1174e-110">When the user presses the mouse button and holds it down while the mouse pauses on the <xref:System.Windows.Controls.GridViewColumnHeader>, the <xref:System.Windows.Controls.Primitives.ButtonBase.IsPressed%2A> property value changes to `true`.</span></span> <span data-ttu-id="1174e-111">De même, lorsque l’utilisateur commence l’opération glisser, la <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> modifications apportées aux propriétés <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating>.</span><span class="sxs-lookup"><span data-stu-id="1174e-111">Likewise, when the user begins the drag operation, the <xref:System.Windows.Controls.GridViewColumnHeader.Role%2A> property changes to <xref:System.Windows.Controls.GridViewColumnHeaderRole.Floating>.</span></span>  
  
 <span data-ttu-id="1174e-112">L’exemple suivant montre comment définir <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> pour modifier la <xref:System.Windows.Controls.Control.Foreground%2A> et <xref:System.Windows.Controls.Control.Background%2A> couleurs des en-têtes flottants et d’origine lorsque l’utilisateur fait glisser une colonne vers une nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="1174e-112">The following example shows how to set <xref:System.Windows.Controls.ControlTemplate.Triggers%2A> to change the <xref:System.Windows.Controls.Control.Foreground%2A> and <xref:System.Windows.Controls.Control.Background%2A> colors of the original and floating headers when the user drags a column to a new position.</span></span>  
  
 [!code-xaml[ListViewHeaderRoleStyle#GVCHControlTemplateStart](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#gvchcontroltemplatestart)]  
[!code-xaml[ListViewHeaderRoleStyle#ControlTemplateTriggersStart](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#controltemplatetriggersstart)]  
[!code-xaml[ListViewHeaderRoleStyle#IsPressed](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#ispressed)]  
[!code-xaml[ListViewHeaderRoleStyle#Floating](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#floating)]  
[!code-xaml[ListViewHeaderRoleStyle#ControlTemplateTriggersEnd](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#controltemplatetriggersend)]  
[!code-xaml[ListViewHeaderRoleStyle#GVCHControlTemplateEnd](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHeaderRoleStyle/CS/Window1.xaml#gvchcontroltemplateend)]  
  
## <a name="see-also"></a><span data-ttu-id="1174e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1174e-113">See also</span></span>
- <xref:System.Windows.Controls.GridViewColumnHeader>
- <xref:System.Windows.Controls.GridViewColumnHeaderRole>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="1174e-114">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="1174e-114">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
- [<span data-ttu-id="1174e-115">Vue d’ensemble de ListView</span><span class="sxs-lookup"><span data-stu-id="1174e-115">ListView Overview</span></span>](../../../../docs/framework/wpf/controls/listview-overview.md)
- [<span data-ttu-id="1174e-116">Vue d’ensemble de GridView</span><span class="sxs-lookup"><span data-stu-id="1174e-116">GridView Overview</span></span>](../../../../docs/framework/wpf/controls/gridview-overview.md)
