---
title: 'Procédure : Créer un contrôle TextBox multiligne'
ms.date: 03/30/2017
helpviewer_keywords:
- TextBox control [WPF], multiple lines of text
ms.assetid: 05914a93-d0ea-4a9a-b693-09df7d4e2ac2
ms.openlocfilehash: ca1b499b2acdfd9fd2ff0f57f2b0c07d7da10789
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517823"
---
# <a name="how-to-create-a-multiline-textbox-control"></a>Procédure : Créer un contrôle TextBox multiligne
Cet exemple montre comment utiliser [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] pour définir un <xref:System.Windows.Controls.TextBox> contrôle s’étend automatiquement pour s’adapter à plusieurs lignes de texte.  
  
## <a name="example"></a>Exemple  
 Définissant le <xref:System.Windows.Controls.TextBox.TextWrapping%2A> attribut **encapsuler** amène le texte entré à la ligne vers une nouvelle ligne lorsque le bord de la <xref:System.Windows.Controls.TextBox> contrôle est atteint, agrandissant automatiquement le <xref:System.Windows.Controls.TextBox> contrôle pour faire de la place pour une nouvelle ligne, si nécessaire.  
  
 Définition de la <xref:System.Windows.Controls.Primitives.TextBoxBase.AcceptsReturn%2A> attribut **true** provoque une nouvelle ligne à insérer lorsque la touche retour est enfoncée, développer une fois encore automatiquement le <xref:System.Windows.Controls.TextBox> à faire de la place pour une nouvelle ligne, si nécessaire.  
  
 Le <xref:System.Windows.Controls.Primitives.TextBoxBase.VerticalScrollBarVisibility%2A> attribut ajoute une barre de défilement à la <xref:System.Windows.Controls.TextBox>, de sorte que le contenu de la <xref:System.Windows.Controls.TextBox> puisse être défilé si le <xref:System.Windows.Controls.TextBox> s’étend au-delà de la taille du cadre ou de la fenêtre qui l’entoure.  
  
 [!code-xaml[TextBox_MiscCode#_MultilineTextBoxXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_multilinetextboxxaml)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.TextWrapping>
- [Vue d’ensemble de TextBox](../../../../docs/framework/wpf/controls/textbox-overview.md)
- [Vue d’ensemble de RichTextBox](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
