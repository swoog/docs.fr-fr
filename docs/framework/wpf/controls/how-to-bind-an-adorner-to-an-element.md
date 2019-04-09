---
title: 'Procédure : Lier un ornement à un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UIElements [WPF], binding adorners to
- adorners [WPF], binding to specified UIElements
ms.assetid: b2101611-a0ee-4137-bdb8-9b3673d2e6b9
ms.openlocfilehash: 54c9e6dfff2bbf7bfabde523b5d6ae5a623fe733
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59194719"
---
# <a name="how-to-bind-an-adorner-to-an-element"></a><span data-ttu-id="d55dc-102">Procédure : Lier un ornement à un élément</span><span class="sxs-lookup"><span data-stu-id="d55dc-102">How to: Bind an Adorner to an Element</span></span>
<span data-ttu-id="d55dc-103">Cet exemple montre comment lier par programmation un ornement à une certaine <xref:System.Windows.UIElement>.</span><span class="sxs-lookup"><span data-stu-id="d55dc-103">This example shows how to programmatically bind an adorner to a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d55dc-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="d55dc-104">Example</span></span>  
 <span data-ttu-id="d55dc-105">Pour lier un ornement à un particulier <xref:System.Windows.UIElement>, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d55dc-105">To bind an adorner to a particular <xref:System.Windows.UIElement>, follow these steps:</span></span>  
  
1.  <span data-ttu-id="d55dc-106">Appeler le `static` méthode <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> pour obtenir un <xref:System.Windows.Documents.AdornerLayer> de l’objet pour le <xref:System.Windows.UIElement> à orner.</span><span class="sxs-lookup"><span data-stu-id="d55dc-106">Call the `static` method <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> to get an <xref:System.Windows.Documents.AdornerLayer> object for the <xref:System.Windows.UIElement> to be adorned.</span></span> <xref:System.Windows.Documents.AdornerLayer.GetAdornerLayer%2A> <span data-ttu-id="d55dc-107">Remonte l’arborescence visuelle, en commençant à l’emplacement spécifié **UIElement**et retourne la première couche d’ornement qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="d55dc-107">walks up the visual tree, starting at the specified **UIElement**, and returns the first adorner layer it finds.</span></span> <span data-ttu-id="d55dc-108">(Si aucune couche d’ornement n’est trouvée, la méthode retourne Null.)</span><span class="sxs-lookup"><span data-stu-id="d55dc-108">(If no adorner layers are found, the method returns null.)</span></span>  
  
2.  <span data-ttu-id="d55dc-109">Appelez le <xref:System.Windows.Documents.AdornerLayer.Add%2A> méthode à laquelle lier l’ornement à la cible **UIElement**.</span><span class="sxs-lookup"><span data-stu-id="d55dc-109">Call the <xref:System.Windows.Documents.AdornerLayer.Add%2A> method to bind the adorner to the target **UIElement**.</span></span>  
  
 <span data-ttu-id="d55dc-110">L’exemple suivant lie un SimpleCircleAdorner (illustré ci-dessus) à un <xref:System.Windows.Controls.TextBox> nommé *myTextBox*.</span><span class="sxs-lookup"><span data-stu-id="d55dc-110">The following example binds a SimpleCircleAdorner (shown above) to a <xref:System.Windows.Controls.TextBox> named *myTextBox*.</span></span>  
  
 [!code-csharp[Adorners_SimpleCircleAdorner#_AdornSingleElement](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_adornsingleelement)]
 [!code-vb[Adorners_SimpleCircleAdorner#_AdornSingleElement](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_adornsingleelement)]  
  
> [!NOTE]
>  <span data-ttu-id="d55dc-111">L’utilisation du [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] pour lier un ornement à un autre élément n’est pas prise en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="d55dc-111">Using [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] to bind an adorner to another element is currently not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d55dc-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d55dc-112">See also</span></span>

- [<span data-ttu-id="d55dc-113">Vue d'ensemble des ornements</span><span class="sxs-lookup"><span data-stu-id="d55dc-113">Adorners Overview</span></span>](adorners-overview.md)
