---
title: 'Procédure : Animer une propriété à l’aide d’un objet AnimationClock'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], properties [WPF], with AnimationClocks
- AnimationClocks [WPF]
ms.assetid: e6542021-714c-4675-9567-04f1c7380834
ms.openlocfilehash: 4fa9efc593461d26eabaee5e2f62c1a17da1b543
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59201362"
---
# <a name="how-to-animate-a-property-by-using-an-animationclock"></a>Procédure : Animer une propriété à l’aide d’un objet AnimationClock
Cet exemple montre comment utiliser <xref:System.Windows.Media.Animation.Clock> objets à animer une propriété.  
  
 Il existe trois façons d’animer une propriété de dépendance :  
  
-   Créer un <xref:System.Windows.Media.Animation.AnimationTimeline> et l’associer à cette propriété à l’aide un <xref:System.Windows.Media.Animation.Storyboard>.  
  
-   Utilisez l’objet <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> méthode pour appliquer un seul <xref:System.Windows.Media.Animation.AnimationTimeline> à une propriété cible.  
  
-   Créer un <xref:System.Windows.Media.Animation.AnimationClock> à partir d’un <xref:System.Windows.Media.Animation.AnimationTimeline> et appliquez-le à une propriété.  
  
 <xref:System.Windows.Media.Animation.Storyboard> objets et le <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> activer la méthode vous permet d’animer des propriétés sans créer et distribuer des horloges directement (pour obtenir des exemples, consultez [animer une propriété à l’aide d’un Storyboard](how-to-animate-a-property-by-using-a-storyboard.md) et [animer une propriété sans À l’aide d’un Storyboard](how-to-animate-a-property-without-using-a-storyboard.md)) ; horloges sont créées et distribuées automatiquement pour vous.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment créer un <xref:System.Windows.Media.Animation.AnimationClock> et l’appliquer à deux propriétés similaires.  
  
 [!code-csharp[timingbehaviors_procedural_snip#GraphicsMMCreateAnimationClockWholeClass](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/AnimationClockExample.cs#graphicsmmcreateanimationclockwholeclass)]
 [!code-vb[timingbehaviors_procedural_snip#GraphicsMMCreateAnimationClockWholeClass](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/animationclockexample.vb#graphicsmmcreateanimationclockwholeclass)]  
  
 Pour obtenir un exemple montrant comment contrôler de manière interactive un <xref:System.Windows.Media.Animation.Clock> après son démarrage, consultez [contrôler une horloge de façon interactive](how-to-interactively-control-a-clock.md).  
  
## <a name="see-also"></a>Voir aussi

- [Animer une propriété à l’aide d’une table de montage séquentiel](how-to-animate-a-property-by-using-a-storyboard.md)
- [Animer une propriété sans utiliser de table de montage séquentiel](how-to-animate-a-property-without-using-a-storyboard.md)
- [Vue d'ensemble des techniques d'animation de propriétés](property-animation-techniques-overview.md)
