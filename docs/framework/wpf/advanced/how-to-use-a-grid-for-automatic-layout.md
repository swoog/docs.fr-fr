---
title: 'Procédure : Utiliser une grille pour la disposition automatique'
ms.date: 03/30/2017
helpviewer_keywords:
- grids [WPF], automatic layout
- automatic layout [WPF], grid use
ms.assetid: ab9de407-e0c1-4047-bdf0-24951bf73879
ms.openlocfilehash: 5fa023002ac66a65e3c179434841c975287d170c
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357480"
---
# <a name="how-to-use-a-grid-for-automatic-layout"></a>Procédure : Utiliser une grille pour la disposition automatique
Cet exemple décrit comment utiliser une grille quand vous tirez parti de la disposition automatique pour créer une application localisable.  
  
 Localisation d’un [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] peut prendre beaucoup de temps. Les localisateurs doivent souvent redimensionner et repositionner les éléments, en plus de traduire le texte. Dans le passé chaque langue qu’un [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] était adaptée nécessitait un ajustement. Désormais avec les capacités de [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] vous pouvez concevoir des éléments qui réduisent les ajustements nécessaires. L’approche consistant à écrire des applications qui peuvent être plus facilement redimensionnées et repositionnées est appelée `auto layout`.  
  
 Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemple illustre l’utilisation d’une grille pour positionner des boutons et du texte. Notez que la hauteur et la largeur des cellules sont définies sur `Auto`; par conséquent, la cellule qui contient le bouton avec une image s’ajuste pour s’ajuster à l’image. Étant donné que le <xref:System.Windows.Controls.Grid> élément pouvant s’ajuster à son contenu, il peut être utile lorsque vous effectuez l’approche de la disposition automatique pour concevoir des applications qui peuvent être localisées.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser une grille.  
  
 [!code-xaml[LocalizationGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationGrid/CS/Pane1.xaml#1)]  
  
 Le graphique suivant montre la sortie générée par l’exemple de code.  
  
 ![Exemple de grille](./media/glob-grid.png "glob_grid")  
Grille  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de l’utilisation de la disposition automatique](use-automatic-layout-overview.md)
- [Utiliser la disposition automatique pour créer un bouton](how-to-use-automatic-layout-to-create-a-button.md)
