---
title: 'Procédure : Récupérer une sélection de texte'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [WPF], retrieving
- TextBox control [WPF], retrieving text
- retrieving text [WPF]
ms.assetid: d5793172-1e11-4a39-9be0-73f336ed858d
ms.openlocfilehash: b7f0b9ee02a7ace717787fc8eeb6e15649829a49
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770784"
---
# <a name="how-to-retrieve-a-text-selection"></a>Procédure : Récupérer une sélection de texte
Cet exemple montre une manière d’utiliser le <xref:System.Windows.Controls.TextBox.SelectedText%2A> propriété à récupérer le texte que l’utilisateur a sélectionné dans un <xref:System.Windows.Controls.TextBox> contrôle.  
  
## <a name="example"></a>Exemple  
 Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemple illustre la définition d’un <xref:System.Windows.Controls.TextBox> contrôle contenant du texte à sélectionner, et un <xref:System.Windows.Controls.Button> contrôle avec un <xref:System.Windows.Controls.Button.OnClick%2A> (méthode).  
  
 Dans cet exemple, un bouton avec associé à un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements est utilisé pour récupérer la sélection de texte. Lorsque l’utilisateur clique sur le bouton, le <xref:System.Windows.Controls.Button.OnClick%2A> méthode copie le texte sélectionné dans la zone de texte dans une chaîne. Circonstances particulières auxquelles la sélection de texte est récupérée (en cliquant sur un bouton), ainsi que l’action effectuée avec cette sélection (copie la sélection de texte vers une chaîne), peut facilement être modifié pour prendre en charge un large éventail de scénarios.  
  
 [!code-xaml[TextBox_MiscCode#_TextBoxSelectTextXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_textboxselecttextxaml)]  
  
## <a name="example"></a>Exemple  
 Ce qui suit C# exemple illustre un <xref:System.Windows.Controls.Button.OnClick%2A> Gestionnaire d’événements pour le bouton défini dans le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] pour cet exemple.  
  
 [!code-csharp[TextBox_MiscCode#_SelectText](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_selecttext)]
 [!code-vb[TextBox_MiscCode#_SelectText](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_MiscCode/VisualBasic/Window1.xaml.vb#_selecttext)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
