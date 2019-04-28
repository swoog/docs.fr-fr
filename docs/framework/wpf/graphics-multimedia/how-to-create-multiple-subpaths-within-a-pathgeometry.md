---
title: 'Procédure : Créer plusieurs sous-chemins dans un PathGeometry'
ms.date: 03/30/2017
helpviewer_keywords:
- multiple subpaths [WPF]
- graphics [WPF], subpaths
- subpaths [WPF]
ms.assetid: 104a862c-dde2-4e62-ac87-80660dd1681c
ms.openlocfilehash: 286075448cd6a343f8a7b15b2b5005f840f68e1d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61904720"
---
# <a name="how-to-create-multiple-subpaths-within-a-pathgeometry"></a>Procédure : Créer plusieurs sous-chemins dans un PathGeometry
Cet exemple montre comment créer plusieurs sous-chemins dans un <xref:System.Windows.Media.PathGeometry>. Pour créer plusieurs sous-chemins, vous créez un <xref:System.Windows.Media.PathFigure> de chaque sous-tracé.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée deux sous-chemins, chacun d’eux un triangle.  
  
 [!code-xaml[GeometrySample#38](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/pathgeometryexample.xaml#38)]  
  
 L’exemple suivant montre comment créer plusieurs sous-chemins à l’aide un <xref:System.Windows.Shapes.Path> et [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] syntaxe d’attribut. Chaque `M` crée un sous-chemin de sorte que l’exemple crée deux sous-chemins qui dessinent chacun un triangle.  
  
 [!code-xaml[GeometrySample#58](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/geometryattributesyntaxexample.xaml#58)]  
  
 (Notez que cette syntaxe d’attribut crée en fait un <xref:System.Windows.Media.StreamGeometry>, une version légère d’une <xref:System.Windows.Media.PathGeometry>. (Pour plus d’informations, consultez la page [Syntaxe XAML pour les tracés](path-markup-syntax.md).)  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de Geometry](geometry-overview.md)
