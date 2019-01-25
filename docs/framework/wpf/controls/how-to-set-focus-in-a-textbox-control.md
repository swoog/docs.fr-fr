---
title: 'Procédure : Définir le focus dans un contrôle TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- focus [WPF], setting
- TextBox control [WPF], setting focus
ms.assetid: 24b61b45-dc2d-425e-9839-b017af7ab86f
ms.openlocfilehash: 1ab7fa5f5ce895d163e3db3dd020fee3f29b7153
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54590706"
---
# <a name="how-to-set-focus-in-a-textbox-control"></a><span data-ttu-id="4f2cb-102">Procédure : Définir le focus dans un contrôle TextBox</span><span class="sxs-lookup"><span data-stu-id="4f2cb-102">How to: Set Focus in a TextBox Control</span></span>
<span data-ttu-id="4f2cb-103">Cet exemple montre comment utiliser le <xref:System.Windows.UIElement.Focus%2A> méthode pour définir le focus sur un <xref:System.Windows.Controls.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4f2cb-103">This example shows how to use the <xref:System.Windows.UIElement.Focus%2A> method to set focus on a <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f2cb-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="4f2cb-104">Example</span></span>  
 <span data-ttu-id="4f2cb-105">Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemple décrit une simple <xref:System.Windows.Controls.TextBox> contrôle nommé *tbFocusMe*</span><span class="sxs-lookup"><span data-stu-id="4f2cb-105">The following [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] example describes a simple <xref:System.Windows.Controls.TextBox> control named *tbFocusMe*</span></span>  
  
 [!code-xaml[TextBox_MiscCode#_TextBoxFocusXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textboxfocusxaml)]  
  
## <a name="example"></a><span data-ttu-id="4f2cb-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="4f2cb-106">Example</span></span>  
 <span data-ttu-id="4f2cb-107">L’exemple suivant appelle la <xref:System.Windows.UIElement.Focus%2A> méthode pour définir le focus sur le <xref:System.Windows.Controls.TextBox> contrôle portant le nom *tbFocusMe*.</span><span class="sxs-lookup"><span data-stu-id="4f2cb-107">The following example calls the <xref:System.Windows.UIElement.Focus%2A> method to set the focus on the <xref:System.Windows.Controls.TextBox> control with the Name *tbFocusMe*.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_FocusTextBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_focustextbox)]
 [!code-vb[TextBox_MiscCode#_FocusTextBox](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_focustextbox)]  
  
## <a name="see-also"></a><span data-ttu-id="4f2cb-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f2cb-108">See also</span></span>
- <xref:System.Windows.UIElement.Focusable%2A>
- <xref:System.Windows.UIElement.IsFocused%2A>
- [<span data-ttu-id="4f2cb-109">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="4f2cb-109">TextBox Overview</span></span>](../../../../docs/framework/wpf/controls/textbox-overview.md)
- [<span data-ttu-id="4f2cb-110">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="4f2cb-110">RichTextBox Overview</span></span>](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
