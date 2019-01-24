---
title: 'Procédure : Créer un élément de grille'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], creating [WPF], grid instance
ms.assetid: b2f07626-9df8-43b8-8d36-492f3cb42837
ms.openlocfilehash: b5bb9572b6a34b21208a8d8c0583068873772aae
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54726596"
---
# <a name="how-to-create-a-grid-element"></a>Procédure : Créer un élément de grille
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment créer et utiliser une instance de <xref:System.Windows.Controls.Grid> à l’aide [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] ou du code. Cet exemple utilise trois <xref:System.Windows.Controls.ColumnDefinition> objets et trois <xref:System.Windows.Controls.RowDefinition> objets pour créer une grille qui a neuf cellules, comme dans une feuille de calcul. Chaque cellule contient un <xref:System.Windows.Controls.TextBlock> élément qui représente les données et la ligne supérieure contient un <xref:System.Windows.Controls.TextBlock> avec le <xref:System.Windows.Controls.Grid.ColumnSpan%2A> propriété appliqué. Pour afficher les limites de chaque cellule, le <xref:System.Windows.Controls.Grid.ShowGridLines%2A> propriété est activée.  
  
 [!code-csharp[Grid#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Grid/CSharp/Grid_Code.cs#3)]
 [!code-vb[Grid#3](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Grid/VisualBasic/grid_vb.vb#3)]
 [!code-xaml[Grid#3](../../../../samples/snippets/xaml/VS_Snippets_Wpf/Grid/XAML/default.xaml#3)]  
  
  Chacune de ces approches génère une interface utilisateur qui ressemble beaucoup, comme celui ci-dessous.

  ![une capture d’écran illustre une interface utilisateur WPF qui contient une grille divisée en trois colonnes.  Il porte l’en-tête '2018 produits fournis » s’étendant sur toutes les colonnes de la ligne du haut et a trois colonnes avec des chiffres de ventes pour un certain trimestre.  La ligne inférieure comporte du texte s’étendant sur deux colonnes avec le message « nombre Total d’unités : 300,000'](./media/how-to-create-a-grid-element/how-to-create-a-grid-element.png)
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.Grid>
- [Vue d’ensemble de Panel](../../../../docs/framework/wpf/controls/panels-overview.md)
