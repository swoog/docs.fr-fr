---
title: 'Procédure : Utiliser des clés de paramètres système'
ms.date: 03/30/2017
helpviewer_keywords:
- resource keys [WPF], SystemParameters class
- classes [WPF], SystemParameters
ms.assetid: 77571283-d16c-45bb-9f69-cafbbf72b21e
ms.openlocfilehash: 147f65b4bb214c12317309081c345251d7426cd6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59147329"
---
# <a name="how-to-use-system-parameters-keys"></a>Procédure : Utiliser des clés de paramètres système
Les ressources système exposent plusieurs métriques système en tant que ressources pour aider les développeurs à créer des visuels cohérents avec les paramètres système. <xref:System.Windows.SystemParameters> est une classe qui contient les valeurs de paramètre système et des clés de ressources liées aux valeurs, par exemple, <xref:System.Windows.SystemParameters.FullPrimaryScreenHeight%2A> et <xref:System.Windows.SystemParameters.FullPrimaryScreenHeightKey%2A>. Les métriques de paramètres système peuvent être utilisées en tant que ressources statiques ou dynamiques. Utilisez une ressource dynamique si vous souhaitez que les métriques de paramètres soient mises à jour automatiquement pendant que l’application s’exécute ; sinon, utilisez une ressource statique.  
  
> [!NOTE]
>  Ressources dynamiques ont le mot clé *clé* ajouté au nom de propriété.  
  
 L’exemple suivant montre comment accéder à des ressources dynamiques de paramètres système et comment les utiliser pour personnaliser un bouton ou lui appliquer un style. Cela [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] exemple dimensionne un bouton en assignant <xref:System.Windows.SystemParameters> valeurs à la largeur et la hauteur du bouton.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[SystemRes_snip#ParameterDynamicResources](~/samples/snippets/csharp/VS_Snippets_Wpf/SystemRes_snip/CSharp/MyApp.xaml#parameterdynamicresources)]  
  
## <a name="see-also"></a>Voir aussi

- [Peindre une zone avec un pinceau système](../graphics-multimedia/how-to-paint-an-area-with-a-system-brush.md)
- [Utiliser SystemFonts](how-to-use-systemfonts.md)
- [Utiliser SystemParameters](how-to-use-systemparameters.md)
