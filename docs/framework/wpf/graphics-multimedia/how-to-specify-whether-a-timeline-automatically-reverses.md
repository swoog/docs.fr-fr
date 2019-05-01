---
title: 'Procédure : Spécifier l’inversion automatique d’une chronologie'
ms.date: 03/30/2017
helpviewer_keywords:
- AutoReverse property of timelines [WPF]
- Timelines [WPF], AutoReverse property
ms.assetid: 1648dd90-1bee-409a-ac69-ac729867f557
ms.openlocfilehash: 0fe2d337d8afa5197475e5b9ee40950226596e8b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62024662"
---
# <a name="how-to-specify-whether-a-timeline-automatically-reverses"></a>Procédure : Spécifier l’inversion automatique d’une chronologie
Une chronologie <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> propriété détermine si elle repart en arrière après avoir effectué une itération en avant. L’exemple suivant montre plusieurs animations avec durée identiques et des valeurs cibles, mais avec différents <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> paramètres. Pour illustrer comment le <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> propriété se comporte avec différentes <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> certaines animations, les paramètres sont configurés pour être répétés. La dernière animation indique comment la <xref:System.Windows.Media.Animation.Timeline.AutoReverse%2A> propriété fonctionne sur les chronologies imbriquées.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[timingbehaviors_snip#AutoReverseAndRepeatBehaviorExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AutoReverseExample.xaml#autoreverseandrepeatbehaviorexamplewholepage)]
