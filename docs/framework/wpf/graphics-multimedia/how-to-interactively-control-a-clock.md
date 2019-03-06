---
title: 'Procédure : Contrôler une horloge de façon interactive'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controlling clocks interactively [WPF]
- clocks [WPF], controlling interactively
ms.assetid: d0b520e0-2f18-4cef-977f-2909e709548a
ms.openlocfilehash: 6d3dbc8c39e63b46871b0cc88fbe8d5d51b63463
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57361653"
---
# <a name="how-to-interactively-control-a-clock"></a><span data-ttu-id="3ae7e-102">Procédure : Contrôler une horloge de façon interactive</span><span class="sxs-lookup"><span data-stu-id="3ae7e-102">How to: Interactively Control a Clock</span></span>
<span data-ttu-id="3ae7e-103">Un <xref:System.Windows.Media.Animation.Clock> l’objet <xref:System.Windows.Media.Animation.ClockController> propriété vous permet de manière interactive Démarrer, suspendre, reprendre, rechercher, avancer l’horloge à sa période de remplissage et arrêter l’horloge.</span><span class="sxs-lookup"><span data-stu-id="3ae7e-103">A <xref:System.Windows.Media.Animation.Clock> object's <xref:System.Windows.Media.Animation.ClockController> property enables you to interactively start, pause, resume, seek, advance the clock to its fill period, and stop the clock.</span></span> <span data-ttu-id="3ae7e-104">Que l’horloge racine d’arborescence de minutage peut être contrôlée de manière interactive.</span><span class="sxs-lookup"><span data-stu-id="3ae7e-104">Only the root clock of a timing tree can be interactively controlled.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3ae7e-105">Il existe d’autres façons de manière interactive des animations de contrôle qui ne nécessitent pas de travailler directement avec les horloges : vous pouvez également utiliser des tables de montage séquentiel.</span><span class="sxs-lookup"><span data-stu-id="3ae7e-105">There are other ways to interactively control animations that don't require you to work directly with clocks: you can also use Storyboards.</span></span> <span data-ttu-id="3ae7e-106">Les storyboards sont pris en charge dans le balisage et code.</span><span class="sxs-lookup"><span data-stu-id="3ae7e-106">Storyboards are supported in both markup and code.</span></span> <span data-ttu-id="3ae7e-107">Pour obtenir un exemple, consultez [animer une propriété à l’aide d’un Storyboard](how-to-animate-a-property-by-using-a-storyboard.md) ou [vue d’ensemble de l’Animation](animation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3ae7e-107">For an example, see [Animate a Property by Using a Storyboard](how-to-animate-a-property-by-using-a-storyboard.md) or the [Animation Overview](animation-overview.md).</span></span>  
  
 <span data-ttu-id="3ae7e-108">Dans l’exemple suivant, plusieurs boutons sont utilisés pour contrôler une horloge d’animation de manière interactive.</span><span class="sxs-lookup"><span data-stu-id="3ae7e-108">In the following example, several buttons are used to interactively control an animation clock.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3ae7e-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ae7e-109">Example</span></span>  
 [!code-csharp[timingbehaviors_procedural_snip#GraphicsMMClockControllerExample](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/ClockControllerExample.cs#graphicsmmclockcontrollerexample)]
 [!code-vb[timingbehaviors_procedural_snip#GraphicsMMClockControllerExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/clockcontrollerexample.vb#graphicsmmclockcontrollerexample)]  
  
## <a name="see-also"></a><span data-ttu-id="3ae7e-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ae7e-110">See also</span></span>
- [<span data-ttu-id="3ae7e-111">Animer une propriété à l’aide d’une table de montage séquentiel</span><span class="sxs-lookup"><span data-stu-id="3ae7e-111">Animate a Property by Using a Storyboard</span></span>](how-to-animate-a-property-by-using-a-storyboard.md)
- [<span data-ttu-id="3ae7e-112">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="3ae7e-112">Animation Overview</span></span>](animation-overview.md)
