---
title: 'Procédure : Mettre un contrôle TextBox en lecture seule'
ms.date: 03/30/2017
helpviewer_keywords:
- read-only TextBox controls [WPF]
- TextBox control read-only
ms.assetid: e707ec59-8b22-473e-b77c-3060a237517a
ms.openlocfilehash: 7f24458eb98bd669d59f15c49d1d9e3beb6833b1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770940"
---
# <a name="how-to-make-a-textbox-control-read-only"></a>Procédure : Mettre un contrôle TextBox en lecture seule
Cet exemple montre comment configurer un <xref:System.Windows.Controls.TextBox> contrôle pour ne pas autoriser l’entrée d’utilisateur ou la modification.  
  
## <a name="example"></a>Exemple  
 Pour empêcher les utilisateurs de modifier le contenu d’un <xref:System.Windows.Controls.TextBox> , affectez la <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribut **true**.  
  
 [!code-xaml[TextBox_MiscCode#_ReadOnlyTextBoxXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml#_readonlytextboxxaml)]  
  
 Le <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> attribut affecte uniquement l’entrée d’utilisateur ; il n’affecte pas le texte dans le [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] description d’un <xref:System.Windows.Controls.TextBox> contrôle ou texte est définie par programmation via la <xref:System.Windows.Controls.TextBox.Text%2A> propriété.  
  
 La valeur par défaut <xref:System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly%2A> est **false**.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
