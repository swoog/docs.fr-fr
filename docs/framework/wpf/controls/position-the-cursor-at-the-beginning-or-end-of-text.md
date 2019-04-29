---
title: 'Procédure : Positionner le curseur au début ou à la fin du texte dans un contrôle TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- positioning cursor [WPF]
- TextBox control [WPF], positioning cursor
- cursor [WPF], positioning
ms.assetid: c771a0b8-c6b4-4240-aecd-a21d0ba51a2e
ms.openlocfilehash: 3d7da5daf09e06938b8366e0f5f98a599cae4571
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770589"
---
# <a name="how-to-position-the-cursor-at-the-beginning-or-end-of-text-in-a-textbox-control"></a><span data-ttu-id="a91f8-102">Procédure : Positionner le curseur au début ou à la fin du texte dans un contrôle TextBox</span><span class="sxs-lookup"><span data-stu-id="a91f8-102">How to: Position the Cursor at the Beginning or End of Text in a TextBox Control</span></span>
<span data-ttu-id="a91f8-103">Cet exemple montre comment positionner le curseur au début ou à la fin du contenu texte d’un <xref:System.Windows.Controls.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="a91f8-103">This example shows how to position the cursor at the beginning or end of the text contents of a <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a91f8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a91f8-104">Example</span></span>  
 <span data-ttu-id="a91f8-105">Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] code décrit un <xref:System.Windows.Controls.TextBox> contrôler et lui assigne un nom.</span><span class="sxs-lookup"><span data-stu-id="a91f8-105">The following [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] code describes a <xref:System.Windows.Controls.TextBox> control and assigns it a Name.</span></span>  
  
 [!code-xaml[TextBox_MiscCode#_MoveCursorXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_movecursorxaml)]  
  
## <a name="example"></a><span data-ttu-id="a91f8-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="a91f8-106">Example</span></span>  
 <span data-ttu-id="a91f8-107">Pour positionner le curseur au début du contenu d’un <xref:System.Windows.Controls.TextBox> contrôler, appelez le <xref:System.Windows.Controls.TextBox.Select%2A> (méthode) et spécifiez la sélection de position de départ de 0 et une longueur de sélection 0.</span><span class="sxs-lookup"><span data-stu-id="a91f8-107">To position the cursor at the beginning of the contents of a <xref:System.Windows.Controls.TextBox> control, call the <xref:System.Windows.Controls.TextBox.Select%2A> method and specify the selection start position of 0, and a selection length of 0.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_CursorToStart](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_cursortostart)]
 [!code-vb[TextBox_MiscCode#_CursorToStart](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_cursortostart)]  
  
## <a name="example"></a><span data-ttu-id="a91f8-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="a91f8-108">Example</span></span>  
 <span data-ttu-id="a91f8-109">Pour positionner le curseur à la fin du contenu d’un <xref:System.Windows.Controls.TextBox> contrôler, appelez le <xref:System.Windows.Controls.TextBox.Select%2A> (méthode) et spécifier la position de départ de sélection égale à la longueur du contenu texte et une longueur de sélection 0.</span><span class="sxs-lookup"><span data-stu-id="a91f8-109">To position the cursor at the end of the contents of a <xref:System.Windows.Controls.TextBox> control, call the <xref:System.Windows.Controls.TextBox.Select%2A> method and specify the selection start position equal to the  length of the text content, and a selection length of 0.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_CursorToEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_cursortoend)]
 [!code-vb[TextBox_MiscCode#_CursorToEnd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_cursortoend)]  
  
## <a name="see-also"></a><span data-ttu-id="a91f8-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a91f8-110">See also</span></span>

- [<span data-ttu-id="a91f8-111">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="a91f8-111">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="a91f8-112">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="a91f8-112">RichTextBox Overview</span></span>](richtextbox-overview.md)
