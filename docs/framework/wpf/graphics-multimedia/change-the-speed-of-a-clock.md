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
# <a name="how-to-change-the-speed-of-a-clock-without-changing-the-speed-of-its-timeline"></a>Procédure : Modifier la vitesse d'une horloge sans modifier la vitesse de sa chronologie
Un <xref:System.Windows.Media.Animation.ClockController> l’objet <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> propriété permet de modifier la vitesse d’un <xref:System.Windows.Media.Animation.Clock> sans en altérer le <xref:System.Windows.Media.Animation.Timeline.SpeedRatio%2A> de l’horloge <xref:System.Windows.Media.Animation.Timeline>. Dans l’exemple suivant, un <xref:System.Windows.Media.Animation.ClockController> est utilisé pour modifier de manière interactive la <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> d’une horloge. Le <xref:System.Windows.Media.Animation.Clock.CurrentGlobalSpeedInvalidated> événement et de l’horloge <xref:System.Windows.Media.Animation.Clock.CurrentGlobalSpeed%2A> propriété sont utilisées pour afficher la vitesse globale actuelle de l’horloge chaque fois que son interactive <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> est modifiée.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[timingbehaviors_procedural_snip#GraphicsMMClockControllerSpeedRatioExample](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/ClockControllerSpeedRatioExample.cs#graphicsmmclockcontrollerspeedratioexample)]
 [!code-vb[timingbehaviors_procedural_snip#GraphicsMMClockControllerSpeedRatioExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/clockcontrollerspeedratioexample.vb#graphicsmmclockcontrollerspeedratioexample)]
