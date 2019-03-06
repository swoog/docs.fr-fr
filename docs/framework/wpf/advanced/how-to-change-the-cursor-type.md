---
title: 'Procédure : Modifier le type de curseur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- mouse pointer [WPF], cursor type
- cursor (mouse pointer)
ms.assetid: 08c945a7-8ab0-4320-acf3-0b4955a344c2
ms.openlocfilehash: e62658f4c4249c93bd24dffd3878dd2ec2b75029
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57371142"
---
# <a name="how-to-change-the-cursor-type"></a>Procédure : Modifier le type de curseur
Cet exemple montre comment modifier le <xref:System.Windows.Input.Cursor> du pointeur de la souris pour un élément spécifique et pour l’application.  
  
 Cet exemple se compose d’un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] fichier et un fichier code-behind.  
  
## <a name="example"></a>Exemple  
 L’interface utilisateur est créé, qui se compose d’un <xref:System.Windows.Controls.ComboBox> pour sélectionner le texte souhaité <xref:System.Windows.Input.Cursor>, une paire de <xref:System.Windows.Controls.RadioButton> objets pour déterminer si la modification de curseur s’applique à un seul élément ou qu’il s’applique à l’application entière et un <xref:System.Windows.Controls.Border> qui est l’élément qui le nouveau curseur s’applique à.  
  
 [!code-xaml[cursors#ChangeCursorsXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/cursors/CSharp/Window1.xaml#changecursorsxaml)]  
  
 Le code-behind suivant crée un <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> Gestionnaire d’événements qui est appelé lorsque le type de curseur est modifié dans le <xref:System.Windows.Controls.ComboBox>.  Une instruction switch filtre sur le nom de curseur et définit la <xref:System.Windows.FrameworkElement.Cursor%2A> propriété sur le <xref:System.Windows.Controls.Border> qui se nomme *DisplayArea*.  
  
 Si la modification de curseur est définie sur « Application entière », le <xref:System.Windows.Input.Mouse.OverrideCursor%2A> propriété est définie sur le <xref:System.Windows.FrameworkElement.Cursor%2A> propriété de la <xref:System.Windows.Controls.Border> contrôle.  Cela force le curseur pour modifier pour toute l’application.  
  
 [!code-csharp[cursors#ChangeCursorsSample](~/samples/snippets/csharp/VS_Snippets_Wpf/cursors/CSharp/Window1.xaml.cs#changecursorssample)]
 [!code-vb[cursors#ChangeCursorsSample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/cursors/VisualBasic/Window1.xaml.vb#changecursorssample)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des entrées](input-overview.md)
