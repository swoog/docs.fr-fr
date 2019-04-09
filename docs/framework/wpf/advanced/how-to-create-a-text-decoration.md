---
title: 'Procédure : Créer une décoration de texte'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [WPF], baseline
- text [WPF], decorations
- fonts [WPF], underline
- fonts [WPF], overline
- strikethrough type [WPF]
- fonts [WPF], strikethrough
- overline type [WPF]
- underline type [WPF]
- typography [WPF], text decorations
- baseline type [WPF]
ms.assetid: cf3cb4e7-782a-4be7-b2d4-e0935e21e4e0
ms.openlocfilehash: d586eef8d1308070da38a0a54c63c3ba64d30c8b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59133833"
---
# <a name="how-to-create-a-text-decoration"></a>Procédure : Créer une décoration de texte
Un <xref:System.Windows.TextDecoration> objet est un ornement visuel que vous pouvez ajouter au texte. Il existe quatre types de décorations de texte : souligné, ligne de base, barré et surligné. L’exemple suivant montre les emplacements des ornements de texte par rapport au texte.  
  
 ![Diagramme des types de décoration de texte](./media/how-to-create-a-text-decoration/text-decoration-types.gif)  
  
 Pour ajouter une décoration de texte au texte, créez un <xref:System.Windows.TextDecoration> de l’objet et modifiez ses propriétés. Utilisez le <xref:System.Windows.TextDecoration.Location%2A> propriété pour spécifier où la décoration de texte s’affiche, comme souligné. Utilisez le <xref:System.Windows.TextDecoration.Pen%2A> propriété pour spécifier l’apparence de la décoration de texte, tel qu’un remplissage uni ou la couleur de dégradé. Si vous ne spécifiez pas une valeur pour le <xref:System.Windows.TextDecoration.Pen%2A> propriété, les valeurs par défaut des ornements à la même couleur que le texte. Une fois que vous avez défini un <xref:System.Windows.TextDecoration> de l’objet, ajoutez-la à la <xref:System.Windows.TextDecorations> collection de l’objet de texte souhaité.  
  
 L’exemple suivant montre une décoration de texte qui a été mise en forme avec un pinceau dégradé linéaire et un stylet en pointillés.  
  
 ![Ornement de texte avec souligné dégradé linéaire](./media/how-to-create-a-text-decoration/text-decoration-gradient.png)  
  
 Le <xref:System.Windows.Documents.Hyperlink> objet est un élément de contenu de flux inline qui permet d’héberger des liens hypertexte dans le contenu de flux. Par défaut, <xref:System.Windows.Documents.Hyperlink> utilise un <xref:System.Windows.TextDecoration> objet pour afficher un trait de soulignement. <xref:System.Windows.TextDecoration> les objets peuvent être des performances, en particulier si vous disposez de nombreuses <xref:System.Windows.Documents.Hyperlink> objets. Si vous utilisez beaucoup de <xref:System.Windows.Documents.Hyperlink> éléments, vous souhaiterez afficher un soulignement uniquement lors du déclenchement d’un événement, tel que le <xref:System.Windows.ContentElement.MouseEnter> événement.  
  
 Dans l’exemple suivant, le trait de soulignement pour le lien « Mon MSN » est dynamique, il s’affiche uniquement quand le <xref:System.Windows.ContentElement.MouseEnter> est déclenché.  
  
 ![Liens hypertexte affichant TextDecorations](./media/how-to-create-a-text-decoration/text-decorations-hyperlinks.png)  
   
 Pour plus d’informations, consultez [Spécifier si un lien hypertexte est souligné ou non](how-to-specify-whether-a-hyperlink-is-underlined.md).  
  
## <a name="example"></a>Exemple  
 Dans l’exemple de code suivant, une décoration de texte souligné utilise la valeur de police par défaut.  
  
 [!code-csharp[TextDecorationSnippets#TextDecorationSnippets1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml.cs#textdecorationsnippets1)]
 [!code-vb[TextDecorationSnippets#TextDecorationSnippets1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextDecorationSnippets/visualbasic/window1.xaml.vb#textdecorationsnippets1)]
 [!code-xaml[TextDecorationSnippets#TextDecorationSnippets1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml#textdecorationsnippets1)]  
  
 Dans l’exemple de code suivant, une décoration de texte souligné est créée avec un pinceau de couleur unie pour le stylet.  
  
 [!code-csharp[TextDecorationSnippets#TextDecorationSnippets2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml.cs#textdecorationsnippets2)]
 [!code-vb[TextDecorationSnippets#TextDecorationSnippets2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextDecorationSnippets/visualbasic/window1.xaml.vb#textdecorationsnippets2)]
 [!code-xaml[TextDecorationSnippets#TextDecorationSnippets2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml#textdecorationsnippets2)]  
  
 Dans l’exemple de code suivant, une décoration de texte souligné est créée avec un pinceau dégradé linéaire pour le stylet en pointillés.  
  
 [!code-csharp[TextDecorationSnippets#TextDecorationSnippets3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml.cs#textdecorationsnippets3)]
 [!code-vb[TextDecorationSnippets#TextDecorationSnippets3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextDecorationSnippets/visualbasic/window1.xaml.vb#textdecorationsnippets3)]
 [!code-xaml[TextDecorationSnippets#TextDecorationSnippets3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextDecorationSnippets/CSharp/Window1.xaml#textdecorationsnippets3)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.TextDecoration>
- <xref:System.Windows.Documents.Hyperlink>
- [Spécifier si un lien hypertexte est souligné ou non](how-to-specify-whether-a-hyperlink-is-underlined.md)
