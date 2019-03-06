---
title: "Procédure : Définir l'alignement horizontal et vertical d'un TileBrush"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TileBrush [WPF], alignment of
- vertical alignment of TileBrushes [WPF]
- aligning [WPF], TileBrushes
- horizontal alignment of Tilebrushes [WPF]
ms.assetid: 65ae89bd-9246-4c9e-bde4-2fb991d4060d
ms.openlocfilehash: d18e4a9fe4f99c1947402c252082e1580a0b22cc
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57352553"
---
# <a name="how-to-set-the-horizontal-and-vertical-alignment-of-a-tilebrush"></a>Procédure : Définir l'alignement horizontal et vertical d'un TileBrush
Cet exemple montre comment contrôler l’alignement horizontal et vertical d’un contenu dans une mosaïque. Pour contrôler l’alignement horizontal et vertical d’un <xref:System.Windows.Media.TileBrush>, utilisez son <xref:System.Windows.Media.TileBrush.AlignmentX%2A> et <xref:System.Windows.Media.TileBrush.AlignmentY%2A> propriétés.  
  
 Le <xref:System.Windows.Media.TileBrush.AlignmentX%2A> et <xref:System.Windows.Media.TileBrush.AlignmentY%2A> propriétés d’un <xref:System.Windows.Media.TileBrush> sont utilisées lorsque une des conditions suivantes est vraie :  
  
-   Le <xref:System.Windows.Media.TileBrush.Stretch%2A> propriété est <xref:System.Windows.Media.Stretch.Uniform> ou <xref:System.Windows.Media.Stretch.UniformToFill> et <xref:System.Windows.Media.TileBrush.Viewbox%2A> et <xref:System.Windows.Media.TileBrush.Viewport%2A> ont des proportions différentes.  
  
