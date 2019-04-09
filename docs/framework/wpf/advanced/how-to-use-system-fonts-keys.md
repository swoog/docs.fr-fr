---
title: 'Procédure : Utiliser des clés de polices système'
ms.date: 03/30/2017
helpviewer_keywords:
- resource keys [WPF], SystemFonts class
ms.assetid: 036ebea7-5677-4f60-8ba4-56c9f9d9b8bd
ms.openlocfilehash: e924f4c14d98380d9f4c0defe27d9f98c3293114
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59148926"
---
# <a name="how-to-use-system-fonts-keys"></a>Procédure : Utiliser des clés de polices système
Les ressources système exposent plusieurs métriques système en tant que ressources pour aider les développeurs à créer des visuels cohérents avec les paramètres système. <xref:System.Windows.SystemFonts> est une classe qui contient les valeurs de police système et les ressources de police système liées aux valeurs, par exemple, <xref:System.Windows.SystemFonts.CaptionFontFamily%2A> et <xref:System.Windows.SystemFonts.CaptionFontFamilyKey%2A>.  
  
 Les métriques de police système peuvent être utilisées en tant que ressources statiques ou dynamiques. Utilisez une ressource dynamique si vous souhaitez que les métriques de police soient mises à jour automatiquement pendant que l’application s’exécute ; sinon, utilisez une ressource statique.  
  
> [!NOTE]
>  Ressources dynamiques ont le mot clé *clé* ajouté au nom de propriété.  
  
 L’exemple suivant montre comment accéder à des ressources dynamiques de police système et comment les utiliser pour personnaliser un bouton ou lui appliquer un style. Cela [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] exemple crée un style de bouton qui assigne <xref:System.Windows.SystemFonts> valeurs à un bouton.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[SystemRes_snip#FontDynamicResources](~/samples/snippets/csharp/VS_Snippets_Wpf/SystemRes_snip/CSharp/MyApp.xaml#fontdynamicresources)]  
  
## <a name="see-also"></a>Voir aussi

- [Peindre une zone avec un pinceau système](../graphics-multimedia/how-to-paint-an-area-with-a-system-brush.md)
- [Utiliser SystemParameters](how-to-use-systemparameters.md)
- [Utiliser SystemFonts](how-to-use-systemfonts.md)
