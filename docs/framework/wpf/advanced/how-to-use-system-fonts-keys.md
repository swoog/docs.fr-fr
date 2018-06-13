---
title: Guide pratique pour utiliser des clés de polices système
ms.date: 03/30/2017
helpviewer_keywords:
- resource keys [WPF], SystemFonts class
ms.assetid: 036ebea7-5677-4f60-8ba4-56c9f9d9b8bd
ms.openlocfilehash: c68f197daebd7423aa4ad2e7fdfb6e7f89c74ed0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33544425"
---
# <a name="how-to-use-system-fonts-keys"></a>Guide pratique pour utiliser des clés de polices système
Les ressources système exposent plusieurs métriques système en tant que ressources pour aider les développeurs à créer des visuels cohérents avec les paramètres système. <xref:System.Windows.SystemFonts> est une classe qui contient des valeurs de police système et des ressources de police système liées aux valeurs, par exemple, <xref:System.Windows.SystemFonts.CaptionFontFamily%2A> et <xref:System.Windows.SystemFonts.CaptionFontFamilyKey%2A>.  
  
 Les métriques de police système peuvent être utilisées en tant que ressources statiques ou dynamiques. Utilisez une ressource dynamique si vous souhaitez que les métriques de police soient mises à jour automatiquement pendant que l’application s’exécute ; sinon, utilisez une ressource statique.  
  
> [!NOTE]
>  Ressources dynamiques ont le mot clé *clé* ajouté au nom de propriété.  
  
 L’exemple suivant montre comment accéder à des ressources dynamiques de police système et comment les utiliser pour personnaliser un bouton ou lui appliquer un style. Cela [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] exemple crée un style de bouton qui assigne <xref:System.Windows.SystemFonts> valeurs à un bouton.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[SystemRes_snip#FontDynamicResources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SystemRes_snip/CSharp/MyApp.xaml#fontdynamicresources)]  
  
## <a name="see-also"></a>Voir aussi  
 [Peindre une zone avec un pinceau système](../../../../docs/framework/wpf/graphics-multimedia/how-to-paint-an-area-with-a-system-brush.md)  
 [Utiliser SystemParameters](../../../../docs/framework/wpf/advanced/how-to-use-systemparameters.md)  
 [Utiliser des SystemFonts](../../../../docs/framework/wpf/advanced/how-to-use-systemfonts.md)
