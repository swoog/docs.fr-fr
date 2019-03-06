---
title: 'Procédure : Positionner le curseur au début ou à la fin du texte dans un contrôle TextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- positioning cursor [WPF]
- TextBox control [WPF], positioning cursor
- cursor [WPF], positioning
ms.assetid: c771a0b8-c6b4-4240-aecd-a21d0ba51a2e
ms.openlocfilehash: e4058518e4eb56e1cd9d5fdafd792d8f8d3b77ab
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57367841"
---
# <a name="how-to-position-the-cursor-at-the-beginning-or-end-of-text-in-a-textbox-control"></a>Procédure : Positionner le curseur au début ou à la fin du texte dans un contrôle TextBox
Cet exemple montre comment positionner le curseur au début ou à la fin du contenu texte d’un <xref:System.Windows.Controls.TextBox> contrôle.  
  
## <a name="example"></a>Exemple  
 Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] code décrit un <xref:System.Windows.Controls.TextBox> contrôler et lui assigne un nom.  
  
 [!code-xaml[TextBox_MiscCode#_MoveCursorXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_movecursorxaml)]  
  
## <a name="example"></a>Exemple  
 Pour positionner le curseur au début du contenu d’un <xref:System.Windows.Controls.TextBox> contrôler, appelez le <xref:System.Windows.Controls.TextBox.Select%2A> (méthode) et spécifiez la sélection de position de départ de 0 et une longueur de sélection 0.  
  
 [!code-csharp[TextBox_MiscCode#_CursorToStart](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_cursortostart)]
 [!code-vb[TextBox_MiscCode#_CursorToStart](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_cursortostart)]  
  
## <a name="example"></a>Exemple  
 Pour positionner le curseur à la fin du contenu d’un <xref:System.Windows.Controls.TextBox> contrôler, appelez le <xref:System.Windows.Controls.TextBox.Select%2A> (méthode) et spécifier la position de départ de sélection égale à la longueur du contenu texte et une longueur de sélection 0.  
  
 [!code-csharp[TextBox_MiscCode#_CursorToEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_cursortoend)]
 [!code-vb[TextBox_MiscCode#_CursorToEnd](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_cursortoend)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
