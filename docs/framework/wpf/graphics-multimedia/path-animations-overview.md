---
title: Vue d'ensemble des animations de tracés
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], paths
- path animations [WPF]
ms.assetid: 979c732c-df74-47a6-be96-8e07b3707d53
ms.openlocfilehash: 0f795ad00823e7b1c37221f7417b09d3982c4c18
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47216927"
---
# <a name="path-animations-overview"></a>Vue d'ensemble des animations de tracés
<a name="introduction"></a> Cette rubrique présente les animations de tracés qui vous permettent d’utiliser un tracé géométrique pour générer des valeurs de sortie. Les animations de tracés sont utiles pour déplacer et faire pivoter des objets le long des tracés complexes.  
  
<a name="prerequisites"></a>   
## <a name="prerequisites"></a>Prérequis  
 Pour comprendre cette rubrique, vous devez être familiarisé avec [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] fonctionnalités d’animations. Pour une introduction aux fonctionnalités d’animation, consultez le [vue d’ensemble de l’Animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md).  
  
 Étant donné que vous utilisez un <xref:System.Windows.Media.PathGeometry> objet pour définir une animation de tracés, vous devez également être familiarisé avec <xref:System.Windows.Media.PathGeometry> et les différents types de <xref:System.Windows.Media.PathSegment> objets. Pour plus d’informations, consultez le [vue d’ensemble de Geometry](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md).  
  
<a name="what_is_a_path_animation"></a>   
## <a name="what-is-a-path-animation"></a>Qu’est-ce qu’une animation de tracés ?  
 Une animation de tracés est un type de <xref:System.Windows.Media.Animation.AnimationTimeline> qui utilise un <xref:System.Windows.Media.PathGeometry> comme entrée. Au lieu de définir un From, de propriété, ou par (comme vous le feriez pour un From/To/By animation) ou à l’aide d’images clés (que vous utiliseriez pour une animation d’image clé), vous définissez un tracé géométrique et utilisez-le pour définir le `PathGeometry` propriété de l’animation de tracés. À mesure que l’animation de tracés avance, elle lit les informations relatives aux coordonnées x, y et à l’angle à partir du tracé et les utilise pour générer sa sortie.  
  
 Les animations de tracés sont très utiles pour animer un objet le long d’un tracé complexe. Une façon de déplacer un objet sur un tracé consiste à utiliser un <xref:System.Windows.Media.MatrixTransform> et un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> pour transformer un objet sur un tracé complex. L’exemple suivant illustre cette technique à l’aide de la <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> objet à animer le <xref:System.Windows.Media.MatrixTransform.Matrix%2A> propriété d’un <xref:System.Windows.Media.MatrixTransform>. Le <xref:System.Windows.Media.MatrixTransform> est appliqué à un bouton et oblige ce dernier à déplacer sur un tracé courbé. Étant donné que le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> propriété est définie sur `true`, le rectangle pivote le long de la tangente du chemin d’accès.  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathdoesrotatewithtangentexample.xaml#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathDoesRotateWithTangentExample.cs#matrixanimationusingpathdoesrotatewithtangentwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathDoesRotateWithTangentExample.vb#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 Pour plus d’informations sur la syntaxe de chemin d’accès qui est utilisée dans le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] exemple, consultez le [syntaxe de balisage de chemin d’accès](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md) vue d’ensemble. Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).  
  
 Vous pouvez appliquer une animation de tracés à une propriété à l’aide un <xref:System.Windows.Media.Animation.Storyboard> dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] et de code, ou en utilisant le <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> méthode dans le code. Vous pouvez également utiliser une animation de tracés pour créer un <xref:System.Windows.Media.Animation.AnimationClock> et l’appliquer à une ou plusieurs propriétés. Pour plus d’informations sur les différentes méthodes pour appliquer des animations, consultez [vue d’ensemble des Techniques d’Animation propriété](../../../../docs/framework/wpf/graphics-multimedia/property-animation-techniques-overview.md).  
  
<a name="animation_types"></a>   
## <a name="path-animation-types"></a>Types d’animation de tracés  
 Étant donné que les animations génèrent des valeurs de propriété, il existe différents types d’animation pour différents types de propriété. Pour animer une propriété qui accepte un <xref:System.Double> (telles que la <xref:System.Windows.Media.TranslateTransform.X%2A> propriété d’un <xref:System.Windows.Media.TranslateTransform>), vous utilisez une animation qui produit <xref:System.Double> valeurs. Pour animer une propriété qui accepte un <xref:System.Windows.Point>, utilisez une animation qui produit <xref:System.Windows.Point> valeurs et ainsi de suite.  
  
 Classes d’animation de tracé appartiennent à la <xref:System.Windows.Media.Animation> espace de noms et utilisent la convention d’affectation de noms suivante :  
  
 *\<Type>* `AnimationUsingPath`  
  
 Où  *\<Type >* est le type de valeur que la classe anime.  
  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] fournit les classes d’animation de tracés suivantes.  
  
