---
title: 'Procédure : Répéter une animation'
ms.date: 03/30/2017
helpviewer_keywords:
- RepeatBehavior property of timelines [WPF]
- repeating animating [WPF]
- Timelines RepeatBehavior property [WPF]
- animation [WPF], repeating
ms.assetid: e6f3b068-eeeb-47fd-8d40-8848c31f1e1e
ms.openlocfilehash: a80f72b0e67c13890d4befcbd5ab7c4a92a93fe7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61942088"
---
# <a name="how-to-repeat-an-animation"></a><span data-ttu-id="f58f8-102">Procédure : Répéter une animation</span><span class="sxs-lookup"><span data-stu-id="f58f8-102">How to: Repeat an Animation</span></span>
<span data-ttu-id="f58f8-103">Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> propriété d’un <xref:System.Windows.Media.Animation.Timeline> afin de contrôler le comportement de répétition d’une animation.</span><span class="sxs-lookup"><span data-stu-id="f58f8-103">This example shows how to use the <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> property of a <xref:System.Windows.Media.Animation.Timeline> in order to control the repeat behavior of an animation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f58f8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f58f8-104">Example</span></span>  
 <span data-ttu-id="f58f8-105">Le <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> propriété d’un <xref:System.Windows.Media.Animation.Timeline> contrôle le nombre de fois où une animation répète sa durée simple.</span><span class="sxs-lookup"><span data-stu-id="f58f8-105">The <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> property of a <xref:System.Windows.Media.Animation.Timeline> controls how many times an animation repeats its simple duration.</span></span> <span data-ttu-id="f58f8-106">À l’aide de <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>, vous pouvez spécifier qu’un <xref:System.Windows.Media.Animation.Timeline> se répète pour un certain nombre de fois (nombre d’itérations) ou pour une période de temps spécifié.</span><span class="sxs-lookup"><span data-stu-id="f58f8-106">By using <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>, you can specify that a <xref:System.Windows.Media.Animation.Timeline> repeats for a certain number of times (an iteration count) or for a specified time period.</span></span> <span data-ttu-id="f58f8-107">Dans les deux cas, l’animation passe par les exécutions de début-fin autant dont il a besoin pour remplir la durée ou au nombre demandé.</span><span class="sxs-lookup"><span data-stu-id="f58f8-107">In either case, the animation goes through as many beginning-to-end runs that it needs in order to fill the requested count or duration.</span></span>  
  
 <span data-ttu-id="f58f8-108">Par défaut, les chronologies ont un nombre de répétitions de 1.0, ce qui signifie qu’ils jouent une seule fois et ne se répètent pas.</span><span class="sxs-lookup"><span data-stu-id="f58f8-108">By default, timelines have a repeat count of 1.0, which means they play one time and do not repeat.</span></span> <span data-ttu-id="f58f8-109">Toutefois, si vous définissez la <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> propriété d’un <xref:System.Windows.Media.Animation.Timeline> à <xref:System.Windows.Media.Animation.RepeatBehavior.Forever%2A>, la chronologie se répète indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="f58f8-109">However, if you set the <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> property of a <xref:System.Windows.Media.Animation.Timeline> to <xref:System.Windows.Media.Animation.RepeatBehavior.Forever%2A>, the timeline repeats indefinitely.</span></span>  
  
 <span data-ttu-id="f58f8-110">L’exemple suivant montre comment utiliser le <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> propriété pour contrôler le comportement de répétition d’une animation.</span><span class="sxs-lookup"><span data-stu-id="f58f8-110">The following example shows how to use the <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> property to control the repeat behavior of an animation.</span></span> <span data-ttu-id="f58f8-111">L’exemple anime le <xref:System.Windows.FrameworkElement.Width%2A> propriété de cinq rectangles avec chaque rectangle à l’aide d’un autre type de comportement de répétition.</span><span class="sxs-lookup"><span data-stu-id="f58f8-111">The example animates the <xref:System.Windows.FrameworkElement.Width%2A> property of five rectangles with each rectangle using a different type of repeat behavior.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#RepeatBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/RepeatBehaviorExample.xaml#repeatbehaviorwholepage)]  
  
 <span data-ttu-id="f58f8-112">Pour obtenir un exemple complet, consultez [comportement de minutage d’Animation exemple](https://go.microsoft.com/fwlink/?LinkID=159970).</span><span class="sxs-lookup"><span data-stu-id="f58f8-112">For the complete sample, see [Animation Timing Behavior Sample](https://go.microsoft.com/fwlink/?LinkID=159970).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f58f8-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f58f8-113">See also</span></span>

- [<span data-ttu-id="f58f8-114">Accumuler des valeurs d'animation pendant des cycles de répétition</span><span class="sxs-lookup"><span data-stu-id="f58f8-114">Accumulate Animation Values During Repeat Cycles</span></span>](how-to-accumulate-animation-values-during-repeat-cycles.md)
- [<span data-ttu-id="f58f8-115">Spécifier l’inversion automatique d’une chronologie</span><span class="sxs-lookup"><span data-stu-id="f58f8-115">Specify Whether a Timeline Automatically Reverses</span></span>](how-to-specify-whether-a-timeline-automatically-reverses.md)
- [<span data-ttu-id="f58f8-116">L’animation et minutage des rubriques de procédures</span><span class="sxs-lookup"><span data-stu-id="f58f8-116">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
- [<span data-ttu-id="f58f8-117">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="f58f8-117">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="f58f8-118">Comportement de minuterie d’animation exemple</span><span class="sxs-lookup"><span data-stu-id="f58f8-118">Animation Timing Behavior Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159970)
