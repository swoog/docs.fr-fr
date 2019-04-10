---
title: 'Procédure : Lier les propriétés de deux contrôles'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], binding properties of two controls
- binding properties of two controls [WPF]
- controls [WPF], binding properties of
ms.assetid: 06318fac-6afd-4c7d-a277-6d7ef50f47bc
ms.openlocfilehash: 0dd7b817b632758cfca8b5c45d88e333510485f6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59222059"
---
# <a name="how-to-bind-the-properties-of-two-controls"></a><span data-ttu-id="648a6-102">Procédure : Lier les propriétés de deux contrôles</span><span class="sxs-lookup"><span data-stu-id="648a6-102">How to: Bind the Properties of Two Controls</span></span>
<span data-ttu-id="648a6-103">Cet exemple montre comment lier la propriété d’un contrôle instancié à celle d’un autre en utilisant le <xref:System.Windows.Data.Binding.ElementName%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="648a6-103">This example shows how to bind the property of one instantiated control to that of another using the <xref:System.Windows.Data.Binding.ElementName%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="648a6-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="648a6-104">Example</span></span>  
 <span data-ttu-id="648a6-105">L’exemple suivant montre comment lier le <xref:System.Windows.Controls.Panel.Background%2A> propriété d’un <xref:System.Windows.Controls.Canvas> à la <xref:System.Windows.Controls.Primitives.Selector.SelectedItem%2A>.</span><span class="sxs-lookup"><span data-stu-id="648a6-105">The following example shows how to bind the <xref:System.Windows.Controls.Panel.Background%2A> property of a <xref:System.Windows.Controls.Canvas> to the <xref:System.Windows.Controls.Primitives.Selector.SelectedItem%2A>.</span></span><xref:System.Windows.Controls.ContentControl.Content%2A> <span data-ttu-id="648a6-106">propriété d’un <xref:System.Windows.Controls.ComboBox>:</span><span class="sxs-lookup"><span data-stu-id="648a6-106">property of a <xref:System.Windows.Controls.ComboBox>:</span></span>  
  
 [!code-xaml[BindDptoDp#1](~/samples/snippets/csharp/VS_Snippets_Wpf/BindDPtoDP/CS/Window1.xaml#1)]  
  
 <span data-ttu-id="648a6-107">Lors de l’affichage, on obtient un résultat similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="648a6-107">When this example is rendered it looks like the following:</span></span>  
  
 <span data-ttu-id="648a6-108">![Canevas avec arrière-plan vert](./media/databindingbindingdpssample.PNG "DataBindingBindingDPsSample")</span><span class="sxs-lookup"><span data-stu-id="648a6-108">![A canvas with a green background](./media/databindingbindingdpssample.PNG "DataBindingBindingDPsSample")</span></span>  
  
 <span data-ttu-id="648a6-109">**Remarque** la propriété de cible de liaison (dans cet exemple, le <xref:System.Windows.Controls.Panel.Background%2A> propriété) doit être une propriété de dépendance.</span><span class="sxs-lookup"><span data-stu-id="648a6-109">**Note** The binding target property (in this example, the <xref:System.Windows.Controls.Panel.Background%2A> property) must be a dependency property.</span></span> <span data-ttu-id="648a6-110">Pour plus d’informations, consultez [Vue d’ensemble de la liaison de données](data-binding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="648a6-110">For more information, see [Data Binding Overview](data-binding-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="648a6-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="648a6-111">See also</span></span>

- [<span data-ttu-id="648a6-112">Spécifier la source de liaison</span><span class="sxs-lookup"><span data-stu-id="648a6-112">Specify the Binding Source</span></span>](how-to-specify-the-binding-source.md)
- [<span data-ttu-id="648a6-113">Rubriques Comment</span><span class="sxs-lookup"><span data-stu-id="648a6-113">How-to Topics</span></span>](data-binding-how-to-topics.md)
