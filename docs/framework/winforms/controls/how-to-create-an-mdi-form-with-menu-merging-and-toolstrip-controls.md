---
title: 'Procédure : créer un formulaire MDI avec la fusion des menus et des contrôles ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripPanel control [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
ms.assetid: 64992ed9-44af-4baf-b45f-863e6ab35711
ms.openlocfilehash: 0edcc27968c55908cda0e881ed66f83323316711
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591308"
---
# <a name="how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls"></a><span data-ttu-id="bc52f-102">Procédure : créer un formulaire MDI avec la fusion des menus et des contrôles ToolStrip</span><span class="sxs-lookup"><span data-stu-id="bc52f-102">How to: Create an MDI Form with Menu Merging and ToolStrip Controls</span></span>
<span data-ttu-id="bc52f-103">L'espace de noms <xref:System.Windows.Forms?displayProperty=nameWithType> prend en charge plusieurs applications MDI (Multiple Document Interface) et le contrôle <xref:System.Windows.Forms.MenuStrip> prend en charge la fusion de menus.</span><span class="sxs-lookup"><span data-stu-id="bc52f-103">The <xref:System.Windows.Forms?displayProperty=nameWithType> namespace supports multiple document interface (MDI) applications, and the <xref:System.Windows.Forms.MenuStrip> control supports menu merging.</span></span> <span data-ttu-id="bc52f-104">Les formulaires MDI peuvent également contenir des contrôles <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="bc52f-104">MDI forms can also <xref:System.Windows.Forms.ToolStrip> controls.</span></span>  
  
 <span data-ttu-id="bc52f-105">Il existe une prise en charge étendue pour cette fonctionnalité dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bc52f-105">There is extensive support for this feature in Visual Studio.</span></span>  
  
 <span data-ttu-id="bc52f-106">Consultez également [procédure pas à pas : Création d’un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="bc52f-106">Also see [Walkthrough: Creating an MDI Form with Menu Merging and ToolStrip Controls](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc52f-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="bc52f-107">Example</span></span>  
 <span data-ttu-id="bc52f-108">L'exemple de code suivant montre comment utiliser des contrôles <xref:System.Windows.Forms.ToolStripPanel> avec un formulaire MDI.</span><span class="sxs-lookup"><span data-stu-id="bc52f-108">The following code example demonstrates how to use <xref:System.Windows.Forms.ToolStripPanel> controls with an MDI form.</span></span> <span data-ttu-id="bc52f-109">Le formulaire prend également en charge la fusion de menus avec les menus enfants.</span><span class="sxs-lookup"><span data-stu-id="bc52f-109">The form also supports menu merging with child menus.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.MdiForm#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.MdiForm#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="bc52f-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="bc52f-110">Compiling the Code</span></span>  
 <span data-ttu-id="bc52f-111">Cet exemple de code nécessite :</span><span class="sxs-lookup"><span data-stu-id="bc52f-111">This code example requires:</span></span>  
  
- <span data-ttu-id="bc52f-112">Références aux assemblys System.Drawing et System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="bc52f-112">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc52f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc52f-113">See also</span></span>

- [<span data-ttu-id="bc52f-114">Contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="bc52f-114">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
