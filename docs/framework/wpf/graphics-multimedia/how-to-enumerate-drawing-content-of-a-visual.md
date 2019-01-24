---
title: "Procédure : Énumérer le contenu de dessin d'un Visual"
ms.date: 03/30/2017
helpviewer_keywords:
- retrieving the DrawingGroup value of a Visual [WPF]
- enumerating the contents of a Visual [WPF]
ms.assetid: 2974ddb3-2997-4713-8fd2-e93d549c58a8
ms.openlocfilehash: a3131b6c86b0f6a7aa79cca305b9c3b2496346f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561946"
---
# <a name="how-to-enumerate-drawing-content-of-a-visual"></a>Procédure : Énumérer le contenu de dessin d'un Visual
Le <xref:System.Windows.Media.Drawing> objet fournissent un modèle d’objet pour énumérer le contenu d’un <xref:System.Windows.Media.Visual>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> méthode pour récupérer le <xref:System.Windows.Media.DrawingGroup> valeur d’un <xref:System.Windows.Media.Visual> et l’énumérer.  
  
> [!NOTE]
>  Lorsque vous énumérez le contenu de l’élément visuel, vous récupérez <xref:System.Windows.Media.Drawing> objets et pas la représentation sous-jacente des données rendues comme une liste d’instructions de graphismes vectoriels. Pour plus d’informations, consultez [Vue d’ensemble du rendu graphique WPF](../../../../docs/framework/wpf/graphics-multimedia/wpf-graphics-rendering-overview.md).  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMRetrieveDrawings](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/EnumerateDrawingsExample.xaml.cs#graphicsmmretrievedrawings)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.Drawing>
- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.VisualTreeHelper>
- [Vue d’ensemble des objets de dessin](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
- [Vue d’ensemble du rendu graphique de WPF](../../../../docs/framework/wpf/graphics-multimedia/wpf-graphics-rendering-overview.md)
