---
title: Guide pratique pour changer la propriété TextWrapping par programmation
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- documents [WPF], changing TextWrapping property programmatically
- TextWrapping property [WPF], changing programmatically
ms.assetid: 30d25554-4c82-4df9-a8d6-35683a4a13bb
ms.openlocfilehash: 1b0f039f0484d1d1e73c3c12af06e0faffbce1cb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-change-the-textwrapping-property-programmatically"></a>Guide pratique pour changer la propriété TextWrapping par programmation
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment modifier la valeur de la <xref:System.Windows.Controls.TextBlock.TextWrapping%2A> propriété par programmation.  
  
 Trois <xref:System.Windows.Controls.Button> éléments sont placés dans un <xref:System.Windows.Controls.StackPanel> élément [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]. Chaque <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événement pour un <xref:System.Windows.Controls.Button> correspond à un gestionnaire d’événements dans le code. Les gestionnaires d’événements utilisent le même nom que le <xref:System.Windows.Controls.TextBlock.TextWrapping%2A> valeur s’appliquera à `txt2` lorsque le bouton est activé. En outre, le texte de `txt1` (un <xref:System.Windows.Controls.TextBlock> ne pas indiqué dans le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]) est mis à jour pour refléter les modifications de la propriété.  
  
 [!code-xaml[TextWrapProperty#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextWrapProperty/VisualBasic/Pane1.xaml#1)]  
  
 [!code-csharp[TextWrapProperty#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextWrapProperty/CSharp/Window1.xaml.cs#2)]
 [!code-vb[TextWrapProperty#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextWrapProperty/VisualBasic/Pane1.xaml.vb#2)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.TextBlock.TextWrapping%2A>  
 <xref:System.Windows.TextWrapping>
