---
title: 'Procédure : Mettre un contrôle TextBox en lecture seule'
ms.date: 03/30/2017
helpviewer_keywords:
- read-only TextBox controls [WPF]
- TextBox control read-only
ms.assetid: e707ec59-8b22-473e-b77c-3060a237517a
ms.openlocfilehash: 7f24458eb98bd669d59f15c49d1d9e3beb6833b1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770940"
---
# <a name="how-to-make-a-textbox-control-read-only"></a><span data-ttu-id="b5cbf-102">Procédure : Mettre un contrôle TextBox en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5cbf-102">How to: Make a TextBox Control Read-Only</span></span>
<span data-ttu-id="b5cbf-103">Cet exemple montre comment configurer un <xref:System.Windows.Controls.TextBox> contrôle pour ne pas autoriser l’entrée d’utilisateur ou la modification.</span><span class="sxs-lookup"><span data-stu-id="b5cbf-103">This example shows how to configure a <xref:System.Windows.Controls.TextBox> control to not allow user input or modification.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b5cbf-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b5cbf-104">Example</span></span>  
 <span data-ttu-id="b5cbf-105">Pour empêcher les utilisateurs de modifier le contenu d’un <xref:System.Windows.Controls.TextBox> , affectez la <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribut **true**.</span><span class="sxs-lookup"><span data-stu-id="b5cbf-105">To prevent users from modifying the contents of a <xref:System.Windows.Controls.TextBox> control, set the <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribute to **true**.</span></span>  
  
 [!code-xaml[TextBox_MiscCode#_ReadOnlyTextBoxXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_readonlytextboxxaml)]  
  
 <span data-ttu-id="b5cbf-106">Le <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribut affecte uniquement l’entrée d’utilisateur ; il n’affecte pas le texte dans le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] description d’un <xref:System.Windows.Controls.TextBox> contrôle ou texte est définie par programmation via la <xref:System.Windows.Controls.TextBox.Text%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="b5cbf-106">The <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribute affects user input only; it does not affect text set in the [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] description of a <xref:System.Windows.Controls.TextBox> control, or text set programmatically through the <xref:System.Windows.Controls.TextBox.Text%2A> property.</span></span>  
  
 <span data-ttu-id="b5cbf-107">La valeur par défaut <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> est **false**.</span><span class="sxs-lookup"><span data-stu-id="b5cbf-107">The default value of <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> is **false**.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5cbf-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5cbf-108">See also</span></span>

- [<span data-ttu-id="b5cbf-109">Vue d’ensemble de TextBox</span><span class="sxs-lookup"><span data-stu-id="b5cbf-109">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="b5cbf-110">Vue d’ensemble de RichTextBox</span><span class="sxs-lookup"><span data-stu-id="b5cbf-110">RichTextBox Overview</span></span>](richtextbox-overview.md)
