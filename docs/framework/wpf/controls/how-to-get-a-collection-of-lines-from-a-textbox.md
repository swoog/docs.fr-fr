---
title: "Procédure : Obtenir une collection de lignes à partir d'un TextBox"
ms.date: 03/30/2017
helpviewer_keywords:
- lines [WPF], getting collection of
- TextBox control [WPF], getting collection of lines
ms.assetid: a12f529d-b926-47f6-92bf-cad5f17b532a
ms.openlocfilehash: 1aa73e55a3fdfd658c6a337b598dff96244ace40
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57354191"
---
# <a name="how-to-get-a-collection-of-lines-from-a-textbox"></a><span data-ttu-id="49d6b-102">Procédure : Obtenir une collection de lignes à partir d'un TextBox</span><span class="sxs-lookup"><span data-stu-id="49d6b-102">How to: Get a Collection of Lines from a TextBox</span></span>
<span data-ttu-id="49d6b-103">Cet exemple montre comment obtenir une collection de lignes de texte à partir d’un <xref:System.Windows.Controls.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="49d6b-103">This example shows how to get a collection of lines of text from a <xref:System.Windows.Controls.TextBox>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="49d6b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="49d6b-104">Example</span></span>  
 <span data-ttu-id="49d6b-105">L’exemple suivant montre une méthode simple qui prend un <xref:System.Windows.Controls.TextBox> comme argument et retourne un <xref:System.Collections.Specialized.StringCollection> contenant les lignes de texte dans le **zone de texte**.</span><span class="sxs-lookup"><span data-stu-id="49d6b-105">The following example shows a simple method that takes a <xref:System.Windows.Controls.TextBox> as the argument, and returns a <xref:System.Collections.Specialized.StringCollection> containing the lines of text in the **TextBox**.</span></span>  <span data-ttu-id="49d6b-106">Le <xref:System.Windows.Controls.TextBox.LineCount%2A> propriété est utilisée pour déterminer le nombre de lignes n’est actuellement dans le **zone de texte**et le <xref:System.Windows.Controls.TextBox.GetLineText%2A> méthode est ensuite utilisée pour extraire chaque ligne et l’ajouter à la collection de lignes.</span><span class="sxs-lookup"><span data-stu-id="49d6b-106">The <xref:System.Windows.Controls.TextBox.LineCount%2A> property is used to determine how many lines are currently in the **TextBox**, and the <xref:System.Windows.Controls.TextBox.GetLineText%2A> method is then used to extract each line and add it to the collection of lines.</span></span>  
  
 [!code-csharp[TextBox_MiscCode#_TextBox_GetLines](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textbox_getlines)]  
  
## <a name="see-also"></a><span data-ttu-id="49d6b-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49d6b-107">See also</span></span>
- [<span data-ttu-id="49d6b-108">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="49d6b-108">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="49d6b-109">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="49d6b-109">RichTextBox Overview</span></span>](richtextbox-overview.md)
