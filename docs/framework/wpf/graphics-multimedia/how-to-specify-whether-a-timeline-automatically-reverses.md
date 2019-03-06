---
title: "Procédure : Spécifier l'inversion automatique ou non d'une chronologie"
ms.date: 03/30/2017
helpviewer_keywords:
- AutoReverse property of timelines [WPF]
- Timelines [WPF], AutoReverse property
ms.assetid: 1648dd90-1bee-409a-ac69-ac729867f557
ms.openlocfilehash: 0fe2d337d8afa5197475e5b9ee40950226596e8b
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57354204"
---
# <a name="how-to-specify-whether-a-timeline-automatically-reverses"></a><span data-ttu-id="90dd2-102">Procédure : Spécifier l'inversion automatique ou non d'une chronologie</span><span class="sxs-lookup"><span data-stu-id="90dd2-102">How to: Specify Whether a Timeline Automatically Reverses</span></span>
<span data-ttu-id="90dd2-103">Une chronologie <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> propriété détermine si elle repart en arrière après avoir effectué une itération en avant.</span><span class="sxs-lookup"><span data-stu-id="90dd2-103">A timeline's <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> property determines whether it plays in reverse after it completes a forward iteration.</span></span> <span data-ttu-id="90dd2-104">L’exemple suivant montre plusieurs animations avec durée identiques et des valeurs cibles, mais avec différents <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> paramètres.</span><span class="sxs-lookup"><span data-stu-id="90dd2-104">The following example shows several animations with identical duration and target values, but with different <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> settings.</span></span> <span data-ttu-id="90dd2-105">Pour illustrer comment le <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> propriété se comporte avec différentes <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> certaines animations, les paramètres sont configurés pour être répétés.</span><span class="sxs-lookup"><span data-stu-id="90dd2-105">To demonstrate how the <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> property behaves with different <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> settings, some animations are set to repeat.</span></span> <span data-ttu-id="90dd2-106">La dernière animation indique comment la <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> propriété fonctionne sur les chronologies imbriquées.</span><span class="sxs-lookup"><span data-stu-id="90dd2-106">The last animation shows how the <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> property works on nested timelines.</span></span>  
  
## <a name="example"></a><span data-ttu-id="90dd2-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="90dd2-107">Example</span></span>  
 [!code-xaml[timingbehaviors_snip#AutoReverseAndRepeatBehaviorExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AutoReverseExample.xaml#autoreverseandrepeatbehaviorexamplewholepage)]
