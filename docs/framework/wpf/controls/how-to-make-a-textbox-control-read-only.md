---
title: 'Comment : mettre un contrôle TextBox en lecture seule'
ms.date: 03/30/2017
helpviewer_keywords:
- read-only TextBox controls [WPF]
- TextBox control read-only
ms.assetid: e707ec59-8b22-473e-b77c-3060a237517a
ms.openlocfilehash: 3ba93cae5977f3c8c76f3bfa9f5732d3f0736af7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33554539"
---
# <a name="how-to-make-a-textbox-control-read-only"></a>Comment : mettre un contrôle TextBox en lecture seule
Cet exemple montre comment configurer un <xref:System.Windows.Controls.TextBox> contrôle de n’autoriser l’entrée d’utilisateur ou la modification.  
  
## <a name="example"></a>Exemple  
 Pour empêcher les utilisateurs de modifier le contenu d’un <xref:System.Windows.Controls.TextBox> , affectez la <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribut **true**.  
  
 [!code-xaml[TextBox_MiscCode#_ReadOnlyTextBoxXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_readonlytextboxxaml)]  
  
 Le <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribut affecte uniquement l’entrée d’utilisateur ; il n’affecte pas le texte dans le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] description d’un <xref:System.Windows.Controls.TextBox> contrôle, ou le texte défini par programme via le <xref:System.Windows.Controls.TextBox.Text%2A> propriété.  
  
 La valeur par défaut <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> est **false**.  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble de TextBox](../../../../docs/framework/wpf/controls/textbox-overview.md)  
 [Vue d’ensemble de RichTextBox](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
