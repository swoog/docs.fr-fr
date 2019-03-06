---
title: "Procédure : Modifier la vitesse d'une horloge sans modifier la vitesse de sa chronologie"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- speed of Clock [WPF], changing
- clocks [WPF], changing speed of
ms.assetid: 72f36dd0-f085-445d-8589-19a83fe74f5e
ms.openlocfilehash: 19e6874b9b472cb4a5f716677f99af03f2b73b10
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57358273"
---
# <a name="how-to-change-the-speed-of-a-clock-without-changing-the-speed-of-its-timeline"></a><span data-ttu-id="bb471-102">Procédure : Modifier la vitesse d'une horloge sans modifier la vitesse de sa chronologie</span><span class="sxs-lookup"><span data-stu-id="bb471-102">How to: Change the Speed of a Clock Without Changing the Speed of Its Timeline</span></span>
<span data-ttu-id="bb471-103">Un <xref:System.Windows.Media.Animation.ClockController> l’objet <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> propriété permet de modifier la vitesse d’un <xref:System.Windows.Media.Animation.Clock> sans en altérer le <xref:System.Windows.Media.Animation.Timeline.SpeedRatio%2A> de l’horloge <xref:System.Windows.Media.Animation.Timeline>.</span><span class="sxs-lookup"><span data-stu-id="bb471-103">A <xref:System.Windows.Media.Animation.ClockController> object's <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> property enables you to change the speed of a <xref:System.Windows.Media.Animation.Clock> without altering the <xref:System.Windows.Media.Animation.Timeline.SpeedRatio%2A> of the clock's <xref:System.Windows.Media.Animation.Timeline>.</span></span> <span data-ttu-id="bb471-104">Dans l’exemple suivant, un <xref:System.Windows.Media.Animation.ClockController> est utilisé pour modifier de manière interactive la <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> d’une horloge.</span><span class="sxs-lookup"><span data-stu-id="bb471-104">In the following example, a <xref:System.Windows.Media.Animation.ClockController> is used to interactively modify the <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> of a clock.</span></span> <span data-ttu-id="bb471-105">Le <xref:System.Windows.Media.Animation.Clock.CurrentGlobalSpeedInvalidated> événement et de l’horloge <xref:System.Windows.Media.Animation.Clock.CurrentGlobalSpeed%2A> propriété sont utilisées pour afficher la vitesse globale actuelle de l’horloge chaque fois que son interactive <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> est modifiée.</span><span class="sxs-lookup"><span data-stu-id="bb471-105">The <xref:System.Windows.Media.Animation.Clock.CurrentGlobalSpeedInvalidated> event and the clock's <xref:System.Windows.Media.Animation.Clock.CurrentGlobalSpeed%2A> property are used to display the clock's current global speed each time its interactive <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> is changed.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bb471-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="bb471-106">Example</span></span>  
 [!code-csharp[timingbehaviors_procedural_snip#GraphicsMMClockControllerSpeedRatioExample](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/ClockControllerSpeedRatioExample.cs#graphicsmmclockcontrollerspeedratioexample)]
 [!code-vb[timingbehaviors_procedural_snip#GraphicsMMClockControllerSpeedRatioExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/clockcontrollerspeedratioexample.vb#graphicsmmclockcontrollerspeedratioexample)]
