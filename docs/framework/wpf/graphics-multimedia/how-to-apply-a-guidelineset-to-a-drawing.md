---
title: 'Procédure : Appliquer un GuidelineSet à un dessin'
ms.date: 03/30/2017
helpviewer_keywords:
- GuidelineSet property [WPF], applying to drawings
- graphics [WPF], GuidelineSet property
ms.assetid: 45f3e0b4-8820-45a7-b865-b8ea5b17b0c8
ms.openlocfilehash: 4bd2ee349f2c1855a9af6b4c00f2630cd50a9108
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493376"
---
# <a name="how-to-apply-a-guidelineset-to-a-drawing"></a>Procédure : Appliquer un GuidelineSet à un dessin
Cet exemple montre comment appliquer un <xref:System.Windows.Media.GuidelineSet> à un <xref:System.Windows.Media.DrawingGroup>.  
  
 Le <xref:System.Windows.Media.DrawingGroup> classe est le seul type de <xref:System.Windows.Media.Drawing> qui a un <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> propriété. Pour appliquer un <xref:System.Windows.Media.GuidelineSet> à un autre type de <xref:System.Windows.Media.Drawing>, ajoutez-le à un <xref:System.Windows.Media.DrawingGroup> , puis appliquez le <xref:System.Windows.Media.GuidelineSet> à votre <xref:System.Windows.Media.DrawingGroup>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée deux <xref:System.Windows.Media.DrawingGroup> les objets qui sont presque identiques ; la seule différence est : le second <xref:System.Windows.Media.DrawingGroup> a un <xref:System.Windows.Media.GuidelineSet> et n’est pas le cas de la première.  
  
 L’illustration suivante montre la sortie de l’exemple. Étant donné que la différence de rendu entre les deux <xref:System.Windows.Media.DrawingGroup> objets étant très subtile, certaines parties des dessins sont agrandies.  
  
 ![DrawingGroup avec et sans GuidelineSet](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-drawinggroup-guidelineset.png "graphicsmm_drawinggroup_guidelineset")  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMDrawingGroupGuidelineSetExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupGuidelineSetExample.cs#graphicsmmdrawinggroupguidelinesetexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMDrawingGroupGuidelineSetExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupGuidelineSetExample.xaml#graphicsmmdrawinggroupguidelinesetexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.GuidelineSet>
- [Vue d’ensemble des objets de dessin](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
