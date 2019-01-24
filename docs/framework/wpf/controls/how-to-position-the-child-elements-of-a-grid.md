---
title: "Procédure : Positionner les éléments enfants d'une grille"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], positioning child elements
ms.assetid: 27b3ba9b-ad32-44e2-bcab-a79d573a463c
ms.openlocfilehash: a1b567356588d6798bae5d73d3d410882d087986
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538672"
---
# <a name="how-to-position-the-child-elements-of-a-grid"></a>Procédure : Positionner les éléments enfants d'une grille
Cet exemple montre comment obtenir et définir des méthodes qui sont définies sur <xref:System.Windows.Controls.Grid> pour positionner des éléments enfants.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit un parent <xref:System.Windows.Controls.Grid> élément (`grid1`) qui a trois colonnes et trois lignes. Un enfant <xref:System.Windows.Shapes.Rectangle> élément (`rect1`) est ajouté à la <xref:System.Windows.Controls.Grid> position de colonne zéro, position de ligne zéro. <xref:System.Windows.Controls.Button> les éléments représentent les méthodes qui peuvent être appelées pour repositionner le <xref:System.Windows.Shapes.Rectangle> élément dans le <xref:System.Windows.Controls.Grid>. Lorsqu’un utilisateur clique sur un bouton, la méthode associée est activée.  
  
 [!code-xaml[gridGetSetMethods](../../../../samples/snippets/csharp/VS_Snippets_Wpf/gridGetSetMethods/CSharp/Window1.xaml)]  
  
 L’exemple de code-behind suivant gère les méthodes que le bouton <xref:System.Windows.Controls.Primitives.ButtonBase.Click> déclenchent des événements. L’exemple écrit ces appels de méthode <xref:System.Windows.Controls.TextBlock> éléments liée de l’utilisation des méthodes get pour les nouvelles valeurs de propriété sous forme de chaînes de sortie.  
  
 [!code-csharp[gridGetSetMethods#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/gridGetSetMethods/CSharp/Window1.xaml.cs#2)]
 [!code-vb[gridGetSetMethods#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/gridGetSetMethods/VisualBasic/Window1.xaml.vb#2)]  
 Voici le résultat final !
 
 ![une capture d’écran illustre une interface utilisateur WPF avec deux colonnes, la partie droite a une grille de 3 x 3 et gauche comprend des boutons pour déplacer un rectangle coloré entre les colonnes et les lignes de la grille](./media/grid-methods-sample.png) 
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.Grid>
- [Vue d’ensemble de Panel](../../../../docs/framework/wpf/controls/panels-overview.md)
