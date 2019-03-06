---
title: 'Procédure : Accélérer ou décélérer une animation'
ms.date: 03/30/2017
helpviewer_keywords:
- decelerating animation [WPF]
- accelerating animation [WPF]
- animation [WPF], accelerating
- animation [WPF], decelerating
ms.assetid: 4f383b2c-f94d-4a4e-9a06-f56f5dae95f9
ms.openlocfilehash: d4fcaf4a684c37590f27d603ef5cb2c86a6fb854
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57376245"
---
# <a name="how-to-accelerate-or-decelerate-an-animation"></a><span data-ttu-id="8bf49-102">Procédure : Accélérer ou décélérer une animation</span><span class="sxs-lookup"><span data-stu-id="8bf49-102">How to: Accelerate or Decelerate an Animation</span></span>
<span data-ttu-id="8bf49-103">Cet exemple montre comment réaliser une animation d’accélération et une décélération au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="8bf49-103">This example demonstrates how to make an animation accelerate and decelerate over time.</span></span> <span data-ttu-id="8bf49-104">Dans l’exemple suivant, plusieurs rectangles sont animés par des animations avec différents <xref:System.Windows.Media.Animation.Timeline.AccelerationRatio%2A> et <xref:System.Windows.Media.Animation.Timeline.DecelerationRatio%2A> paramètres.</span><span class="sxs-lookup"><span data-stu-id="8bf49-104">In the following example, several rectangles are animated by animations with different <xref:System.Windows.Media.Animation.Timeline.AccelerationRatio%2A> and <xref:System.Windows.Media.Animation.Timeline.DecelerationRatio%2A> settings.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8bf49-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="8bf49-105">Example</span></span>  
 [!code-xaml[timingbehaviors_snip#1](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AccelDecelExample.xaml#1)]  
  
 <span data-ttu-id="8bf49-106">Code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="8bf49-106">Code has been omitted from this example.</span></span> <span data-ttu-id="8bf49-107">Pour le code complet, consultez la [comportement de minuterie d’Animation (C#)](https://github.com/dotnet/samples/tree/master/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp) ou [comportement de minuterie d’Animation (Visual Basic)](https://github.com/dotnet/samples/tree/master/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic).</span><span class="sxs-lookup"><span data-stu-id="8bf49-107">For the complete code, see the [Animation Timing Behavior (C#)](https://github.com/dotnet/samples/tree/master/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp) or [Animation Timing Behavior (Visual Basic)](https://github.com/dotnet/samples/tree/master/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic).</span></span>
