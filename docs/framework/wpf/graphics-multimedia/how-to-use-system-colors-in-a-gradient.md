---
title: 'Procédure : Utiliser des couleurs système dans un dégradé'
ms.date: 03/30/2017
helpviewer_keywords:
- gradients [WPF], system colors in
- system colors in gradients [WPF]
ms.assetid: 11942e7e-6300-4b50-8ed1-f50e8d20e7d2
ms.openlocfilehash: 44dfd30dc8d21e638855a383f1c9360a61ce81f9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54726414"
---
# <a name="how-to-use-system-colors-in-a-gradient"></a>Procédure : Utiliser des couleurs système dans un dégradé
Pour utiliser une couleur système dans un dégradé, vous utilisez le  *\<SystemColor >* couleur et  *\<SystemColor >* ColorKey de propriétés statiques de la <xref:System.Windows.SystemColors> classe pour obtenir une référence à la couleur, où  *\<SystemColor >* est le nom de la couleur système souhaitée. Utilisez le  *\<SystemColor >* propriétés ColorKey lorsque vous souhaitez créer une référence dynamique qui met à jour automatiquement en tant que les modifications de thème du système. Sinon, utilisez le  *\<SystemColor >* propriétés de couleur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise des ressources de couleurs système dynamiques pour créer un dégradé.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMDynamicSystemColorGradientExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/DynamicSystemColorExample.xaml#graphicsmmdynamicsystemcolorgradientexamplewholepage)]  
  
 L’exemple suivant utilise des ressources de couleurs système statiques pour créer un dégradé.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMStaticSystemColorGradientExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/StaticSystemColorExample.xaml#graphicsmmstaticsystemcolorgradientexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.SystemColors>
- [Peindre une zone avec un pinceau système](../../../../docs/framework/wpf/graphics-multimedia/how-to-paint-an-area-with-a-system-brush.md)
- [Vue d’ensemble de la peinture avec des couleurs unies ou des dégradés](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)
