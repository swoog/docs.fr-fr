---
title: "Comment : vérifier qu'un GridSplitter est visible"
ms.date: 03/30/2017
helpviewer_keywords:
- GridSplitter control [WPF], ensuring visibility of
ms.assetid: 0a62a964-89c8-48f0-9023-5df721a8cf47
ms.openlocfilehash: 926df118bfd8e7ab3d1f0c953d0b6debafd59073
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-make-sure-that-a-gridsplitter-is-visible"></a>Comment : vérifier qu'un GridSplitter est visible
Cet exemple montre comment s’assurer un <xref:System.Windows.Controls.GridSplitter> contrôle n’est pas masqué par les autres contrôles dans un <xref:System.Windows.Controls.Grid>.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Controls.Panel.Children%2A> d’un <xref:System.Windows.Controls.Grid> contrôle sont rendus dans l’ordre qu’ils sont définis dans le balisage ou de code. <xref:System.Windows.Controls.GridSplitter> les contrôles peuvent être masqués par d’autres contrôles si vous ne les définissent pas en tant que les derniers éléments dans la <xref:System.Windows.Controls.Panel.Children%2A> collection, ou si vous donnez des autres contrôles est élevé, plus <xref:System.Windows.Controls.Panel.ZIndexProperty>.  
  
 Pour empêcher masqué <xref:System.Windows.Controls.GridSplitter> contrôles, effectuez l’une des opérations suivantes.  
  
-   Assurez-vous que <xref:System.Windows.Controls.GridSplitter> contrôles sont les dernières <xref:System.Windows.Controls.Panel.Children%2A> ajouté à la <xref:System.Windows.Controls.Grid>. L’exemple suivant illustre la <xref:System.Windows.Controls.GridSplitter> comme dernier élément dans le <xref:System.Windows.Controls.Panel.Children%2A> collection de la <xref:System.Windows.Controls.Grid>.  
  
 [!code-xaml[GridSplitterSnips#GridSplitterLastChild](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterlastchild)]  
  
-   Définir le <xref:System.Windows.Controls.Panel.ZIndexProperty> sur la <xref:System.Windows.Controls.GridSplitter> est supérieur à un contrôle qui serait le masquer dans le cas contraire. L’exemple suivant donne le <xref:System.Windows.Controls.GridSplitter> un degré plus élevé de contrôle <xref:System.Windows.Controls.Panel.ZIndexProperty> à la <xref:System.Windows.Controls.Button> contrôle.  
  
 [!code-xaml[GridSplitterSnips#GridSplitterZIndex](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterzindex)]  
  
-   Définir les marges du contrôle qui serait sinon masquer le <xref:System.Windows.Controls.GridSplitter> afin que le <xref:System.Windows.Controls.GridSplitter> est exposé. L’exemple suivant définit des marges sur un contrôle qui, sinon, chevaucherait et masquer le <xref:System.Windows.Controls.GridSplitter>.  
  
 [!code-xaml[GridSplitterSnips#GridSplitterMargin](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplittermargin)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.GridSplitter>  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/controls/gridsplitter-how-to-topics.md)
