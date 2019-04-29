---
title: 'Procédure : Animer une propriété à l’aide d’une table de montage séquentiel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], Storyboards
- Storyboards [WPF], animation
ms.assetid: f4a314e9-1da2-4367-85fc-1232487efa7a
ms.openlocfilehash: f6064368b4f5e4fa8324b4039d734d4430cd9174
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61761206"
---
# <a name="how-to-animate-a-property-by-using-a-storyboard"></a>Procédure : Animer une propriété à l’aide d’une table de montage séquentiel
Cet exemple montre comment utiliser un <xref:System.Windows.Media.Animation.Storyboard> pour animer des propriétés. Pour animer une propriété en utilisant un <xref:System.Windows.Media.Animation.Storyboard>, créer une animation pour chaque propriété que vous souhaitez animer et créez également un <xref:System.Windows.Media.Animation.Storyboard> pour contenir les animations.  
  
 Le type de propriété détermine le type d’animation à utiliser. Par exemple, pour animer une propriété qui accepte <xref:System.Double> valeurs, utilisez un <xref:System.Windows.Media.Animation.DoubleAnimation>. Le <xref:System.Windows.Media.Animation.Storyboard.TargetName%2A> et <xref:System.Windows.Media.Animation.Storyboard.TargetProperty> propriétés jointes spécifient l’objet et la propriété à laquelle l’animation est appliquée.  
  
 Pour démarrer un storyboard [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], utilisez un <xref:System.Windows.Media.Animation.BeginStoryboard> action et un <xref:System.Windows.EventTrigger>. Le <xref:System.Windows.EventTrigger> commence le <xref:System.Windows.Media.Animation.BeginStoryboard> action lorsque l’événement qui est spécifié par son <xref:System.Windows.EventTrigger.RoutedEvent%2A> propriété se produit. Le <xref:System.Windows.Media.Animation.BeginStoryboard> action démarre le <xref:System.Windows.Media.Animation.Storyboard>.  
  
 L’exemple suivant utilise <xref:System.Windows.Media.Animation.Storyboard> objets à animer deux <xref:System.Windows.Controls.Button> contrôles. Pour modifier le premier bouton taille, son <xref:System.Windows.FrameworkElement.Width%2A> est animée. Pour faire en sorte que le deuxième bouton change de couleur, la <xref:System.Windows.Media.SolidColorBrush.Color%2A> propriété de la <xref:System.Windows.Media.SolidColorBrush> est utilisé pour définir le <xref:System.Windows.Controls.Control.Background%2A> du bouton qui est animé.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[AnimatePropertyStoryboards#1](~/samples/snippets/xaml/VS_Snippets_Wpf/AnimatePropertyStoryboards/XAML/StoryboardExample.xaml#1)]  
  
> [!NOTE]
>  Bien que les animations puissent cibler à la fois un <xref:System.Windows.FrameworkElement> d’objet, comme un <xref:System.Windows.Controls.Control> ou <xref:System.Windows.Controls.Panel>et un <xref:System.Windows.Freezable> d’objet, comme un <xref:System.Windows.Media.Brush> ou <xref:System.Windows.Media.Transform>, uniquement les éléments d’infrastructure ont une <xref:System.Windows.FrameworkElement.Name%2A> propriété. Pour attribuer un nom à un objet Freezable afin qu’il puisse être ciblé par une animation, utilisez la [Directive x:Name](../../xaml-services/x-name-directive.md), comme illustré dans l’exemple précédent.  
  
 Si vous utilisez du code, vous devez créer un <xref:System.Windows.NameScope> pour un <xref:System.Windows.FrameworkElement> et enregistrer les noms des objets à animer avec <xref:System.Windows.FrameworkElement>. Pour démarrer les animations dans le code, utilisez un <xref:System.Windows.Media.Animation.BeginStoryboard> action avec un <xref:System.Windows.EventTrigger>. Si vous le souhaitez, vous pouvez utiliser un gestionnaire d’événements et le <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> méthode de <xref:System.Windows.Media.Animation.Storyboard>. L'exemple suivant illustre l'utilisation de la méthode <xref:System.Windows.Media.Animation.Storyboard.Begin%2A>.  
  
 [!code-csharp[AnimatePropertyStoryboards#11](~/samples/snippets/csharp/VS_Snippets_Wpf/AnimatePropertyStoryboards/CSharp/StoryboardExample.cs#11)]
 [!code-vb[AnimatePropertyStoryboards#11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AnimatePropertyStoryboards/VisualBasic/StoryboardExample.vb#11)]  
  
 Pour plus d’informations sur l’animation et les tables de montage séquentiel, consultez [Vue d’ensemble de l’animation](animation-overview.md).  
  
 Si vous utilisez du code, vous n’êtes pas limité à l’utilisation <xref:System.Windows.Media.Animation.Storyboard> objets pour animer des propriétés. Pour obtenir d’autres informations et exemples, consultez [Comment : animer une propriété sans utiliser de storyboard](how-to-animate-a-property-without-using-a-storyboard.md) et [Comment : animer une propriété à l’aide d’un AnimationClock](how-to-animate-a-property-by-using-an-animationclock.md).
