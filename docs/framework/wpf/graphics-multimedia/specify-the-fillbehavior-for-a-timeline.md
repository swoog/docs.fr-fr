---
title: 'Procédure : Spécifier le FillBehavior pour une chronologie ayant atteint la fin de sa période active'
ms.date: 03/30/2017
helpviewer_keywords:
- FillBehavior property for inactive timelines [WPF]
- Timelines [WPF], FillBehavior property
ms.assetid: db805f59-d513-4dac-af15-47005dae3199
ms.openlocfilehash: 9f03c5b8d4585c32e0a9f119649dd15a23523033
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59091114"
---
# <a name="how-to-specify-the-fillbehavior-for-a-timeline-that-has-reached-the-end-of-its-active-period"></a>Procédure : Spécifier le FillBehavior pour une chronologie ayant atteint la fin de sa période active
Cet exemple montre comment spécifier le <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> pour le texte inactif <xref:System.Windows.Media.Animation.Timeline> d’une propriété animée.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> propriété d’un <xref:System.Windows.Media.Animation.Timeline> détermine ce qui se passe à la valeur d’une propriété animée lorsqu’il n’est pas en cours d’animation, autrement dit, quand le <xref:System.Windows.Media.Animation.Timeline> est inactif, mais son parent <xref:System.Windows.Media.Animation.Timeline> est active ou d’une période d’attente. Par exemple, une propriété animée reste à sa fin valeur une fois que l’animation se termine ou qu’il fait revenir à la valeur qu’elle avait avant le démarrage de l’animation ?  
  
 L’exemple suivant utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer la <xref:System.Windows.FrameworkElement.Width%2A> de deux rectangles. Chaque rectangle utilise un autre <xref:System.Windows.Media.Animation.Timeline> objet.  
  
 Un <xref:System.Windows.Media.Animation.Timeline> a un <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> qui est défini sur <xref:System.Windows.Media.Animation.FillBehavior.Stop>, ce qui entraîne la largeur du rectangle à revenir à son non animées valeur lorsque le <xref:System.Windows.Media.Animation.Timeline> se termine. L’autre <xref:System.Windows.Media.Animation.Timeline> a un <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> de <xref:System.Windows.Media.Animation.FillBehavior.HoldEnd>, ce qui entraîne la largeur reste à sa fin valeur lorsque le <xref:System.Windows.Media.Animation.Timeline> se termine.  
  
 [!code-xaml[timingbehaviors_snip#FillBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/FillBehaviorExample.xaml#fillbehaviorwholepage)]  
  
 Pour obtenir un exemple complet, consultez [Galerie d’exemples d’Animation](https://go.microsoft.com/fwlink/?LinkID=159969).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.DoubleAnimation>
- <xref:System.Windows.FrameworkElement.Width%2A>
- <xref:System.Windows.Media.Animation.Timeline>
- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A>
- <xref:System.Windows.Media.Animation.FillBehavior.Stop>
- <xref:System.Windows.Media.Animation.FillBehavior.HoldEnd>
- [Vue d’ensemble de l’animation](animation-overview.md)
- [L’animation et minutage des rubriques de procédures](animation-and-timing-how-to-topics.md)
