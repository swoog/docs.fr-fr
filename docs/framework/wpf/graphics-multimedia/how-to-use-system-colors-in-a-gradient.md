---
title: 'Procédure : Utiliser des couleurs système dans un dégradé'
ms.date: 03/30/2017
helpviewer_keywords:
- gradients [WPF], system colors in
- system colors in gradients [WPF]
ms.assetid: 11942e7e-6300-4b50-8ed1-f50e8d20e7d2
ms.openlocfilehash: 55c99640907a0c372f8c7bbc50b9b45c9f15ef3c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769237"
---
# <a name="how-to-use-system-colors-in-a-gradient"></a>Procédure : Utiliser des couleurs système dans un dégradé
Pour utiliser une couleur système dans un dégradé, vous utilisez le  *\<SystemColor >* couleur et  *\<SystemColor >* ColorKey de propriétés statiques de la <xref:System.Windows.SystemColors> classe pour obtenir une référence à la couleur, où  *\<SystemColor >* est le nom de la couleur système souhaitée. Utilisez le  *\<SystemColor >* propriétés ColorKey lorsque vous souhaitez créer une référence dynamique qui met à jour automatiquement en tant que les modifications de thème du système. Sinon, utilisez le  *\<SystemColor >* propriétés de couleur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise des ressources de couleurs système dynamiques pour créer un dégradé.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMDynamicSystemColorGradientExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/DynamicSystemColorExample.xaml#graphicsmmdynamicsystemcolorgradientexamplewholepage)]  
  
 L’exemple suivant utilise des ressources de couleurs système statiques pour créer un dégradé.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMStaticSystemColorGradientExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/StaticSystemColorExample.xaml#graphicsmmstaticsystemcolorgradientexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.SystemColors>
- [Peindre une zone avec un pinceau système](how-to-paint-an-area-with-a-system-brush.md)
- [Vue d’ensemble de la peinture avec des couleurs unies ou des dégradés](painting-with-solid-colors-and-gradients-overview.md)
