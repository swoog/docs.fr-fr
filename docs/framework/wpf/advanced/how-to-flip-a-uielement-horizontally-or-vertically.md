---
title: 'Procédure : Retourner un UIElement horizontalement ou verticalement'
ms.date: 03/30/2017
helpviewer_keywords:
- flipping UIElements [WPF]
- UIElements [WPF], flipping
ms.assetid: 02c6730f-65c0-40d5-a553-4cb663721882
ms.openlocfilehash: 3dd9a8e2a94acf62973701094e8966c8ebff15c9
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57356349"
---
# <a name="how-to-flip-a-uielement-horizontally-or-vertically"></a><span data-ttu-id="c2605-102">Procédure : Retourner un UIElement horizontalement ou verticalement</span><span class="sxs-lookup"><span data-stu-id="c2605-102">How to: Flip a UIElement Horizontally or Vertically</span></span>
<span data-ttu-id="c2605-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.ScaleTransform> pour retourner un <xref:System.Windows.UIElement> horizontalement ou verticalement.</span><span class="sxs-lookup"><span data-stu-id="c2605-103">This example shows how to use a <xref:System.Windows.Media.ScaleTransform> to flip a <xref:System.Windows.UIElement> horizontally or vertically.</span></span> <span data-ttu-id="c2605-104">Dans cet exemple, un <xref:System.Windows.Controls.Button> contrôle (un type de <xref:System.Windows.UIElement>) est retourné en appliquant un <xref:System.Windows.Media.ScaleTransform> à son <xref:System.Windows.UIElement.RenderTransform%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c2605-104">In this example, a <xref:System.Windows.Controls.Button> control (a type of <xref:System.Windows.UIElement>) is flipped by applying a <xref:System.Windows.Media.ScaleTransform> to its <xref:System.Windows.UIElement.RenderTransform%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c2605-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2605-105">Example</span></span>  
 <span data-ttu-id="c2605-106">L’illustration suivante montre le bouton à retourner.</span><span class="sxs-lookup"><span data-stu-id="c2605-106">The following illustration shows the button to flip.</span></span>  
  
 <span data-ttu-id="c2605-107">![Un bouton sans transformation](./media/graphicsmm-buttonflipbeforeflip.gif "graphicsmm_buttonflipbeforeflip")</span><span class="sxs-lookup"><span data-stu-id="c2605-107">![A button with no transform](./media/graphicsmm-buttonflipbeforeflip.gif "graphicsmm_buttonflipbeforeflip")</span></span>  
<span data-ttu-id="c2605-108">UIElement à retourner</span><span class="sxs-lookup"><span data-stu-id="c2605-108">The UIElement to flip</span></span>  
  
 <span data-ttu-id="c2605-109">Voici le code qui crée le bouton.</span><span class="sxs-lookup"><span data-stu-id="c2605-109">The following shows the code that creates the button.</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMButtonWithoutFlip](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmbuttonwithoutflip)]  
  
