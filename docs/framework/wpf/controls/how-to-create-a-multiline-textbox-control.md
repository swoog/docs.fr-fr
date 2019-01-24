---
title: 'Procédure : Créer un contrôle TextBox multiligne'
ms.date: 03/30/2017
helpviewer_keywords:
- TextBox control [WPF], multiple lines of text
ms.assetid: 05914a93-d0ea-4a9a-b693-09df7d4e2ac2
ms.openlocfilehash: ca1b499b2acdfd9fd2ff0f57f2b0c07d7da10789
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517823"
---
# <a name="how-to-create-a-multiline-textbox-control"></a><span data-ttu-id="154f1-102">Procédure : Créer un contrôle TextBox multiligne</span><span class="sxs-lookup"><span data-stu-id="154f1-102">How to: Create a Multiline TextBox Control</span></span>
<span data-ttu-id="154f1-103">Cet exemple montre comment utiliser [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] pour définir un <xref:System.Windows.Controls.TextBox> contrôle s’étend automatiquement pour s’adapter à plusieurs lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="154f1-103">This example shows how to use [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] to define a <xref:System.Windows.Controls.TextBox> control that will automatically expand to accommodate multiple lines of text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="154f1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="154f1-104">Example</span></span>  
 <span data-ttu-id="154f1-105">Définissant le <xref:System.Windows.Controls.TextBox.TextWrapping%2A> attribut **encapsuler** amène le texte entré à la ligne vers une nouvelle ligne lorsque le bord de la <xref:System.Windows.Controls.TextBox> contrôle est atteint, agrandissant automatiquement le <xref:System.Windows.Controls.TextBox> contrôle pour faire de la place pour une nouvelle ligne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="154f1-105">Setting the <xref:System.Windows.Controls.TextBox.TextWrapping%2A> attribute to **Wrap** will cause entered text to wrap to a new line when the edge of the <xref:System.Windows.Controls.TextBox> control is reached, automatically expanding the <xref:System.Windows.Controls.TextBox> control to include room for a new line, if necessary.</span></span>  
  
 <span data-ttu-id="154f1-106">Définition de la <xref:System.Windows.Controls.Primitives.TextBoxBase.AcceptsReturn%2A> attribut **true** provoque une nouvelle ligne à insérer lorsque la touche retour est enfoncée, développer une fois encore automatiquement le <xref:System.Windows.Controls.TextBox> à faire de la place pour une nouvelle ligne, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="154f1-106">Setting the <xref:System.Windows.Controls.Primitives.TextBoxBase.AcceptsReturn%2A> attribute to **true** causes a new line to be inserted when the RETURN key is pressed, once again automatically expanding the <xref:System.Windows.Controls.TextBox> to include room for a new line, if necessary.</span></span>  
  
 <span data-ttu-id="154f1-107">Le <xref:System.Windows.Controls.Primitives.TextBoxBase.VerticalScrollBarVisibility%2A> attribut ajoute une barre de défilement à la <xref:System.Windows.Controls.TextBox>, de sorte que le contenu de la <xref:System.Windows.Controls.TextBox> puisse être défilé si le <xref:System.Windows.Controls.TextBox> s’étend au-delà de la taille du cadre ou de la fenêtre qui l’entoure.</span><span class="sxs-lookup"><span data-stu-id="154f1-107">The <xref:System.Windows.Controls.Primitives.TextBoxBase.VerticalScrollBarVisibility%2A> attribute adds a scroll bar to the <xref:System.Windows.Controls.TextBox>, so that the contents of the <xref:System.Windows.Controls.TextBox> can be scrolled through if the <xref:System.Windows.Controls.TextBox> expands beyond the size of the frame or window that encloses it.</span></span>  
  
 [!code-xaml[TextBox_MiscCode#_MultilineTextBoxXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_multilinetextboxxaml)]  
  
## <a name="see-also"></a><span data-ttu-id="154f1-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="154f1-108">See also</span></span>
- <xref:System.Windows.TextWrapping>
- [<span data-ttu-id="154f1-109">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="154f1-109">TextBox Overview</span></span>](../../../../docs/framework/wpf/controls/textbox-overview.md)
- [<span data-ttu-id="154f1-110">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="154f1-110">RichTextBox Overview</span></span>](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
