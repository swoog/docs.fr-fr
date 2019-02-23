---
title: 'Procédure : Spécifier HandoffBehavior entre des animations de storyboard'
ms.date: 03/30/2017
helpviewer_keywords:
- Storyboards [WPF], handoff behavior between animations
- animation [WPF], handoff behavior between
ms.assetid: 97bd6842-929b-49d9-813e-46553ae46472
ms.openlocfilehash: a6da3f58fc6e999f5196cf5d8d3fd00f1098fc50
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "56745851"
---
# <a name="how-to-specify-handoffbehavior-between-storyboard-animations"></a><span data-ttu-id="bfbd7-102">Procédure : Spécifier HandoffBehavior entre des animations de storyboard</span><span class="sxs-lookup"><span data-stu-id="bfbd7-102">How to: Specify HandoffBehavior Between Storyboard Animations</span></span>
<span data-ttu-id="bfbd7-103">Cet exemple montre comment spécifier le comportement de transfert entre des animations de storyboard.</span><span class="sxs-lookup"><span data-stu-id="bfbd7-103">This example shows how to specify handoff behavior between storyboard animations.</span></span> <span data-ttu-id="bfbd7-104">Le <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> propriété du <xref:System.Windows.Media.Animation.BeginStoryboard> spécifie comment les nouvelles animations interagissent avec les animations existantes qui sont déjà appliquées à une propriété.</span><span class="sxs-lookup"><span data-stu-id="bfbd7-104">The <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> property of <xref:System.Windows.Media.Animation.BeginStoryboard> specifies how new animations interact with any existing ones that are already applied to a property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bfbd7-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="bfbd7-105">Example</span></span>  
 <span data-ttu-id="bfbd7-106">L’exemple suivant crée deux boutons s’agrandissent lorsque le curseur de souris se déplace au-dessus d’eux et diminuent lorsque le curseur se déplace.</span><span class="sxs-lookup"><span data-stu-id="bfbd7-106">The following example creates two buttons that enlarge when the mouse cursor moves over them and become smaller when the cursor moves away.</span></span> <span data-ttu-id="bfbd7-107">Si vous placez la souris sur un bouton et ensuite supprimez rapidement le curseur, la deuxième animation sera appliquée avant que la première est terminée.</span><span class="sxs-lookup"><span data-stu-id="bfbd7-107">If you mouse over a button and then quickly remove the cursor, the second animation will be applied before the first one is finished.</span></span> <span data-ttu-id="bfbd7-108">C’est lorsque deux animations se chevauchent ainsi que vous pouvez voir la différence entre la <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> les valeurs de <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> et <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace>.</span><span class="sxs-lookup"><span data-stu-id="bfbd7-108">It is when two animations overlap like this that you can see the difference between the <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A> values of <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> and <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace>.</span></span> <span data-ttu-id="bfbd7-109">La valeur <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> combine les animations qui se chevauche à l’origine d’une transition plus fluide entre les animations alors que la valeur <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace> provoque la nouvelle animation remplacement immédiat de l’animation précédemment qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="bfbd7-109">A value of <xref:System.Windows.Media.Animation.HandoffBehavior.Compose> combines the overlapping animations causing a smoother transition between animations while a value of <xref:System.Windows.Media.Animation.HandoffBehavior.SnapshotAndReplace> causes the new animation to immediately replace the earlier overlapping animation.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#HandoffBehaviorWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/HandoffBehaviorExample.xaml#handoffbehaviorwholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="bfbd7-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfbd7-110">See also</span></span>
- <xref:System.Windows.Media.Animation.BeginStoryboard>
- <xref:System.Windows.Media.Animation.BeginStoryboard.HandoffBehavior%2A>
- [<span data-ttu-id="bfbd7-111">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="bfbd7-111">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [<span data-ttu-id="bfbd7-112">L’animation et minutage des rubriques de procédures</span><span class="sxs-lookup"><span data-stu-id="bfbd7-112">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
