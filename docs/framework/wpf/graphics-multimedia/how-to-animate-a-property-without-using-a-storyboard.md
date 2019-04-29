---
title: 'Procédure : Animer une propriété sans utiliser de table de montage séquentiel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- non-Storyboard animation
- local animation [WPF]
- animation [WPF], non-Storyboard (local)
ms.assetid: d411db70-4df7-487d-82bc-95a7c1b2e7f8
ms.openlocfilehash: 93609cdeb4d879cbec0f90096e4fa2c131a2ec5e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61761284"
---
# <a name="how-to-animate-a-property-without-using-a-storyboard"></a><span data-ttu-id="88501-102">Procédure : Animer une propriété sans utiliser de table de montage séquentiel</span><span class="sxs-lookup"><span data-stu-id="88501-102">How to: Animate a Property Without Using a Storyboard</span></span>
<span data-ttu-id="88501-103">Cet exemple montre comment appliquer une animation à une propriété sans utiliser un <xref:System.Windows.Media.Animation.Storyboard>.</span><span class="sxs-lookup"><span data-stu-id="88501-103">This example shows one way to apply an animation to a property without using a <xref:System.Windows.Media.Animation.Storyboard>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="88501-104">La fonctionnalité n’est pas disponible en langage [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="88501-104">This functionality is not available in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span></span> <span data-ttu-id="88501-105">Pour plus d’informations sur l’animation d’une propriété en [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], consultez [Animer une propriété à l’aide d’un storyboard](how-to-animate-a-property-by-using-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="88501-105">For information about animating a property in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], see [Animate a Property by Using a Storyboard](how-to-animate-a-property-by-using-a-storyboard.md).</span></span>  
  
 <span data-ttu-id="88501-106">Pour appliquer une animation locale à une propriété, utilisez le <xref:System.Windows.UIElement.BeginAnimation%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="88501-106">To apply a local animation to a property, use the <xref:System.Windows.UIElement.BeginAnimation%2A> method.</span></span> <span data-ttu-id="88501-107">Cette méthode accepte deux paramètres : un <xref:System.Windows.DependencyProperty> qui spécifie la propriété à animer et l’animation à appliquer à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88501-107">This method takes two parameters: a <xref:System.Windows.DependencyProperty> that specifies the property to animate, and the animation to apply to that property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="88501-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="88501-108">Example</span></span>  
 <span data-ttu-id="88501-109">L’exemple suivant montre comment animer la couleur d’arrière-plan et de la largeur d’un <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="88501-109">The following example shows how to animate the width and background color of a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-cpp[animateproperty#11](~/samples/snippets/cpp/VS_Snippets_Wpf/animateproperty/CPP/LocalAnimationExample.cpp#11)]
 [!code-csharp[animateproperty#11](~/samples/snippets/csharp/VS_Snippets_Wpf/animateproperty/CSharp/LocalAnimationExample.cs#11)]
 [!code-vb[animateproperty#11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/animateproperty/VisualBasic/LocalAnimationExample.vb#11)]  
  
 <span data-ttu-id="88501-110">Une variété de classes d’animation dans le <xref:System.Windows.Media.Animation> espace de noms existe pour animer différents types de propriétés.</span><span class="sxs-lookup"><span data-stu-id="88501-110">A variety of animation classes in the <xref:System.Windows.Media.Animation> namespace exist for animating different types of properties.</span></span> <span data-ttu-id="88501-111">Pour plus d’informations sur l’animation de propriétés, consultez [Vue d’ensemble de l’animation](animation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="88501-111">For more information about animating properties, see [Animation Overview](animation-overview.md).</span></span> <span data-ttu-id="88501-112">Pour plus d’informations sur les propriétés de dépendance (le type de propriétés présentées dans ces exemples) et leurs fonctionnalités, consultez [Vue d’ensemble des propriétés de dépendance](../advanced/dependency-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="88501-112">For more information about dependency properties (the type of properties that are shown in these examples) and their features, see [Dependency Properties Overview](../advanced/dependency-properties-overview.md).</span></span>  
  
 <span data-ttu-id="88501-113">Il existe d’autres façons d’animer sans utiliser <xref:System.Windows.Media.Animation.Storyboard> objets ; pour plus d’informations, consultez [vue d’ensemble des Techniques d’Animation propriété](property-animation-techniques-overview.md).</span><span class="sxs-lookup"><span data-stu-id="88501-113">There are other ways to animate without using <xref:System.Windows.Media.Animation.Storyboard> objects; for more information, see [Property Animation Techniques Overview](property-animation-techniques-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88501-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88501-114">See also</span></span>

- <xref:System.Windows.Media.Animation.AnimationTimeline>
- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A>
- <xref:System.Windows.Media.Animation>
- <xref:System.Windows.Media.Animation.Storyboard>
- [<span data-ttu-id="88501-115">Vue d’ensemble des techniques d’animation de propriétés</span><span class="sxs-lookup"><span data-stu-id="88501-115">Property Animation Techniques Overview</span></span>](property-animation-techniques-overview.md)
- [<span data-ttu-id="88501-116">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="88501-116">Animation Overview</span></span>](animation-overview.md)
