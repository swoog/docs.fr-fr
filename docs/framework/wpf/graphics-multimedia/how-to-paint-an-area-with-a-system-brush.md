---
title: 'Comment : peindre une zone avec un pinceau système'
ms.date: 03/30/2017
helpviewer_keywords:
- system brushes [WPF], painting with
- painting [WPF], with system brushes
- brushes [WPF], painting with system brushes [WPF]
ms.assetid: 5141a763-9235-42cb-a6bb-afc75513eac7
ms.openlocfilehash: f8a66ffc283016d65a17b33e98ce28fe4cd1c242
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33561145"
---
# <a name="how-to-paint-an-area-with-a-system-brush"></a>Comment : peindre une zone avec un pinceau système
Le <xref:System.Windows.SystemColors> classe fournit l’accès aux pinceaux système et couleurs, tel que <xref:System.Windows.SystemColors.ControlBrush%2A>, <xref:System.Windows.SystemColors.ControlBrushKey%2A>, et <xref:System.Windows.SystemColors.DesktopBrush%2A>. Un pinceau système est un <xref:System.Windows.Media.SolidColorBrush> objet qui peint une zone avec la couleur système spécifiée. Un pinceau système produit toujours un remplissage uni ; vous ne pouvez pas l’utiliser pour créer un dégradé.  
  
 Vous pouvez utiliser des pinceaux système comme ressource dynamique ou statique. Utilisez une ressource dynamique si vous souhaitez que le pinceau soit automatiquement mis à jour si l’utilisateur modifie le pinceau système alors que l’application est en cours d’exécution ; sinon, utilisez une ressource statique. La classe SystemColors contient diverses propriétés statiques qui suivent une convention d’affectation de noms stricte :  
  
-   *\<SystemColor>* Brush  
  
     Obtient une référence statique à un <xref:System.Windows.Media.SolidColorBrush> de la couleur système spécifié.  
  
-   *\<SystemColor>* BrushKey  
  
     Obtient une référence dynamique à un <xref:System.Windows.Media.SolidColorBrush> de la couleur système spécifié.  
  
-   *\<SystemColor>* Color  
  
     Obtient une référence statique à un <xref:System.Windows.Media.Color> structure de la couleur système spécifié.  
  
-   *\<SystemColor>* ColorKey  
  
     Obtient une référence dynamique à la <xref:System.Windows.Media.Color> structure de la couleur système spécifié.  
  
 Une couleur système est un <xref:System.Windows.Media.Color> structure peut être utilisé pour configurer un pinceau. Par exemple, vous pouvez créer un dégradé à l’aide de couleurs système en définissant le <xref:System.Windows.Media.GradientStop.Color%2A> propriétés d’un <xref:System.Windows.Media.LinearGradientBrush> de dégradé de l’objet avec les couleurs système. Pour obtenir un exemple, consultez [utiliser des couleurs système dans un dégradé](../../../../docs/framework/wpf/graphics-multimedia/how-to-use-system-colors-in-a-gradient.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise une référence de pinceau système dynamique pour définir l’arrière-plan d’un bouton.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMDynamicSystemColorDesktopBrushKeyExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/DynamicSystemBrushExample.xaml#graphicsmmdynamicsystemcolordesktopbrushkeyexamplewholepage)]  
  
 L’exemple suivant utilise une référence de pinceau système statique pour définir l’arrière-plan d’un bouton.  
  
 [!code-xaml[brushsamples_snip#GraphicsMMStaticSystemColorDesktopBrushExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/StaticSystemBrushExample.xaml#graphicsmmstaticsystemcolordesktopbrushexamplewholepage)]  
  
 Pour obtenir un exemple montrant comment utiliser une couleur système dans un dégradé, consultez [utiliser les couleurs système dans un dégradé](../../../../docs/framework/wpf/graphics-multimedia/how-to-use-system-colors-in-a-gradient.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Utiliser des couleurs système dans un dégradé](../../../../docs/framework/wpf/graphics-multimedia/how-to-use-system-colors-in-a-gradient.md)  
 [Vue d’ensemble de la peinture avec des couleurs unies ou des dégradés](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)
