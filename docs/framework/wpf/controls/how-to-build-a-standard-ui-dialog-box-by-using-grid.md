---
title: 'Procédure : Générer une boîte de dialogue d’interface utilisateur standard à l’aide d’une grille'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dialog boxes [WPF], creating
- Grid control [WPF], creating [WPF], dialog box
ms.assetid: d6ac3d51-844b-4d29-96d8-81a696a7b960
ms.openlocfilehash: 0ade908e92e552017acb9ba242ccba2c28c3c995
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59149524"
---
# <a name="how-to-build-a-standard-ui-dialog-box-by-using-grid"></a>Procédure : Générer une boîte de dialogue d’interface utilisateur standard à l’aide d’une grille
Cet exemple montre comment créer une norme [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] boîte de dialogue à l’aide de la <xref:System.Windows.Controls.Grid> élément.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une boîte de dialogue similaire à la **exécuter** boîte de dialogue dans le [!INCLUDE[TLA#tla_mswin](../../../../includes/tlasharptla-mswin-md.md)] système d’exploitation.  
  
 L’exemple crée un <xref:System.Windows.Controls.Grid> et utilise le <xref:System.Windows.Controls.ColumnDefinition> et <xref:System.Windows.Controls.RowDefinition> classes pour définir les cinq colonnes et quatre lignes.  
  
 L’exemple ajoute et positionne un <xref:System.Windows.Controls.Image>, `RunIcon.png`, pour représenter l’image qui se trouve dans la boîte de dialogue. L’image est placée dans la première colonne et ligne de la <xref:System.Windows.Controls.Grid> (le coin supérieur droit).  
  
 Ensuite, l’exemple ajoute un <xref:System.Windows.Controls.TextBlock> élément à la première colonne, qui couvre les colonnes restantes de la première ligne. Il ajoute un autre <xref:System.Windows.Controls.TextBlock> élément à la deuxième ligne dans la première colonne, pour représenter le **Open** zone de texte. Un <xref:System.Windows.Controls.TextBlock> suit, ce qui représente la zone de saisie de données.  
  
 Enfin, l’exemple ajoute trois <xref:System.Windows.Controls.Button> à la dernière ligne, les éléments qui représentent le **OK**, **Annuler**, et **Parcourir** événements.  
  
 [!code-csharp[GridRunDialog#1](~/samples/snippets/csharp/VS_Snippets_Wpf/GridRunDialog/CSharp/window1.xaml.cs#1)]
 [!code-vb[GridRunDialog#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GridRunDialog/VisualBasic/grid_vb.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.GridUnitType>
- [Vue d'ensemble de Panel](panels-overview.md)
- [Rubriques Comment](grid-how-to-topics.md)
