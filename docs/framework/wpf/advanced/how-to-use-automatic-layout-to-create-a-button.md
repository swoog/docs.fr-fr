---
title: Guide pratique pour utiliser la disposition automatique pour créer un bouton
ms.date: 03/30/2017
helpviewer_keywords:
- Button controls [WPF], creating with automatic layout
- automatic layout [WPF], creating buttons
ms.assetid: 96c206d0-9e77-4784-9d2d-5045aed2021c
ms.openlocfilehash: 34b372e886b31e801b5598da90299f9815c47620
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-use-automatic-layout-to-create-a-button"></a>Guide pratique pour utiliser la disposition automatique pour créer un bouton
Cet exemple décrit comment tirer parti de la disposition automatique pour créer un bouton dans une application localisable.  
  
 Localisation d’un [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] peut prendre beaucoup de temps. Les localisateurs doivent souvent redimensionner et repositionner les éléments, en plus de traduire le texte. Dans le passé chaque langue qu’un [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] a été adaptée pour l’ajustement nécessaire. Désormais, avec les fonctionnalités de [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] vous pouvez concevoir des éléments qui réduisent les ajustements nécessaires. L’approche consistant à écrire des applications qui peuvent être plus faciles à redimensionner et repositionner est appelée `automatic layout`.  
  
 Les deux [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples de créent des applications qui instancie un bouton : un avec l’anglais et un avec l’espagnol. Notez que le code est identique à l’exception du texte ; le bouton s’ajuste pour s’adapter au texte.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[LocalizationBtn_snip#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn_snip/CS/Pane1.xaml#1)]  
  
 [!code-xaml[LocalizationBtn#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn/CS/Pane1.xaml#1)]  
  
 Le graphique suivant illustre la sortie des exemples de code.  
  
 ![Même bouton avec le texte dans différentes langues](../../../../docs/framework/wpf/advanced/media/globalizationbutton.png "GlobalizationButton")  
Bouton redimensionnable automatiquement  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble de l’utilisation de la disposition automatique](../../../../docs/framework/wpf/advanced/use-automatic-layout-overview.md)  
 [Utiliser une grille pour la disposition automatique](../../../../docs/framework/wpf/advanced/how-to-use-a-grid-for-automatic-layout.md)