|Type de propriété|Classe d’animation de tracés correspondante|Exemple|  
|-------------------|----------------------------------------|-------------|  
|<xref:System.Double>|<xref:System.Windows.Media.Animation.DoubleAnimationUsingPath>|[Animer un objet sur un tracé (animation double)](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-double-animation.md)|  
|<xref:System.Windows.Media.Matrix>|<xref:System.Windows.Media.Animation.MatrixAnimationUsingPath>|[Animer un objet sur un tracé (animation de matrice)](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-matrix-animation.md)|  
|<xref:System.Windows.Point>|<xref:System.Windows.Media.Animation.PointAnimationUsingPath>|[Animer un objet sur un tracé (animation de point)](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-point-animation.md)|  
  
 Un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> génère <xref:System.Windows.Media.Matrix> les valeurs de ses <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.PathGeometry%2A>. Lorsqu’il est utilisé avec un <xref:System.Windows.Media.MatrixTransform>, un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> peut déplacer un objet sur un tracé. Si vous définissez la <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> propriété de la <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> à `true`, il fait également pivoter l’objet le long des courbes du tracé.  
  
 Un <xref:System.Windows.Media.Animation.PointAnimationUsingPath> génère <xref:System.Windows.Point> valeurs de coordonnées x et y de son <xref:System.Windows.Media.Animation.PointAnimationUsingPath.PathGeometry%2A>. En utilisant un <xref:System.Windows.Media.Animation.PointAnimationUsingPath> pour animer une propriété qui accepte <xref:System.Windows.Point> valeurs, vous pouvez déplacer un objet le long d’un chemin d’accès. Un <xref:System.Windows.Media.Animation.PointAnimationUsingPath> ne peut pas faire pivoter des objets.  
  
 Un <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> génère <xref:System.Double> les valeurs de ses <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath.PathGeometry%2A>. En définissant le <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath.Source%2A> propriété, vous pouvez spécifier si le <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> utilise la coordonnée x, la coordonnée y ou l’angle du tracé comme sortie. Vous pouvez utiliser un <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> pour faire pivoter un objet ou le déplacer sur l’axe x ou l’axe des ordonnées.  
  
<a name="pathanimationinput"></a>   
## <a name="path-animation-input"></a>Entrée d’animation de tracés  
 Chaque classe d’animation de tracé fournit un <xref:System.Windows.Media.PathGeometry> propriété pour spécifier son entrée. L’animation de tracés utilise le <xref:System.Windows.Media.PathGeometry> pour générer ses valeurs de sortie. Le <xref:System.Windows.Media.PathGeometry> classe vous permet de décrire plusieurs figures complexes composées d’arcs, de courbes et de lignes.  
  
 Au cœur d’un <xref:System.Windows.Media.PathGeometry> est une collection de <xref:System.Windows.Media.PathFigure> objets ; ces objets sont nommés ainsi car chaque figure décrit une forme discrète dans le <xref:System.Windows.Media.PathGeometry>. Chaque <xref:System.Windows.Media.PathFigure> se compose d’une ou plusieurs <xref:System.Windows.Media.PathSegment> objets, chacun d'entre eux décrivant un segment de la figure.  
  
 Il existe un grand nombre de segments.  
  
|Type de segment|Description|  
|------------------|-----------------|  
|<xref:System.Windows.Media.ArcSegment>|Crée un arc elliptique entre deux points.|  
|<xref:System.Windows.Media.BezierSegment>|Crée une courbe de Bézier cubique entre deux points.|  
|<xref:System.Windows.Media.LineSegment>|Crée une ligne entre deux points.|  
|<xref:System.Windows.Media.PolyBezierSegment>|Crée une série de courbes de Bézier cubiques.|  
|<xref:System.Windows.Media.PolyLineSegment>|Crée une série de lignes.|  
|<xref:System.Windows.Media.PolyQuadraticBezierSegment>|Crée une série de courbes de Bézier quadratiques.|  
|<xref:System.Windows.Media.QuadraticBezierSegment>|Crée une courbe de Bézier quadratique.|  
  
 Les segments dans un <xref:System.Windows.Media.PathFigure> sont combinés en une seule forme géométrique, qui utilise le point de terminaison d’un segment en tant que le point de départ du segment suivant. Le <xref:System.Windows.Media.PathFigure.StartPoint%2A> propriété d’un <xref:System.Windows.Media.PathFigure> Spécifie le point à partir de laquelle le premier segment est tracé. Chaque segment suivant démarre au point de fin du segment précédent. Par exemple, une ligne verticale entre `10,50` à `10,150` peut être définie en configurant le <xref:System.Windows.Media.PathFigure.StartPoint%2A> propriété `10,50` et la création d’un <xref:System.Windows.Media.LineSegment> avec un <xref:System.Windows.Media.LineSegment.Point%2A> paramètre de propriété de `10,150`.  
  
 Pour plus d’informations sur <xref:System.Windows.Media.PathGeometry> , voir la [vue d’ensemble de Geometry](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md).  
  
 Dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez également utiliser une syntaxe abrégée spéciale pour définir le <xref:System.Windows.Media.PathGeometry.Figures%2A> propriété d’un <xref:System.Windows.Media.PathGeometry>. Pour plus d’informations, consultez [syntaxe de balisage de chemin d’accès](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md) vue d’ensemble.  
  
 Pour plus d’informations sur la syntaxe de chemin d’accès qui est utilisée dans le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] exemple, consultez le [syntaxe de balisage de chemin d’accès](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md) vue d’ensemble.  
  
## <a name="see-also"></a>Voir aussi  
 [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028)  
 [Syntaxe XAML pour les tracés](../../../../docs/framework/wpf/graphics-multimedia/path-markup-syntax.md)  
 [Guides pratiques relatifs aux animations de tracés](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)  
 [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [Vue d’ensemble des techniques d’animation de propriétés](../../../../docs/framework/wpf/graphics-multimedia/property-animation-techniques-overview.md)
