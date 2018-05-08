---
title: Vue d'ensemble de TextBlock
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], TextBlock
- TextBlock control [WPF]
ms.assetid: 24720bca-341a-4b03-8a6b-7a678023b10a
ms.openlocfilehash: c18ca64a25f436c3ed2ccd9e04316e25bab00a66
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="textblock-overview"></a>Vue d'ensemble de TextBlock
Le <xref:System.Windows.Controls.TextBlock> contrôle prend en charge le texte flexible [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] applications. Cet élément est principalement destiné aux [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] scénarios d’interface utilisateur de base qui ne nécessitent pas plus d’un paragraphe de texte. Il prend en charge un nombre de propriétés qui permettent un contrôle précis de présentation, telles que <xref:System.Windows.Controls.TextBlock.FontFamily%2A>, <xref:System.Windows.Controls.TextBlock.FontSize%2A>, <xref:System.Windows.Controls.TextBlock.FontWeight%2A>, <xref:System.Windows.Controls.TextBlock.TextEffects%2A>, et <xref:System.Windows.Controls.TextBlock.TextWrapping%2A>. Contenu de texte peut être ajouté à l’aide de la <xref:System.Windows.Controls.TextBlock.Text%2A> propriété. En cas d’utilisation dans du balisage [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], le contenu se trouvant entre la balise d’ouverture et la balise de fermeture est ajouté implicitement comme texte de l’élément.  
  
 A <xref:System.Windows.Controls.TextBlock> élément peut être instancié très simplement à l’aide de [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].  
  
 [!code-xaml[TextBlockSnip_XAML#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBlockSnip_XAML/CS/default.xaml#2)]  
  
 De même, l’utilisation de la <xref:System.Windows.Controls.TextBlock> élément dans le code est relativement simple.  
  
 [!code-csharp[TextBlockSnip#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBlockSnip/CSharp/TextBlockSnips.cs#1)]
 [!code-vb[TextBlockSnip#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextBlockSnip/VisualBasic/TextBlockSnips.vb#1)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.Label>