-   Le <xref:System.Windows.Media.TileBrush.Stretch%2A> propriété est <xref:System.Windows.Media.Stretch.None> et <xref:System.Windows.Media.TileBrush.Viewbox%2A> et <xref:System.Windows.Media.TileBrush.Viewport%2A> sont de tailles différentes.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant aligne le contenu d’un <xref:System.Windows.Media.DrawingBrush>, qui est un type de <xref:System.Windows.Media.TileBrush>, à l’angle supérieur gauche de sa mosaïque. Pour aligner le contenu, l’exemple définit le <xref:System.Windows.Media.TileBrush.AlignmentX%2A> propriété de la <xref:System.Windows.Media.DrawingBrush> à <xref:System.Windows.Media.AlignmentX.Left> et <xref:System.Windows.Media.TileBrush.AlignmentY%2A> propriété <xref:System.Windows.Media.AlignmentY.Top>. Cet exemple produit la sortie suivante.  
  
 ![TileBrush avec haut&#45;alignement gauche](./media/graphicsmm-tilebrushalignmentexampletopleft.png "graphicsmm_TileBrushAlignmentExampleTopLeft")  
TileBrush avec un contenu aligné dans l’angle supérieur gauche  
  
 [!code-csharp[brushoverviewexamples_snip#TileBrushTopLeftAlignmentInline](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_snip/CSharp/TileBrushAlignmentExample.cs#tilebrushtopleftalignmentinline)]
 [!code-vb[brushoverviewexamples_snip#TileBrushTopLeftAlignmentInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_snip/visualbasic/tilebrushalignmentexample.vb#tilebrushtopleftalignmentinline)]
 [!code-xaml[brushoverviewexamples_snip#TileBrushTopLeftAlignmentInline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileBrushAlignmentExample.xaml#tilebrushtopleftalignmentinline)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant aligne le contenu d’un <xref:System.Windows.Media.DrawingBrush> vers le coin inférieur droit de sa mosaïque en définissant le <xref:System.Windows.Media.TileBrush.AlignmentX%2A> propriété <xref:System.Windows.Media.AlignmentX.Right> et <xref:System.Windows.Media.TileBrush.AlignmentY%2A> propriété <xref:System.Windows.Media.AlignmentY.Bottom>. L’exemple produit le résultat suivant :  
  
 ![TileBrush avec bas&#45;avec le bouton droit alignement](./media/graphicsmm-tilebrushalignmentexamplebottomright.png "graphicsmm_TileBrushAlignmentExampleBottomRight")  
TileBrush avec un contenu aligné dans l’angle inférieur droit  
  
 [!code-csharp[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_snip/CSharp/TileBrushAlignmentExample.cs#tilebrushbottomrightalignmentinline)]
 [!code-vb[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_snip/visualbasic/tilebrushalignmentexample.vb#tilebrushbottomrightalignmentinline)]
 [!code-xaml[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileBrushAlignmentExample.xaml#tilebrushbottomrightalignmentinline)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant aligne le contenu d’un <xref:System.Windows.Media.DrawingBrush> à l’angle supérieur gauche de sa mosaïque en définissant le <xref:System.Windows.Media.TileBrush.AlignmentX%2A> propriété <xref:System.Windows.Media.AlignmentX.Left> et <xref:System.Windows.Media.TileBrush.AlignmentY%2A> propriété <xref:System.Windows.Media.AlignmentY.Top>. Il définit également la <xref:System.Windows.Media.TileBrush.Viewport%2A> et <xref:System.Windows.Media.TileBrush.TileMode%2A> de la <xref:System.Windows.Media.DrawingBrush> pour produire un modèle en mosaïque. L’exemple produit le résultat suivant :  
  
 ![TileBrush en mosaïque avec haut&#45;alignement gauche](./media/graphicsmm-tilebrushalignmentexampletoplefttiled.png "graphicsmm_TileBrushAlignmentExampleTopLeftTiled")  
Modèle de mosaïque avec contenu aligné en haut à gauche dans la mosaïque de base  
  
 L’illustration montre la mosaïque pour que vous puissiez voir comment son contenu est aligné. Notez que le <xref:System.Windows.Media.TileBrush.AlignmentX%2A> paramètre n’a aucun effet car le contenu de la <xref:System.Windows.Media.DrawingBrush> remplit horizontalement toute la mosaïque de base.  
  
 [!code-csharp[brushoverviewexamples_snip#TileBrushTopLeftAlignmentTiledInline](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_snip/CSharp/TileBrushAlignmentExample.cs#tilebrushtopleftalignmenttiledinline)]
 [!code-vb[brushoverviewexamples_snip#TileBrushTopLeftAlignmentTiledInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_snip/visualbasic/tilebrushalignmentexample.vb#tilebrushtopleftalignmenttiledinline)]
 [!code-xaml[brushoverviewexamples_snip#TileBrushTopLeftAlignmentTiledInline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileBrushAlignmentExample.xaml#tilebrushtopleftalignmenttiledinline)]  
  
## <a name="example"></a>Exemple  
 Le dernier exemple aligne le contenu d’une mosaïque <xref:System.Windows.Media.DrawingBrush> à l’angle inférieur droit de sa mosaïque de base en définissant le <xref:System.Windows.Media.TileBrush.AlignmentX%2A> propriété <xref:System.Windows.Media.AlignmentX.Right> et <xref:System.Windows.Media.TileBrush.AlignmentY%2A> propriété <xref:System.Windows.Media.AlignmentY.Bottom>. L’exemple produit le résultat suivant :  
  
 ![TileBrush en mosaïque avec bas&#45;avec le bouton droit alignement](./media/graphicsmm-tilebrushalignmentexamplebottomrighttiled.png "graphicsmm_TileBrushAlignmentExampleBottomRightTiled")  
Modèle de mosaïque avec contenu aligné en bas à droite dans la mosaïque de base  
  
 Là encore, le <xref:System.Windows.Media.TileBrush.AlignmentX%2A> paramètre n’a aucun effet car le contenu de la <xref:System.Windows.Media.DrawingBrush> remplit horizontalement toute la mosaïque de base.  
  
 [!code-csharp[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushOverviewExamples_snip/CSharp/TileBrushAlignmentExample.cs#tilebrushbottomrightalignmentinline)]
 [!code-vb[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushOverviewExamples_snip/visualbasic/tilebrushalignmentexample.vb#tilebrushbottomrightalignmentinline)]
 [!code-xaml[brushoverviewexamples_snip#TileBrushBottomRightAlignmentInline](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushOverviewExamples_snip/XAML/TileBrushAlignmentExample.xaml#tilebrushbottomrightalignmentinline)]  
  
 Les exemples utilisent <xref:System.Windows.Media.DrawingBrush> objets afin d’illustrer comment le <xref:System.Windows.Media.TileBrush.AlignmentX%2A> et <xref:System.Windows.Media.TileBrush.AlignmentY%2A> propriétés sont utilisées. Ces propriétés ont un comportement identique pour tous les pinceaux de mosaïque : <xref:System.Windows.Media.DrawingBrush>, <xref:System.Windows.Media.ImageBrush>, et <xref:System.Windows.Media.VisualBrush>. Pour plus d’informations sur les pinceaux mosaïques, consultez l’article [Peinture avec des objets d’image, de dessin et visuels](painting-with-images-drawings-and-visuals.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.DrawingBrush>
- <xref:System.Windows.Media.ImageBrush>
- <xref:System.Windows.Media.VisualBrush>
- [Peinture avec des images, des dessins et des objets visuels](painting-with-images-drawings-and-visuals.md)
