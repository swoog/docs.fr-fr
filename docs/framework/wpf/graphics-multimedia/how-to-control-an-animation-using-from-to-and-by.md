---
title: 'Procédure : Contrôler une animation avec From, To et By'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], From/to/by
- basic animation [WPF]
- animation [WPF], basic animation
- From/to/by animation
ms.assetid: 59afba57-6fc1-44c8-987e-8a5f4142adad
ms.openlocfilehash: 56522ee5bd4391e43c261558b2fa622234c9ea3b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008783"
---
# <a name="how-to-control-an-animation-using-from-to-and-by"></a>Procédure : Contrôler une animation avec From, To et By
Un « From/To/By » ou « animation de base » crée une transition entre deux valeurs cibles (consultez [vue d’ensemble de l’Animation](animation-overview.md) pour une introduction aux différents types d’animations). Pour définir les valeurs cibles d’une animation de base, utilisez son <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A>, <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A>, et <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> propriétés.  Le tableau suivant résume comment la <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A>, <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A>, et <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> propriétés peuvent être utilisées ensemble ou séparément pour déterminer les cibles d’une animation les valeurs.  
  
|Propriétés spécifiées|Comportement obtenu|  
|--------------------------|------------------------|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.From%2A>|L’animation passe de la valeur spécifiée par la <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> valeur, selon la configuration de l’animation précédente de sortie à la propriété la valeur de base de la propriété animée ou à une animation précédente.|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> et <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A>|L’animation passe de la valeur spécifiée par le <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> valeur à la propriété spécifiée par le <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> propriété.|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> et <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A>|L’animation passe de la valeur spécifiée par le <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> valeur à la propriété spécifiée par la somme de la <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> et <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> propriétés.|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.To%2A>|L’animation progresse à partir de la valeur de base de la propriété animée ou d’une animation précédente valeur de sortie à la valeur spécifiée par le <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> propriété.|  
|<xref:System.Windows.Media.Animation.DoubleAnimation.By%2A>|L’animation passe de la valeur de base de la propriété animée ou d’une animation précédente valeur de sortie à la somme de cette valeur et la valeur spécifiée par le <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> propriété.|  
  
> [!NOTE]
>  Ne définissez pas les deux le <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A> propriété et le <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> propriété sur la même animation.  
  
 Pour utiliser d’autres méthodes d’interpolation ou effectuer une animation entre plus de deux valeurs cibles, utilisez une animation d’image clé. Consultez [vue d’ensemble des Animations image clé](key-frame-animations-overview.md) pour plus d’informations.  
  
 Pour plus d’informations sur l’application de plusieurs animations à une propriété unique, consultez [vue d’ensemble des Animations image clé](key-frame-animations-overview.md).  
  
 L’exemple ci-dessous montre les différents effets du paramètre <xref:System.Windows.Media.Animation.DoubleAnimation.To%2A>, <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A>, et <xref:System.Windows.Media.Animation.DoubleAnimation.From%2A> propriétés sur les animations.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[BasicAnimations_snippet#AnimationTargetValuesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snippet/CS/AnimationTargetValuesExample.xaml#animationtargetvalueswholepage)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’animation](animation-overview.md)
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Exemple de valeurs cibles d’animation From, To et By](https://go.microsoft.com/fwlink/?LinkID=159988)
