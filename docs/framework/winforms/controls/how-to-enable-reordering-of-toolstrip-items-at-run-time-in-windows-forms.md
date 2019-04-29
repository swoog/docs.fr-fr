---
title: 'Procédure : Activer la réorganisation des éléments ToolStrip au moment de l’exécution dans les Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], examples
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], rearranging controls
- ToolStrip control [Windows Forms], reordering items
ms.assetid: 8480b69a-379f-4dc2-8dcf-365ed93692b2
ms.openlocfilehash: daff9d6d351db514d552225853f977775f8e3204
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941438"
---
# <a name="how-to-enable-reordering-of-toolstrip-items-at-run-time-in-windows-forms"></a><span data-ttu-id="a5a6a-102">Procédure : Activer la réorganisation des éléments ToolStrip au moment de l’exécution dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="a5a6a-102">How to: Enable Reordering of ToolStrip Items at Run Time in Windows Forms</span></span>
<span data-ttu-id="a5a6a-103">Vous pouvez autoriser l’utilisateur à réorganiser <xref:System.Windows.Forms.ToolStripItem> contrôle sur le <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="a5a6a-103">You can enable the user to rearrange <xref:System.Windows.Forms.ToolStripItem> controls on the <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
### <a name="to-enable-toolstripitem-rearrangement-at-run-time"></a><span data-ttu-id="a5a6a-104">Pour activer la réorganisation ToolStripItem au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="a5a6a-104">To enable ToolStripItem rearrangement at run time</span></span>  
  
- <span data-ttu-id="a5a6a-105">Affectez à la propriété <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="a5a6a-105">Set the <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> property to `true`.</span></span> <span data-ttu-id="a5a6a-106">Par défaut, <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> est `false`.</span><span class="sxs-lookup"><span data-stu-id="a5a6a-106">By default, <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A> is `false`.</span></span>  
  
     <span data-ttu-id="a5a6a-107">Au moment de l’exécution, l’utilisateur maintient enfoncée la touche ALT et le bouton gauche de la souris pour faire glisser un <xref:System.Windows.Forms.ToolStripItem> vers un autre emplacement sur le <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="a5a6a-107">At run time, the user holds down the ALT key and the left mouse button to drag a <xref:System.Windows.Forms.ToolStripItem> to a different location on the <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
    ```vb  
    toolStrip1.AllowItemReorder = True  
    ```  
  
    ```csharp  
    toolStrip1.AllowItemReorder = true;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="a5a6a-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5a6a-108">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.AllowItemReorder%2A>
- [<span data-ttu-id="a5a6a-109">Vue d’ensemble du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="a5a6a-109">ToolStrip Control Overview</span></span>](toolstrip-control-overview-windows-forms.md)
- [<span data-ttu-id="a5a6a-110">Architecture du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="a5a6a-110">ToolStrip Control Architecture</span></span>](toolstrip-control-architecture.md)
- [<span data-ttu-id="a5a6a-111">Résumé de la technologie ToolStrip</span><span class="sxs-lookup"><span data-stu-id="a5a6a-111">ToolStrip Technology Summary</span></span>](toolstrip-technology-summary.md)