## <a name="example"></a><span data-ttu-id="c2605-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2605-110">Example</span></span>  
 <span data-ttu-id="c2605-111">Pour retourner le bouton horizontalement, créez un <xref:System.Windows.Media.ScaleTransform> et définissez son <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> propriété sur -1.</span><span class="sxs-lookup"><span data-stu-id="c2605-111">To flip the button horizontally, create a <xref:System.Windows.Media.ScaleTransform> and set its <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> property to -1.</span></span> <span data-ttu-id="c2605-112">Appliquer le <xref:System.Windows.Media.ScaleTransform> sur le bouton <xref:System.Windows.UIElement.RenderTransform%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c2605-112">Apply the <xref:System.Windows.Media.ScaleTransform> to the button's <xref:System.Windows.UIElement.RenderTransform%2A> property.</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMFlipButtonExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmflipbuttonexample1)]  
  
 <span data-ttu-id="c2605-113">![Bouton renvoyé horizontalement autour de &#40;0,0&#41;](./media/graphicsmm-buttonfliphorizontalflip-displaced.gif "graphicsmm_buttonfliphorizontalflip_displaced")</span><span class="sxs-lookup"><span data-stu-id="c2605-113">![A button flipped horizontally about &#40;0,0&#41;](./media/graphicsmm-buttonfliphorizontalflip-displaced.gif "graphicsmm_buttonfliphorizontalflip_displaced")</span></span>  
<span data-ttu-id="c2605-114">Bouton après l’application de ScaleTransform</span><span class="sxs-lookup"><span data-stu-id="c2605-114">The button after applying the ScaleTransform</span></span>  
  
## <a name="example"></a><span data-ttu-id="c2605-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2605-115">Example</span></span>  
 <span data-ttu-id="c2605-116">Comme vous pouvez le voir à partir de l’illustration précédente, le bouton a été retourné, mais il a également été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c2605-116">As you can see from the previous illustration, the button was flipped, but it was also moved.</span></span> <span data-ttu-id="c2605-117">C’est parce que le bouton a été retourné à partir de son coin supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="c2605-117">That's because the button was flipped from its top left corner.</span></span> <span data-ttu-id="c2605-118">Pour retourner le bouton, vous souhaitez appliquer le <xref:System.Windows.Media.ScaleTransform> à son centre, pas son supérieur.</span><span class="sxs-lookup"><span data-stu-id="c2605-118">To flip the button in place, you want to apply the <xref:System.Windows.Media.ScaleTransform> to its center, not its corner.</span></span> <span data-ttu-id="c2605-119">Un moyen facile d’appliquer le <xref:System.Windows.Media.ScaleTransform> aux boutons center consiste à définir le bouton <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété 0.5, 0.5.</span><span class="sxs-lookup"><span data-stu-id="c2605-119">An easy way to apply the <xref:System.Windows.Media.ScaleTransform> to the buttons center is to set the button's <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property to 0.5, 0.5.</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMFlipButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmflipbuttonexample2)]  
  
 <span data-ttu-id="c2605-120">![Bouton renvoyé horizontalement autour de son centre](./media/graphicsmm-buttonfliphorizontalflip-inplace.gif "graphicsmm_buttonfliphorizontalflip_inplace")</span><span class="sxs-lookup"><span data-stu-id="c2605-120">![A button flipped horizontally about its center](./media/graphicsmm-buttonfliphorizontalflip-inplace.gif "graphicsmm_buttonfliphorizontalflip_inplace")</span></span>  
<span data-ttu-id="c2605-121">Le bouton avec un RenderTransformOrigin de 0.5, 0.5</span><span class="sxs-lookup"><span data-stu-id="c2605-121">The button with a RenderTransformOrigin of 0.5, 0.5</span></span>  
  
## <a name="example"></a><span data-ttu-id="c2605-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="c2605-122">Example</span></span>  
 <span data-ttu-id="c2605-123">Pour retourner le bouton verticalement, définissez la <xref:System.Windows.Media.ScaleTransform> l’objet <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> propriété au lieu de son <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c2605-123">To flip the button vertically, set the <xref:System.Windows.Media.ScaleTransform> object's <xref:System.Windows.Media.ScaleTransform.ScaleY%2A> property instead of its <xref:System.Windows.Media.ScaleTransform.ScaleX%2A> property.</span></span>  
  
 [!code-xaml[Transforms_snip#GraphicsMMVerticalFlipButtonExample2](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/FlipExample.xaml#graphicsmmverticalflipbuttonexample2)]  
  
 <span data-ttu-id="c2605-124">![Bouton renvoyé verticalement autour de son centre](./media/graphicsmm-buttonflipverticalflip-inplace.gif "graphicsmm_buttonflipverticalflip_inplace")</span><span class="sxs-lookup"><span data-stu-id="c2605-124">![A button flipped vertically about its center](./media/graphicsmm-buttonflipverticalflip-inplace.gif "graphicsmm_buttonflipverticalflip_inplace")</span></span>  
<span data-ttu-id="c2605-125">Bouton retourné verticalement</span><span class="sxs-lookup"><span data-stu-id="c2605-125">The vertically flipped button</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2605-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2605-126">See also</span></span>
- [<span data-ttu-id="c2605-127">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="c2605-127">Transforms Overview</span></span>](../graphics-multimedia/transforms-overview.md)
