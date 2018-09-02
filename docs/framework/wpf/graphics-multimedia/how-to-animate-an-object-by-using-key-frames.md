---
title: "Comment : animer un objet à l'aide d'images clés"
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], objects with key frames
- key frames [WPF], animating objects with
ms.assetid: b1f15ba9-cac7-4cea-8699-5c6b55c05c5e
ms.openlocfilehash: 5e948b574e1b4a1c431b9495583e9579502576a8
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43416332"
---
# <a name="how-to-animate-an-object-by-using-key-frames"></a>Comment : animer un objet à l'aide d'images clés
Cet exemple montre comment animer un objet qui, dans cet exemple est la <xref:System.Windows.Controls.Page.Background%2A> propriété d’un <xref:System.Windows.Controls.Page> contrôle, à l’aide d’images clés.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> change de classe pour animer une couleur pour le <xref:System.Windows.Controls.Page.Background%2A> propriété d’un <xref:System.Windows.Controls.Page> contrôle. L’exemple d’animation passe à un pinceau d’arrière-plan différente à intervalles réguliers. Cette animation utilise la <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> classe pour créer trois images clés différentes. L’animation utilise des images clés de la manière suivante :  
  
1.  À la fin de la première seconde, anime une instance de la <xref:System.Windows.Media.LinearGradientBrush> classe. Cette section de l’exemple s’applique à un dégradé linéaire à la couleur d’arrière-plan afin que la couleur passe du jaune au rouge orange.  
  
2.  À la fin de la prochaine seconde, anime une instance de la <xref:System.Windows.Media.RadialGradientBrush> classe. Cette section de l’exemple s’applique à un dégradé radial à la couleur d’arrière-plan afin que la couleur passe du blanc au bleu en noir.  
  
3.  À la fin de la troisième seconde, anime une instance de la <xref:System.Windows.Media.DrawingBrush> classe. Cette section de l’exemple applique un modèle de damier à l’arrière-plan.  
  
4.  L’animation recommence et se répète indéfiniment.  
  
> [!NOTE]
>  <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> est le seul type d’image clé que vous pouvez utiliser avec la <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> classe. Images clés comme <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> créent des changements soudains dans les valeurs, autrement dit, les modifications de couleur dans cet exemple se produisent soudainement.  
  
 [!code-xaml[keyframes_snip#ObjectAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ObjectAnimationUsingKeyFramesExample.xaml#objectanimationusingkeyframeswholepage)]  
  
 Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames>  
 <xref:System.Windows.Controls.Page.Background%2A>  
 <xref:System.Windows.Controls.Page>  
 <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame>  
 <xref:System.Windows.Media.LinearGradientBrush>  
 <xref:System.Windows.Media.RadialGradientBrush>  
 <xref:System.Windows.Media.DrawingBrush>  
 [Vue d'ensemble des animations d'image clé](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [Guides pratiques relatifs aux images clés](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
