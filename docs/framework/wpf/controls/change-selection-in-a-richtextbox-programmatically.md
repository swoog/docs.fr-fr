---
title: Modification par programmation de la sélection dans un RichTextBox
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- changing selections in a text box [WPF]
- changing selections in a RichTextBox [WPF]
ms.assetid: f1213205-1ad7-4cd2-b115-460173cc5aa3
ms.openlocfilehash: a85dc4baa8a59d25f577996c541a422bbe2af24e
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57367074"
---
# <a name="change-selection-in-a-richtextbox-programmatically"></a><span data-ttu-id="bf51c-102">Modification par programmation de la sélection dans un RichTextBox</span><span class="sxs-lookup"><span data-stu-id="bf51c-102">Change Selection in a RichTextBox Programmatically</span></span>
<span data-ttu-id="bf51c-103">Cet exemple montre comment modifier par programme la sélection actuelle dans un <xref:System.Windows.Controls.RichTextBox>.</span><span class="sxs-lookup"><span data-stu-id="bf51c-103">This example shows how to programmatically change the current selection in a <xref:System.Windows.Controls.RichTextBox>.</span></span> <span data-ttu-id="bf51c-104">Cette sélection est le même que si l’utilisateur a sélectionné le contenu à l’aide de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bf51c-104">This selection is the same as if the user had selected the content by using the user interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bf51c-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="bf51c-105">Example</span></span>  
 <span data-ttu-id="bf51c-106">Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] code décrit une nommée <xref:System.Windows.Controls.RichTextBox> contrôle avec du contenu simple.</span><span class="sxs-lookup"><span data-stu-id="bf51c-106">The following [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] code describes a named <xref:System.Windows.Controls.RichTextBox> control with simple content.</span></span>  
  
 [!code-xaml[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/CSharp/ChangeSelectionProgrammaticaly.xaml#changeselectionprogrammaticalyexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="bf51c-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="bf51c-107">Example</span></span>  
 <span data-ttu-id="bf51c-108">Le code suivant sélectionne par programme du texte arbitraire lorsque l’utilisateur clique à l’intérieur de la <xref:System.Windows.Controls.RichTextBox>.</span><span class="sxs-lookup"><span data-stu-id="bf51c-108">The following code programmatically selects some arbitrary text when the user clicks inside the <xref:System.Windows.Controls.RichTextBox>.</span></span>  
  
 [!code-csharp[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/CSharp/ChangeSelectionProgrammaticaly.xaml.cs#changeselectionprogrammaticalycodeexamplewholepage)]
 [!code-vb[RichTextBoxMiscSnippets_snip#ChangeSelectionProgrammaticalyCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBoxMiscSnippets_snip/VisualBasic/ChangeSelectionProgrammaticaly.xaml.vb#changeselectionprogrammaticalycodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="bf51c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf51c-109">See also</span></span>
- [<span data-ttu-id="bf51c-110">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="bf51c-110">RichTextBox Overview</span></span>](richtextbox-overview.md)
- [<span data-ttu-id="bf51c-111">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="bf51c-111">TextBox Overview</span></span>](textbox-overview.md)
