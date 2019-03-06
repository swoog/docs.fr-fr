---
title: 'Procédure : Utiliser un menu contextuel personnalisé avec un TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- context menus [WPF], custom
- menus [WPF], custom
- custom context menus [WPF]
- TextBox control [WPF], custom content menus
ms.assetid: 842d3cd5-6fa0-4be4-8d90-6c7466213b1c
ms.openlocfilehash: 805f5205a91f9b3da0c48c987f1f49f1d81892b7
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57358598"
---
# <a name="how-to-use-a-custom-context-menu-with-a-textbox"></a>Procédure : Utiliser un menu contextuel personnalisé avec un TextBox
Cet exemple montre comment définir et implémenter un menu contextuel personnalisé simple pour un <xref:System.Windows.Controls.TextBox>.  
  
## <a name="example"></a>Exemple  
 Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemple définit un <xref:System.Windows.Controls.TextBox> contrôle qui inclut un menu contextuel personnalisé.  
  
 Le menu contextuel est défini en utilisant un <xref:System.Windows.Controls.ContextMenu> élément.  Le menu contextuel elle-même se compose d’une série de <xref:System.Windows.Controls.MenuItem> éléments et <xref:System.Windows.Controls.Separator> éléments.  Chaque <xref:System.Windows.Controls.MenuItem> élément définit une commande dans le menu contextuel ; le <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> attribut définit le texte affiché pour la commande de menu et le <xref:System.Windows.Controls.MenuItem.Click> attribut spécifie une méthode de gestionnaire pour chaque élément de menu.  Le <xref:System.Windows.Controls.Separator> élément entraîne simplement une ligne de séparation rendus entre les éléments de menu précédents et suivants.  
  
 [!code-xaml[TextBox_ContextMenu#_TextBox_ContextMenuXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_ContextMenu/CSharp/Window1.xaml#_textbox_contextmenuxaml)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre le code d’implémentation pour la définition du menu contexte précédent, ainsi que le code qui active et désactive le menu contextuel.  Le <xref:System.Windows.Controls.ContextMenu.Opened> événement est utilisé pour activer ou désactiver certaines commandes selon l’état actuel de manière dynamique le <xref:System.Windows.Controls.TextBox>.  
  
 Pour restaurer le menu contextuel par défaut, utilisez le <xref:System.Windows.DependencyObject.ClearValue%2A> méthode pour effacer la valeur de la <xref:System.Windows.FrameworkElement.ContextMenu%2A> propriété.  Pour désactiver complètement le menu contextuel, définissez la <xref:System.Windows.FrameworkElement.ContextMenu%2A> propriété à une référence null (`Nothing` en Visual Basic).  
  
 [!code-csharp[TextBox_ContextMenu#_TextBox_ContextMenu](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_ContextMenu/CSharp/Window1.xaml.cs#_textbox_contextmenu)]
 [!code-vb[TextBox_ContextMenu#_TextBox_ContextMenu](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_ContextMenu/VisualBasic/Window1.xaml.vb#_textbox_contextmenu)]  
  
## <a name="see-also"></a>Voir aussi
- [Utiliser la vérification de l'orthographe avec un menu contextuel](how-to-use-spell-checking-with-a-context-menu.md)
- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
