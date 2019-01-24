---
title: "Procédure : Vérifier qu'un GridSplitter est visible"
ms.date: 03/30/2017
helpviewer_keywords:
- GridSplitter control [WPF], ensuring visibility of
ms.assetid: 0a62a964-89c8-48f0-9023-5df721a8cf47
ms.openlocfilehash: 52a995a411614bcb677e34c563ad897637742c94
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54622479"
---
# <a name="how-to-make-sure-that-a-gridsplitter-is-visible"></a>Procédure : Vérifier qu'un GridSplitter est visible
Cet exemple montre comment vérifier une <xref:System.Windows.Controls.GridSplitter> contrôle n’est pas masqué par les autres contrôles dans un <xref:System.Windows.Controls.Grid>.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Controls.Panel.Children%2A> d’un <xref:System.Windows.Controls.Grid> contrôle sont rendus dans l’ordre qu’ils sont définis dans le balisage ou de code. <xref:System.Windows.Controls.GridSplitter> les contrôles peuvent être masqués par d’autres contrôles si vous ne définissez pas comme les derniers éléments dans le <xref:System.Windows.Controls.Panel.Children%2A> collection, ou si vous donnez des autres contrôles un degré plus élevé <xref:System.Windows.Controls.Panel.ZIndexProperty>.  
  
 Pour empêcher masqué <xref:System.Windows.Controls.GridSplitter> contrôles, effectuez l’une des opérations suivantes.  
  
-   Assurez-vous que l’option <xref:System.Windows.Controls.GridSplitter> contrôles sont les dernières <xref:System.Windows.Controls.Panel.Children%2A> ajouté à la <xref:System.Windows.Controls.Grid>. L’exemple suivant montre le <xref:System.Windows.Controls.GridSplitter> en tant que le dernier élément dans le <xref:System.Windows.Controls.Panel.Children%2A> collection de la <xref:System.Windows.Controls.Grid>.  
  
 [!code-xaml[GridSplitterSnips#GridSplitterLastChild](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterlastchild)]  
  
-   Définir le <xref:System.Windows.Controls.Panel.ZIndexProperty> sur la <xref:System.Windows.Controls.GridSplitter> supérieure à un contrôle qui masquez-le dans le cas contraire. L’exemple suivant donne le <xref:System.Windows.Controls.GridSplitter> contrôler un degré plus élevé <xref:System.Windows.Controls.Panel.ZIndexProperty> que le <xref:System.Windows.Controls.Button> contrôle.  
  
 [!code-xaml[GridSplitterSnips#GridSplitterZIndex](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterzindex)]  
  
-   Définissez des marges sur le contrôle qui, sinon, masquerait le <xref:System.Windows.Controls.GridSplitter> afin que le <xref:System.Windows.Controls.GridSplitter> est exposé. L’exemple suivant définit les marges sur un contrôle qui, sinon, chevaucherait et masquer le <xref:System.Windows.Controls.GridSplitter>.  
  
 [!code-xaml[GridSplitterSnips#GridSplitterMargin](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplittermargin)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.GridSplitter>
- [Rubriques de guide pratique](../../../../docs/framework/wpf/controls/gridsplitter-how-to-topics.md)
