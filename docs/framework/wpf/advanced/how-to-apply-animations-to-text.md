---
title: 'Procédure : Appliquer des animations à du texte'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], animations
- animation [WPF], text
ms.assetid: eec3d26c-0a21-420f-8012-671621c47089
ms.openlocfilehash: 4cc7932b43f8a3c35d750f9a9020e16257867f76
ms.sourcegitcommit: 7156c0b9e4ce4ce5ecf48ce3d925403b638b680c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2019
ms.locfileid: "58463122"
---
# <a name="how-to-apply-animations-to-text"></a>Procédure : Appliquer des animations à du texte
Les animations peuvent modifier l’affichage et l’apparence du texte dans votre application. Les exemples suivants utilisent différents types d’animations pour changer l’affichage du texte dans un <xref:System.Windows.Controls.TextBlock> contrôle.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer la largeur du bloc de texte. La valeur de largeur change pour passer de la largeur du bloc de texte à 0 sur une durée de 10 secondes, puis les valeurs de largeur sont inversées et la procédure continue. Ce type d’animation crée un effet de balayage.  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample1)]  
  
 L’exemple suivant utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer l’opacité du bloc de texte. La valeur d’opacité passe de 1.0 à 0 sur une durée de 5 secondes, puis les valeurs d’opacité sont inversées et la procédure continue.  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample2)]  
  
 Le diagramme suivant montre l’effet de la <xref:System.Windows.Controls.TextBlock> contrôle quand son opacité passe de `1.00` à `0.00` pendant l’intervalle de 5 secondes défini par le <xref:System.Windows.Media.Animation.Timeline.Duration%2A>.  
  
 ![Opacité de 1.00 à 0.00 du texte.](./media/how-to-apply-animations-to-text/faded-text-opacity-change.png)  
   
 L’exemple suivant utilise un <xref:System.Windows.Media.Animation.ColorAnimation> pour animer la couleur de premier plan du bloc de texte. La valeur de la couleur de premier plan passe d’une couleur à une autre sur une durée de 5 secondes, puis les valeurs de couleur sont inversées et la procédure continue.  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample3)]  
  
 L’exemple suivant utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour faire pivoter le bloc de texte. Le bloc de texte effectue une rotation complète sur une durée de 20 secondes, puis la procédure de rotation se répète.  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample4](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample4)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de l’animation](../graphics-multimedia/animation-overview.md)
