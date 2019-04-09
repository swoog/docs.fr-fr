---
title: 'Procédure : Positionner un menu contextuel personnalisé dans un RichTextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom context menus [WPF], positioning
- positioning custom context menus [WPF]
- RichTextBox control [WPF], positioning custom context menus
- context menus [WPF], positioning
ms.assetid: bf77c930-a546-4573-9a56-9af345ba189a
ms.openlocfilehash: f9407f59c3daafd09fa5b84006f33ef2f3ebd31f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59209422"
---
# <a name="how-to-position-a-custom-context-menu-in-a-richtextbox"></a><span data-ttu-id="fc4f4-102">Procédure : Positionner un menu contextuel personnalisé dans un RichTextBox</span><span class="sxs-lookup"><span data-stu-id="fc4f4-102">How to: Position a Custom Context Menu in a RichTextBox</span></span>
<span data-ttu-id="fc4f4-103">Cet exemple montre comment positionner un menu contextuel personnalisé pour un <xref:System.Windows.Controls.RichTextBox>.</span><span class="sxs-lookup"><span data-stu-id="fc4f4-103">This example shows how to position a custom context menu for a <xref:System.Windows.Controls.RichTextBox>.</span></span>  
  
 <span data-ttu-id="fc4f4-104">Lorsque vous implémentez un menu contextuel personnalisé pour un **RichTextBox**, il vous appartient de gérer le positionnement du menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fc4f4-104">When you implement a custom context menu for a **RichTextBox**, you are responsible for handling the placement of the context menu.</span></span>  <span data-ttu-id="fc4f4-105">Par défaut, un menu contextuel personnalisé s’ouvre au centre du **RichTextBox**.</span><span class="sxs-lookup"><span data-stu-id="fc4f4-105">By default, a custom context menu is opened at the center of the **RichTextBox**.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fc4f4-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc4f4-106">Example</span></span>  
 <span data-ttu-id="fc4f4-107">Pour remplacer le comportement de positionnement par défaut, ajoutez un écouteur pour le <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> événement.</span><span class="sxs-lookup"><span data-stu-id="fc4f4-107">To override the default placement behavior, add a listener for the <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> event.</span></span>  <span data-ttu-id="fc4f4-108">L’exemple suivant montre comment procéder par programme.</span><span class="sxs-lookup"><span data-stu-id="fc4f4-108">The following example shows how to do this programmatically.</span></span>  
  
 [!code-csharp[RichTextBox_ContextMenu#_AddListener](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_addlistener)]
 [!code-vb[RichTextBox_ContextMenu#_AddListener](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_addlistener)]  
  
## <a name="example"></a><span data-ttu-id="fc4f4-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc4f4-109">Example</span></span>  
 <span data-ttu-id="fc4f4-110">L’exemple suivant illustre une implémentation correspondante <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> écouteur d’événements.</span><span class="sxs-lookup"><span data-stu-id="fc4f4-110">The following example shows an implementation the corresponding <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> event listener.</span></span>  
  
 [!code-csharp[RichTextBox_ContextMenu#_ListenerBody](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_listenerbody)]
 [!code-vb[RichTextBox_ContextMenu#_ListenerBody](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_listenerbody)]  
  
## <a name="see-also"></a><span data-ttu-id="fc4f4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc4f4-111">See also</span></span>

- [<span data-ttu-id="fc4f4-112">Vue d'ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="fc4f4-112">RichTextBox Overview</span></span>](richtextbox-overview.md)
- [<span data-ttu-id="fc4f4-113">Vue d'ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="fc4f4-113">TextBox Overview</span></span>](textbox-overview.md)
