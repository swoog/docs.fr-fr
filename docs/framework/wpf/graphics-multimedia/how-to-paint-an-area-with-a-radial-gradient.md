---
title: 'Procédure : Peindre une zone avec un dégradé radial'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- brushes [WPF], painting with radial gradients
- radial gradients [WPF], painting with
- painting [WPF], with radial gradients
ms.assetid: b5d0fc8a-8986-4796-b003-a75b41a48928
ms.openlocfilehash: c3bcc11dea4b1f223f629415591ab03588881dde
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57379781"
---
# <a name="how-to-paint-an-area-with-a-radial-gradient"></a>Procédure : Peindre une zone avec un dégradé radial
Cet exemple montre comment utiliser le <xref:System.Windows.Media.RadialGradientBrush> classe pour peindre une zone avec un dégradé radial.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.RadialGradientBrush> pour peindre un rectangle avec un dégradé radial qui passe du jaune au rouge au bleu au citron vert.  
  
 [!code-csharp[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/RadialGradientBrushSnippet.cs#simpleradialgradientexamplewholepage)]
 [!code-vb[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/radialgradientbrushsnippet.vb#simpleradialgradientexamplewholepage)]
 [!code-xaml[BrushesIntroduction_snip#SimpleRadialGradientExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/RadialGradientBrushSnippet.xaml#simpleradialgradientexamplewholepage)]  
  
 L’illustration suivante montre le dégradé de l’exemple précédent. Le nom du dégradé ont été mis en surbrillance.  
  
 ![Points de dégradé dans un dégradé radial](./media/wcpsdk-graphicsmm-4gradientstops-rg.png "wcpsdk_graphicsmm_4gradientstops_rg")  
  
> [!NOTE]
>  Les exemples de cette rubrique utilisent le système de coordonnées par défaut pour la définition des points de contrôle. Le système de coordonnées par défaut est relatif à un rectangle englobant : 0 indique 0 % de la zone englobante, et 1 indique 100 % de la zone englobante. Vous pouvez modifier ce système de coordonnées en définissant le <xref:System.Windows.Media.GradientBrush.MappingMode%2A> valeur à la propriété <xref:System.Windows.Media.BrushMappingMode.Absolute>. Un système de coordonnées absolu n’est pas relatif à un rectangle englobant. Les valeurs sont interprétées directement dans l’espace local.  
  
 Pour plus <xref:System.Windows.Media.RadialGradientBrush> obtenir des exemples, consultez le [pinceaux, exemple](https://go.microsoft.com/fwlink/?LinkID=159973). Pour plus d’informations sur les dégradés et les autres types de pinceaux, consultez [peinture avec des couleurs unies et vue d’ensemble des dégradés](painting-with-solid-colors-and-gradients-overview.md).
