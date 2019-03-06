---
title: 'Procédure : Animer un Popup'
ms.date: 03/30/2017
helpviewer_keywords:
- Popup control [WPF], animating
- animation [WPF], Popup controls
ms.assetid: acaa2a0a-6137-4efd-9cd1-75ece222e390
ms.openlocfilehash: ed5edf298e59d6a9adddc03fc21de1900c7ee8e9
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57372839"
---
# <a name="how-to-animate-a-popup"></a><span data-ttu-id="98b8a-102">Procédure : Animer un Popup</span><span class="sxs-lookup"><span data-stu-id="98b8a-102">How to: Animate a Popup</span></span>
<span data-ttu-id="98b8a-103">Cet exemple montre deux façons d’animer un <xref:System.Windows.Controls.Primitives.Popup> contrôle.</span><span class="sxs-lookup"><span data-stu-id="98b8a-103">This example shows two ways to animate a <xref:System.Windows.Controls.Primitives.Popup> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="98b8a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="98b8a-104">Example</span></span>  
 <span data-ttu-id="98b8a-105">L’exemple suivant définit la <xref:System.Windows.Controls.Primitives.PopupAnimation> à une valeur de propriété <xref:System.Windows.Controls.Primitives.PopupAnimation.Slide>, ce qui conduit le <xref:System.Windows.Controls.Primitives.Popup> sur « diapositive-in » lorsqu’il apparaît.</span><span class="sxs-lookup"><span data-stu-id="98b8a-105">The following example sets the <xref:System.Windows.Controls.Primitives.PopupAnimation> property to a value of <xref:System.Windows.Controls.Primitives.PopupAnimation.Slide>, which causes the <xref:System.Windows.Controls.Primitives.Popup> to "slide-in" when it appears.</span></span>  
  
 <span data-ttu-id="98b8a-106">Pour faire pivoter le <xref:System.Windows.Controls.Primitives.Popup>, cet exemple affecte un <xref:System.Windows.Media.RotateTransform> à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété sur le <xref:System.Windows.Controls.Canvas>, qui est l’élément enfant de la <xref:System.Windows.Controls.Primitives.Popup>.</span><span class="sxs-lookup"><span data-stu-id="98b8a-106">In order to rotate the <xref:System.Windows.Controls.Primitives.Popup>, this example assigns a <xref:System.Windows.Media.RotateTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property on the <xref:System.Windows.Controls.Canvas>, which is the child element of the <xref:System.Windows.Controls.Primitives.Popup>.</span></span>  
  
 <span data-ttu-id="98b8a-107">Pour la transformation fonctionne correctement, l’exemple doit définir le <xref:System.Windows.Controls.Primitives.Popup.AllowsTransparency%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="98b8a-107">For the transform to work correctly, the example must set the <xref:System.Windows.Controls.Primitives.Popup.AllowsTransparency%2A> property to `true`.</span></span> <span data-ttu-id="98b8a-108">En outre, le <xref:System.Windows.FrameworkElement.Margin%2A> sur le <xref:System.Windows.Controls.Canvas> contenu doit spécifier suffisamment d’espace pour le <xref:System.Windows.Controls.Primitives.Popup> pour faire pivoter.</span><span class="sxs-lookup"><span data-stu-id="98b8a-108">In addition, the <xref:System.Windows.FrameworkElement.Margin%2A> on the <xref:System.Windows.Controls.Canvas> content must specify enough space for the <xref:System.Windows.Controls.Primitives.Popup> to rotate.</span></span>  
  
 [!code-xaml[AnimatedPopup#RotateTransform2](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatedPopup/CS/Window1.xaml#rotatetransform2)]  
  
 <span data-ttu-id="98b8a-109">L’exemple suivant montre comment un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événement qui se produit lorsqu’un <xref:System.Windows.Controls.Button> est activé, les déclencheurs le <xref:System.Windows.Media.Animation.Storyboard> qui démarre l’animation.</span><span class="sxs-lookup"><span data-stu-id="98b8a-109">The following example shows how a <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event, which occurs when a <xref:System.Windows.Controls.Button> is clicked, triggers the <xref:System.Windows.Media.Animation.Storyboard> that starts the animation.</span></span>  
  
 [!code-xaml[AnimatedPopup#RotateTransform1](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatedPopup/CS/Window1.xaml#rotatetransform1)]  
  
## <a name="see-also"></a><span data-ttu-id="98b8a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98b8a-110">See also</span></span>
- <xref:System.Windows.UIElement.RenderTransform%2A>
- <xref:System.Windows.Controls.Primitives.BulletDecorator>
- <xref:System.Windows.Media.RotateTransform>
- <xref:System.Windows.Media.Animation.Storyboard>
- <xref:System.Windows.Controls.Primitives.Popup>
- [<span data-ttu-id="98b8a-111">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="98b8a-111">How-to Topics</span></span>](popup-how-to-topics.md)
- [<span data-ttu-id="98b8a-112">Vue d’ensemble de Popup</span><span class="sxs-lookup"><span data-stu-id="98b8a-112">Popup Overview</span></span>](popup-overview.md)
