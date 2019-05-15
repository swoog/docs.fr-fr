---
title: 'Procédure : activer les marges de sélection et d’image dans les contrôles ContextMenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ShowCheckMargin property [Windows Forms]
- ShowImageMargin property [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
ms.assetid: eb584e71-59da-4012-aaca-dbe1c7c7a156
ms.openlocfilehash: bf8440704a7e457d0c987c933cc26e0e12e9565f
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591691"
---
# <a name="how-to-enable-check-margins-and-image-margins-in-contextmenustrip-controls"></a><span data-ttu-id="7c698-102">Procédure : activer les marges de sélection et d’image dans les contrôles ContextMenuStrip</span><span class="sxs-lookup"><span data-stu-id="7c698-102">How to: Enable Check Margins and Image Margins in ContextMenuStrip Controls</span></span>
<span data-ttu-id="7c698-103">Vous pouvez personnaliser les objets <xref:System.Windows.Forms.ToolStripMenuItem> de votre contrôle <xref:System.Windows.Forms.MenuStrip> avec des coches et des images personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7c698-103">You can customize the <xref:System.Windows.Forms.ToolStripMenuItem> objects in your <xref:System.Windows.Forms.MenuStrip> control with check marks and custom images.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7c698-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c698-104">Example</span></span>  
 <span data-ttu-id="7c698-105">L'exemple de code suivant montre comment créer des éléments de menu contenant des coches et des images personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7c698-105">The following code example demonstrates how to create menu items that have check marks and custom images.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#60](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#60)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#60](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#60)]  
  
 <span data-ttu-id="7c698-106">Définissez les propriétés <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A?displayProperty=nameWithType> et <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A?displayProperty=nameWithType> pour spécifier à quel moment doivent s'afficher les coches et les images personnalisées dans les éléments du menu.</span><span class="sxs-lookup"><span data-stu-id="7c698-106">Set the <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowCheckMargin%2A?displayProperty=nameWithType> and <xref:System.Windows.Forms.ToolStripDropDownMenu.ShowImageMargin%2A?displayProperty=nameWithType> properties to specify when check marks and custom images appear in your menu items.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7c698-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="7c698-107">Compiling the Code</span></span>  
 <span data-ttu-id="7c698-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="7c698-108">This example requires:</span></span>  
  
- <span data-ttu-id="7c698-109">des références aux assemblys System.Design, System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="7c698-109">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c698-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c698-110">See also</span></span>

- <xref:System.Windows.Forms.ToolStripMenuItem>
- <xref:System.Windows.Forms.ToolStripDropDownMenu>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- [<span data-ttu-id="7c698-111">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="7c698-111">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
