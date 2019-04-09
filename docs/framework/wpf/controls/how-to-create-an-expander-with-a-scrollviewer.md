---
title: 'Procédure : Créer un Expander avec un ScrollViewer'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], Expander
- ScrollViewer control [WPF], with Expander control
- Expander control [WPF], creating
- controls [WPF], ScrollViewer
ms.assetid: 2ad124d2-2406-4157-aaf2-64e067298f01
ms.openlocfilehash: ef0bc5d344f7d465de9209708430d3e61d40d4f7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59114648"
---
# <a name="how-to-create-an-expander-with-a-scrollviewer"></a><span data-ttu-id="cb740-102">Procédure : Créer un Expander avec un ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="cb740-102">How to: Create an Expander with a ScrollViewer</span></span>
<span data-ttu-id="cb740-103">Cet exemple montre comment créer un <xref:System.Windows.Controls.Expander> contrôle qui contient un contenu complexe, comme une image et le texte.</span><span class="sxs-lookup"><span data-stu-id="cb740-103">This example shows how to create an <xref:System.Windows.Controls.Expander> control that contains complex content, such as an image and text.</span></span> <span data-ttu-id="cb740-104">L’exemple joint également le contenu de la <xref:System.Windows.Controls.Expander> dans un <xref:System.Windows.Controls.ScrollViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="cb740-104">The example also encloses the content of the <xref:System.Windows.Controls.Expander> in a <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cb740-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="cb740-105">Example</span></span>  
 <span data-ttu-id="cb740-106">L’exemple suivant montre comment créer un <xref:System.Windows.Controls.Expander>.</span><span class="sxs-lookup"><span data-stu-id="cb740-106">The following example shows how to create an <xref:System.Windows.Controls.Expander>.</span></span> <span data-ttu-id="cb740-107">L’exemple utilise un <xref:System.Windows.Controls.Primitives.BulletDecorator> contrôle, qui contient une image et du texte, afin de définir le <xref:System.Windows.Controls.HeaderedContentControl.Header%2A>.</span><span class="sxs-lookup"><span data-stu-id="cb740-107">The example uses a <xref:System.Windows.Controls.Primitives.BulletDecorator> control, which contains an image and text, in order to define the <xref:System.Windows.Controls.HeaderedContentControl.Header%2A>.</span></span> <span data-ttu-id="cb740-108">Un <xref:System.Windows.Controls.ScrollViewer> contrôle fournit une méthode pour faire défiler le contenu développé.</span><span class="sxs-lookup"><span data-stu-id="cb740-108">A <xref:System.Windows.Controls.ScrollViewer> control provides a method for scrolling the expanded content.</span></span>  
  
 <span data-ttu-id="cb740-109">Notez que l’exemple définit le <xref:System.Windows.FrameworkElement.Height%2A> propriété sur le <xref:System.Windows.Controls.ScrollViewer> au lieu de sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="cb740-109">Note that the example sets the <xref:System.Windows.FrameworkElement.Height%2A> property on the <xref:System.Windows.Controls.ScrollViewer> instead of on the content.</span></span> <span data-ttu-id="cb740-110">Si le <xref:System.Windows.FrameworkElement.Height%2A> est défini sur le contenu, le <xref:System.Windows.Controls.ScrollViewer> n’autorise pas l’utilisateur à faire défiler le contenu.</span><span class="sxs-lookup"><span data-stu-id="cb740-110">If the <xref:System.Windows.FrameworkElement.Height%2A> is set on the content, the <xref:System.Windows.Controls.ScrollViewer> does not allow the user to scroll the content.</span></span> <span data-ttu-id="cb740-111">Le <xref:System.Windows.FrameworkElement.Width%2A> propriété est définie sur le <xref:System.Windows.Controls.Expander> contrôle et si ce paramètre s’applique à la <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> et le contenu développé.</span><span class="sxs-lookup"><span data-stu-id="cb740-111">The <xref:System.Windows.FrameworkElement.Width%2A> property is set on the <xref:System.Windows.Controls.Expander> control and this setting applies to the <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> and the expanded content.</span></span>  
  
 [!code-xaml[ExpanderRichContent#CreateExpander](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml#createexpander)]  
  
 [!code-csharp[ExpanderRichContent#CreateExpanderCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml.cs#createexpandercode)]  
  
## <a name="see-also"></a><span data-ttu-id="cb740-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb740-112">See also</span></span>

- <xref:System.Windows.Controls.Expander>
- [<span data-ttu-id="cb740-113">Vue d'ensemble de l'expanseur</span><span class="sxs-lookup"><span data-stu-id="cb740-113">Expander Overview</span></span>](expander-overview.md)
- [<span data-ttu-id="cb740-114">Rubriques Comment</span><span class="sxs-lookup"><span data-stu-id="cb740-114">How-to Topics</span></span>](expander-how-to-topics.md)
