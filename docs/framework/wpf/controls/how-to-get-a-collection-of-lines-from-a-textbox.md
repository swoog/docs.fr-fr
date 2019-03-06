---
title: "Procédure : Obtenir une collection de lignes à partir d'un TextBox"
ms.date: 03/30/2017
helpviewer_keywords:
- lines [WPF], getting collection of
- TextBox control [WPF], getting collection of lines
ms.assetid: a12f529d-b926-47f6-92bf-cad5f17b532a
ms.openlocfilehash: 1aa73e55a3fdfd658c6a337b598dff96244ace40
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57354191"
---
# <a name="how-to-get-a-collection-of-lines-from-a-textbox"></a>Procédure : Obtenir une collection de lignes à partir d'un TextBox
Cet exemple montre comment obtenir une collection de lignes de texte à partir d’un <xref:System.Windows.Controls.TextBox>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre une méthode simple qui prend un <xref:System.Windows.Controls.TextBox> comme argument et retourne un <xref:System.Collections.Specialized.StringCollection> contenant les lignes de texte dans le **zone de texte**.  Le <xref:System.Windows.Controls.TextBox.LineCount%2A> propriété est utilisée pour déterminer le nombre de lignes n’est actuellement dans le **zone de texte**et le <xref:System.Windows.Controls.TextBox.GetLineText%2A> méthode est ensuite utilisée pour extraire chaque ligne et l’ajouter à la collection de lignes.  
  
 [!code-csharp[TextBox_MiscCode#_TextBox_GetLines](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textbox_getlines)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de TextBox](textbox-overview.md)
- [Vue d’ensemble de RichTextBox](richtextbox-overview.md)
