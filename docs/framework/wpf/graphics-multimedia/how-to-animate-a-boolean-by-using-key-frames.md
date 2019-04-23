---
title: 'Procédure : Animer une valeur booléenne à l’aide d’images clés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Booleans [WPF], animating with key frames
- animation [WPF], Booleans with key frames
- key frames [WPF], animating Booleans with
ms.assetid: 4b0fac96-6231-4fcf-9775-4dd673ddc785
ms.openlocfilehash: 59a72916721cccbe66f704253f148828fa8cd418
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59175030"
---
# <a name="how-to-animate-a-boolean-by-using-key-frames"></a>Procédure : Animer une valeur booléenne à l’aide d’images clés
Cet exemple montre comment animer la valeur de propriété booléenne d’un <xref:System.Windows.Controls.Button> contrôle à l’aide d’images clés.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.BooleanAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.UIElement.IsEnabled%2A> propriété d’un <xref:System.Windows.Controls.Button> contrôle. Toutes les images clés dans cet exemple montre comment utilisent une instance de la <xref:System.Windows.Media.Animation.DiscreteBooleanKeyFrame> classe. Images clés discrètes comme <xref:System.Windows.Media.Animation.DiscreteBooleanKeyFrame> créent des changements soudains entre les valeurs, autrement dit, le déplacement de l’animation est saccadé.  
  
 [!code-csharp[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/BooleanAnimationUsingKeyFramesExample.cs#booleananimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/booleananimationusingkeyframesexample.vb#booleananimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/BooleanAnimationUsingKeyFramesExample.xaml#booleananimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.Animation.BooleanAnimationUsingKeyFrames>
- <xref:System.Windows.UIElement.IsEnabled%2A>
- <xref:System.Windows.Controls.Button>
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Guides pratiques relatifs aux images clés](key-frame-animation-how-to-topics.md)
