---
title: 'Comment : définir le focus dans un contrôle TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- focus [WPF], setting
- TextBox control [WPF], setting focus
ms.assetid: 24b61b45-dc2d-425e-9839-b017af7ab86f
ms.openlocfilehash: 1bda01a3d330ad384c2f922ff3c7679e10d0f148
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33552537"
---
# <a name="how-to-set-focus-in-a-textbox-control"></a><span data-ttu-id="69c2c-102">Comment : définir le focus dans un contrôle TextBox</span><span class="sxs-lookup"><span data-stu-id="69c2c-102">How to: Set Focus in a TextBox Control</span></span>
<span data-ttu-id="69c2c-103">Cet exemple montre comment utiliser le <xref:System.Windows.UIElement.Focus%2A> pour définir le focus sur un <xref:System.Windows.Controls.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="69c2c-103">This example shows how to use the <xref:System.Windows.UIElement.Focus%2A> method to set focus on a <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="69c2c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="69c2c-104">Example</span></span>  
 <span data-ttu-id="69c2c-105">Les éléments suivants [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemple décrit une simple <xref:System.Windows.Controls.TextBox> contrôle nommé *tbFocusMe*</span><span class="sxs-lookup"><span data-stu-id="69c2c-105">The following [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] example describes a simple <xref:System.Windows.Controls.TextBox> control named *tbFocusMe*</span></span>  
  
 [!code-xaml[TextBox_MiscCode#_TextBoxFocusXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textboxfocusxaml)]  
  
## <a name="example"></a><span data-ttu-id="69c2c-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="69c2c-106">Example</span></span>  
 <span data-ttu-id="69c2c-107">L’exemple suivant appelle la <xref:System.Windows.UIElement.Focus%2A> pour définir le focus sur le <xref:System.Windows.Controls.TextBox> contrôle avec le nom *tbFocusMe*.</span><span class="sxs-lookup"><span data-stu-id="69c2c-107">The following example calls the <xref:System.Windows.UIElement.Focus%2A> method to set the focus on the <xref:System.Windows.Controls.TextBox> control with the Name *tbFocusMe*.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_FocusTextBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_focustextbox)]
 [!code-vb[TextBox_MiscCode#_FocusTextBox](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_focustextbox)]  
  
## <a name="see-also"></a><span data-ttu-id="69c2c-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69c2c-108">See Also</span></span>  
 <xref:System.Windows.UIElement.Focusable%2A>  
 <xref:System.Windows.UIElement.IsFocused%2A>  
 [<span data-ttu-id="69c2c-109">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="69c2c-109">TextBox Overview</span></span>](../../../../docs/framework/wpf/controls/textbox-overview.md)  
 [<span data-ttu-id="69c2c-110">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="69c2c-110">RichTextBox Overview</span></span>](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
