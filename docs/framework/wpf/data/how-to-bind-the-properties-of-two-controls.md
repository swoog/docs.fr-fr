---
title: 'Comment : lier les propriétés de deux contrôles'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], binding properties of two controls
- binding properties of two controls [WPF]
- controls [WPF], binding properties of
ms.assetid: 06318fac-6afd-4c7d-a277-6d7ef50f47bc
ms.openlocfilehash: 02e71bfcc41fc3d256ea95381ed27d36b289b8f8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33555579"
---
# <a name="how-to-bind-the-properties-of-two-controls"></a><span data-ttu-id="770a5-102">Comment : lier les propriétés de deux contrôles</span><span class="sxs-lookup"><span data-stu-id="770a5-102">How to: Bind the Properties of Two Controls</span></span>
<span data-ttu-id="770a5-103">Cet exemple montre comment lier la propriété d’un contrôle instancié à celle d’un autre à l’aide de la <xref:System.Windows.Data.Binding.ElementName%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="770a5-103">This example shows how to bind the property of one instantiated control to that of another using the <xref:System.Windows.Data.Binding.ElementName%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="770a5-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="770a5-104">Example</span></span>  
 <span data-ttu-id="770a5-105">L’exemple suivant montre comment lier le <xref:System.Windows.Controls.Panel.Background%2A> propriété d’un <xref:System.Windows.Controls.Canvas> à la <xref:System.Windows.Controls.Primitives.Selector.SelectedItem%2A>.<xref:System.Windows.Controls.ContentControl.Content%2A></span><span class="sxs-lookup"><span data-stu-id="770a5-105">The following example shows how to bind the <xref:System.Windows.Controls.Panel.Background%2A> property of a <xref:System.Windows.Controls.Canvas> to the <xref:System.Windows.Controls.Primitives.Selector.SelectedItem%2A>.<xref:System.Windows.Controls.ContentControl.Content%2A></span></span> <span data-ttu-id="770a5-106">propriété d’un <xref:System.Windows.Controls.ComboBox>:</span><span class="sxs-lookup"><span data-stu-id="770a5-106">property of a <xref:System.Windows.Controls.ComboBox>:</span></span>  
  
 [!code-xaml[BindDptoDp#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BindDPtoDP/CS/Window1.xaml#1)]  
  
 <span data-ttu-id="770a5-107">Lors de l’affichage, on obtient un résultat similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="770a5-107">When this example is rendered it looks like the following:</span></span>  
  
 <span data-ttu-id="770a5-108">![Canevas avec arrière-plan vert](../../../../docs/framework/wpf/data/media/databindingbindingdpssample.PNG "DataBindingBindingDPsSample")</span><span class="sxs-lookup"><span data-stu-id="770a5-108">![A canvas with a green background](../../../../docs/framework/wpf/data/media/databindingbindingdpssample.PNG "DataBindingBindingDPsSample")</span></span>  
  
 <span data-ttu-id="770a5-109">**Remarque** la propriété de cible de liaison (dans cet exemple, le <xref:System.Windows.Controls.Panel.Background%2A> propriété) doit être une propriété de dépendance.</span><span class="sxs-lookup"><span data-stu-id="770a5-109">**Note** The binding target property (in this example, the <xref:System.Windows.Controls.Panel.Background%2A> property) must be a dependency property.</span></span> <span data-ttu-id="770a5-110">Pour plus d’informations, consultez [Vue d’ensemble de la liaison de données](../../../../docs/framework/wpf/data/data-binding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="770a5-110">For more information, see [Data Binding Overview](../../../../docs/framework/wpf/data/data-binding-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="770a5-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="770a5-111">See Also</span></span>  
 [<span data-ttu-id="770a5-112">Spécifier la source de liaison</span><span class="sxs-lookup"><span data-stu-id="770a5-112">Specify the Binding Source</span></span>](../../../../docs/framework/wpf/data/how-to-specify-the-binding-source.md)  
 [<span data-ttu-id="770a5-113">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="770a5-113">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
