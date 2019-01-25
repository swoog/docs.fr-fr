---
title: 'Procédure : Définir un modèle GroupBox'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], GroupBox
- GroupBox control [WPF], creating templates
ms.assetid: 85a4d1a7-4753-4f4a-b26d-14fa10c1ddb5
ms.openlocfilehash: 0e1b0487629bba3550a8b6b4a31c163a7ade6a87
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54743720"
---
# <a name="how-to-define-a-groupbox-template"></a><span data-ttu-id="739d2-102">Procédure : Définir un modèle GroupBox</span><span class="sxs-lookup"><span data-stu-id="739d2-102">How to: Define a GroupBox Template</span></span>
<span data-ttu-id="739d2-103">Cet exemple montre comment créer un modèle pour un <xref:System.Windows.Controls.GroupBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="739d2-103">This example shows how to create a template for a <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="739d2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="739d2-104">Example</span></span>  
 <span data-ttu-id="739d2-105">L’exemple suivant définit un <xref:System.Windows.Controls.GroupBox> modèle de contrôle à l’aide un <xref:System.Windows.Controls.Grid> contrôle de disposition.</span><span class="sxs-lookup"><span data-stu-id="739d2-105">The following example defines a <xref:System.Windows.Controls.GroupBox> control template by using a <xref:System.Windows.Controls.Grid> control for layout.</span></span> <span data-ttu-id="739d2-106">Le modèle utilise un <xref:System.Windows.Controls.BorderGapMaskConverter> pour définir la bordure de la <xref:System.Windows.Controls.GroupBox> afin que la bordure ne masque pas le <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> contenu.</span><span class="sxs-lookup"><span data-stu-id="739d2-106">The template uses a <xref:System.Windows.Controls.BorderGapMaskConverter> to define the border of the <xref:System.Windows.Controls.GroupBox> so that the border does not obscure the <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> content.</span></span>  
  
 [!code-xaml[GroupBoxSnippet#GroupBoxTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GroupBoxSnippet/CS/Window1.xaml#groupboxtemplate)]  
  
## <a name="see-also"></a><span data-ttu-id="739d2-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="739d2-107">See also</span></span>
- <xref:System.Windows.Controls.GroupBox>
- [<span data-ttu-id="739d2-108">Rubriques Comment relatives GroupBox</span><span class="sxs-lookup"><span data-stu-id="739d2-108">GroupBox How-to Topics</span></span>](https://msdn.microsoft.com/library/7692e155-a4c6-428c-b7e0-64b3740daca7)
