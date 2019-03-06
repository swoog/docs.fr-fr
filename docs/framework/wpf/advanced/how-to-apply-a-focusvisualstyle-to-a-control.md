---
title: 'Procédure : Appliquer un FocusVisualStyle à un contrôle'
ms.date: 03/30/2017
helpviewer_keywords:
- properties [WPF], FocusVisualStyle
- FocusVisualStyle property [WPF]
ms.assetid: 363de99e-8ecc-438c-ac4a-f9147432ebd6
ms.openlocfilehash: c4b379d3c57b6d0ae29952c23a35d7cc2cdf7f96
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57366593"
---
# <a name="how-to-apply-a-focusvisualstyle-to-a-control"></a>Procédure : Appliquer un FocusVisualStyle à un contrôle
Cet exemple vous montre comment créer un style de focus visuel dans les ressources et appliquer le style à un contrôle, à l’aide de la <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> propriété.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit un style qui crée une composition de contrôle supplémentaire qui s’applique uniquement lorsque ce contrôle est clavier actif dans le [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)]. Cela s’effectue en définissant un style avec une <xref:System.Windows.Controls.ControlTemplate>, puis de référencer ce style en tant que ressource lors de la définition du <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> propriété.  
  
 Un rectangle externe ressemblant à une bordure est placé en dehors de la zone rectangulaire. À défaut de modification, le dimensionnement du style utilise le <xref:System.Windows.FrameworkElement.ActualHeight%2A> et <xref:System.Windows.FrameworkElement.ActualWidth%2A> du contrôle rectangulaire où le style de focus visuel est appliqué. Cet exemple définit des valeurs négatives pour le <xref:System.Windows.FrameworkElement.Margin%2A> pour rendre la bordure apparaissent légèrement en dehors du contrôle ayant le focus.  
  
 [!code-xaml[FEFocusVisualStyle#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FEFocusVisualStyle/CS/page1.xaml#xaml)]  
  
 Un <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> est additif pour tout style de modèle de contrôle qui est fourni à partir d’un style explicite ou un style de thème ; le style principal pour un contrôle peut toujours être créé à l’aide un <xref:System.Windows.Controls.ControlTemplate> et en définissant ce style sur la <xref:System.Windows.FrameworkElement.Style%2A> propriété.  
  
 Le focus de styles visuels doivent être utilisés de manière cohérente entre un thème ou une interface utilisateur, au lieu d’utiliser une autre pour chaque élément pouvant être actif. Pour plus d’informations, consultez [focus dans les contrôles et FocusVisualStyle](styling-for-focus-in-controls-and-focusvisualstyle.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A>
- [Application d’un style et création de modèles](../controls/styling-and-templating.md)
- [FocusVisualStyle et application d'un style au focus dans les contrôles](styling-for-focus-in-controls-and-focusvisualstyle.md)
