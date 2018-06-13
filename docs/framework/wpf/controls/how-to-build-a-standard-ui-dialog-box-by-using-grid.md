---
title: "Comment : générer une boîte de dialogue d'interface utilisateur standard à l'aide de Grid"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dialog boxes [WPF], creating
- Grid control [WPF], creating [WPF], dialog box
ms.assetid: d6ac3d51-844b-4d29-96d8-81a696a7b960
ms.openlocfilehash: d0b24e320c2a341b069e1c9c3e8b6d5e93076733
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33551880"
---
# <a name="how-to-build-a-standard-ui-dialog-box-by-using-grid"></a>Comment : générer une boîte de dialogue d'interface utilisateur standard à l'aide de Grid
Cet exemple montre comment créer une norme [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] boîte de dialogue à l’aide de la <xref:System.Windows.Controls.Grid> élément.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une boîte de dialogue similaire à la **exécuter** boîte de dialogue de la [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] système d’exploitation.  
  
 L’exemple crée un <xref:System.Windows.Controls.Grid> et utilise le <xref:System.Windows.Controls.ColumnDefinition> et <xref:System.Windows.Controls.RowDefinition> classes pour définir cinq colonnes et quatre lignes.  
  
 L’exemple ajoute et positionne un <xref:System.Windows.Controls.Image>, `RunIcon.png`, pour représenter l’image qui se trouve dans la boîte de dialogue. L’image est placée dans la première colonne et ligne de la <xref:System.Windows.Controls.Grid> (angle supérieur gauche).  
  
 Ensuite, l’exemple ajoute un <xref:System.Windows.Controls.TextBlock> élément à la première colonne, qui couvre les colonnes restantes de la première ligne. Il ajoute un autre <xref:System.Windows.Controls.TextBlock> élément à la deuxième ligne de la première colonne, pour représenter le **ouvrir** zone de texte. A <xref:System.Windows.Controls.TextBlock> suit, qui représente la zone d’entrée de données.  
  
 Enfin, l’exemple ajoute trois <xref:System.Windows.Controls.Button> à la dernière ligne, les éléments qui représentent les **OK**, **Annuler**, et **Parcourir** événements.  
  
 [!code-csharp[GridRunDialog#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridRunDialog/CSharp/window1.xaml.cs#1)]
 [!code-vb[GridRunDialog#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/GridRunDialog/VisualBasic/grid_vb.vb#1)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.Grid>  
 <xref:System.Windows.GridUnitType>  
 [Vue d’ensemble de Panel](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/controls/grid-how-to-topics.md)
