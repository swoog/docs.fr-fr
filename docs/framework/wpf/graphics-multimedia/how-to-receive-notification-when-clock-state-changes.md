---
title: 'Procédure : Recevoir une notification en cas de changement d’état de l’horloge'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- clocks [WPF], notification of state changes
- notifications [WPF], clocks' state changes
ms.assetid: ecb10fc9-d0c2-45c3-b0a1-7b11baa733da
ms.openlocfilehash: dc3fffb88ce59ceb908d6febd2f078820513b641
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61942132"
---
# <a name="how-to-receive-notification-when-a-clocks-state-changes"></a>Procédure : Recevoir une notification en cas de changement d’état de l’horloge
D’une horloge <xref:System.Windows.Media.Animation.Clock.CurrentStateInvalidated> événement se produit lors de son <xref:System.Windows.Media.Animation.Clock.CurrentState%2A> devient non valide, par exemple lorsque l’horloge démarre ou s’arrête. Vous pouvez vous inscrire à cet événement directement en utilisant un <xref:System.Windows.Media.Animation.Clock>, ou vous pouvez vous inscrire à l’aide un <xref:System.Windows.Media.Animation.Timeline>.  
  
 Dans l’exemple suivant, un <xref:System.Windows.Media.Animation.Storyboard> et deux <xref:System.Windows.Media.Animation.DoubleAnimation> objets sont utilisés pour animer la largeur de deux rectangles. Le <xref:System.Windows.Media.Animation.Timeline.CurrentStateInvalidated> événement est utilisé pour écouter les changements d’état de l’horloge.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[timingbehaviors_snip#_graphicsmm_StateExampleMarkupWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/StateExample.xaml#_graphicsmm_stateexamplemarkupwholepage)]  
  
 [!code-csharp[timingbehaviors_snip#_graphicsmm_StateEventHandlers](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/StateExample.xaml.cs#_graphicsmm_stateeventhandlers)]
 [!code-vb[timingbehaviors_snip#_graphicsmm_StateEventHandlers](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/stateexample.xaml.vb#_graphicsmm_stateeventhandlers)]  
  
 L’illustration suivante montre les différents États les animations en tant que la chronologie parent (*Storyboard*) progresse.  
  
 ![États d’horloge pour une table de montage séquentiel avec deux animations](./media/graphicsmm-3timelines.png "graphicsmm_3timelines")  
  
 Le tableau suivant répertorie les moments qui *Animation1*de <xref:System.Windows.Media.Animation.Timeline.CurrentStateInvalidated> se déclenche des événements :  
  
||||||||  
|-|-|-|-|-|-|-|  
|Durée (en secondes)|1|10|19|21|30|39|  
|État|Actif|Actif|Arrêté|Actif|Actif|Arrêté|  
  
 Le tableau suivant répertorie les moments qui *Animation2*de <xref:System.Windows.Media.Animation.Timeline.CurrentStateInvalidated> se déclenche des événements :  
  
||||||||||  
|-|-|-|-|-|-|-|-|-|  
|Durée (en secondes)|1|9|11|19|21|29|31|39|  
|État|Actif|Remplissage|Actif|Arrêté|Actif|Remplissage|Actif|Arrêté|  
  
 Notez que *Animation1*de <xref:System.Windows.Media.Animation.Timeline.CurrentStateInvalidated> événement se déclenche à 10 secondes, même si son état reste <xref:System.Windows.Media.Animation.ClockState.Active>. C’est parce que son état a changé dans 10 secondes, mais il a été remplacée par <xref:System.Windows.Media.Animation.ClockState.Active> à <xref:System.Windows.Media.Animation.ClockState.Filling> , puis revient à <xref:System.Windows.Media.Animation.ClockState.Active> dans le même battement.
