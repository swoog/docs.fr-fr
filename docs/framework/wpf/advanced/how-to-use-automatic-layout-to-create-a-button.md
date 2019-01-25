---
title: 'Procédure : Utiliser la disposition automatique pour créer un bouton'
ms.date: 03/30/2017
helpviewer_keywords:
- Button controls [WPF], creating with automatic layout
- automatic layout [WPF], creating buttons
ms.assetid: 96c206d0-9e77-4784-9d2d-5045aed2021c
ms.openlocfilehash: 501341f0e71e6e5a224c51e4ae01c68ce6b845cb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54543485"
---
# <a name="how-to-use-automatic-layout-to-create-a-button"></a>Procédure : Utiliser la disposition automatique pour créer un bouton
Cet exemple décrit comment tirer parti de la disposition automatique pour créer un bouton dans une application localisable.  
  
 Localisation d’un [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] peut prendre beaucoup de temps. Les localisateurs doivent souvent redimensionner et repositionner les éléments, en plus de traduire le texte. Dans le passé chaque langue qu’un [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] était adaptée nécessitait un ajustement. Désormais avec les capacités de [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] vous pouvez concevoir des éléments qui réduisent les ajustements nécessaires. L’approche consistant à écrire des applications qui peuvent être plus facilement redimensionnées et repositionnées est appelée `automatic layout`.  
  
 Les deux [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples créent des applications qui instancient un bouton ; une en anglais et une en espagnol. Notez que le code est identique à l’exception du texte ; le bouton s’ajuste pour s’adapter au texte.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[LocalizationBtn_snip#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn_snip/CS/Pane1.xaml#1)]  
  
 [!code-xaml[LocalizationBtn#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn/CS/Pane1.xaml#1)]  
  
 Le graphique suivant illustre la sortie des exemples de code.  
  
 ![Même bouton avec le texte dans différentes langues](../../../../docs/framework/wpf/advanced/media/globalizationbutton.png "GlobalizationButton")  
Bouton redimensionnable automatiquement  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de l’utilisation de la disposition automatique](../../../../docs/framework/wpf/advanced/use-automatic-layout-overview.md)
- [Utiliser une grille pour la disposition automatique](../../../../docs/framework/wpf/advanced/how-to-use-a-grid-for-automatic-layout.md)
