---
title: 'Comment : lier un ornement à un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UIElements [WPF], binding adorners to
- adorners [WPF], binding to specified UIElements
ms.assetid: b2101611-a0ee-4137-bdb8-9b3673d2e6b9
ms.openlocfilehash: fb419ee5a57e81e7e3bc72ae04fd200703b80cd3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33552550"
---
# <a name="how-to-bind-an-adorner-to-an-element"></a><span data-ttu-id="7ee63-102">Comment : lier un ornement à un élément</span><span class="sxs-lookup"><span data-stu-id="7ee63-102">How to: Bind an Adorner to an Element</span></span>
<span data-ttu-id="7ee63-103">Cet exemple montre comment lier par programmation un ornement spécifié <xref:System.Windows.UIElement>.</span><span class="sxs-lookup"><span data-stu-id="7ee63-103">This example shows how to programmatically bind an adorner to a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7ee63-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="7ee63-104">Example</span></span>  
 <span data-ttu-id="7ee63-105">Pour lier un ornement à un emplacement donné <xref:System.Windows.UIElement>, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7ee63-105">To bind an adorner to a particular <xref:System.Windows.UIElement>, follow these steps:</span></span>  
  
1.  <span data-ttu-id="7ee63-106">Appeler le `static` méthode <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> pour obtenir un <xref:System.Windows.Documents.AdornerLayer> de l’objet pour le <xref:System.Windows.UIElement> à orner.</span><span class="sxs-lookup"><span data-stu-id="7ee63-106">Call the `static` method <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> to get an <xref:System.Windows.Documents.AdornerLayer> object for the <xref:System.Windows.UIElement> to be adorned.</span></span> <span data-ttu-id="7ee63-107"><xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> parcourt l’arborescence d’éléments visuels, en commençant à la position spécifiée **UIElement**et retourne la première couche d’ornement qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="7ee63-107"><xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> walks up the visual tree, starting at the specified **UIElement**, and returns the first adorner layer it finds.</span></span> <span data-ttu-id="7ee63-108">(Si aucune couche d’ornement n’est trouvée, la méthode retourne Null.)</span><span class="sxs-lookup"><span data-stu-id="7ee63-108">(If no adorner layers are found, the method returns null.)</span></span>  
  
2.  <span data-ttu-id="7ee63-109">Appelez le <xref:System.Windows.Documents.AdornerLayer.Add%2A> méthode à laquelle lier l’ornement à la cible **UIElement**.</span><span class="sxs-lookup"><span data-stu-id="7ee63-109">Call the <xref:System.Windows.Documents.AdornerLayer.Add%2A> method to bind the adorner to the target **UIElement**.</span></span>  
  
 <span data-ttu-id="7ee63-110">L’exemple suivant lie un SimpleCircleAdorner (illustré ci-dessus) pour un <xref:System.Windows.Controls.TextBox> nommé *myTextBox*.</span><span class="sxs-lookup"><span data-stu-id="7ee63-110">The following example binds a SimpleCircleAdorner (shown above) to a <xref:System.Windows.Controls.TextBox> named *myTextBox*.</span></span>  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornSingleElement](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornsingleelement)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornSingleElement](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornsingleelement)]  
  
> [!NOTE]
>  <span data-ttu-id="7ee63-111">L’utilisation du [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] pour lier un ornement à un autre élément n’est pas prise en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="7ee63-111">Using [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] to bind an adorner to another element is currently not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7ee63-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ee63-112">See Also</span></span>  
 [<span data-ttu-id="7ee63-113">Vue d’ensemble des ornements</span><span class="sxs-lookup"><span data-stu-id="7ee63-113">Adorners Overview</span></span>](../../../../docs/framework/wpf/controls/adorners-overview.md)
