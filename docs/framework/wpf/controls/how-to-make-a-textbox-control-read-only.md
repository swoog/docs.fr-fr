---
title: 'Procédure : Mettre un contrôle TextBox en lecture seule'
ms.date: 03/30/2017
helpviewer_keywords:
- read-only TextBox controls [WPF]
- TextBox control read-only
ms.assetid: e707ec59-8b22-473e-b77c-3060a237517a
ms.openlocfilehash: 1e9d333f22099d9593e58b4087f185b2988215ce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517173"
---
# <a name="how-to-make-a-textbox-control-read-only"></a>Procédure : Mettre un contrôle TextBox en lecture seule
Cet exemple montre comment configurer un <xref:System.Windows.Controls.TextBox> contrôle pour ne pas autoriser l’entrée d’utilisateur ou la modification.  
  
## <a name="example"></a>Exemple  
 Pour empêcher les utilisateurs de modifier le contenu d’un <xref:System.Windows.Controls.TextBox> , affectez la <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribut **true**.  
  
 [!code-xaml[TextBox_MiscCode#_ReadOnlyTextBoxXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_readonlytextboxxaml)]  
  
 Le <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribut affecte uniquement l’entrée d’utilisateur ; il n’affecte pas le texte dans le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] description d’un <xref:System.Windows.Controls.TextBox> contrôle ou texte est définie par programmation via la <xref:System.Windows.Controls.TextBox.Text%2A> propriété.  
  
 La valeur par défaut <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> est **false**.  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de TextBox](../../../../docs/framework/wpf/controls/textbox-overview.md)
- [Vue d’ensemble de RichTextBox](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
