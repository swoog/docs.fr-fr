---
title: 'Procédure : Activer la suppression de texte'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [WPF], trimming
- documents [WPF], trimming text
- trimming text [WPF]
ms.assetid: dd8c9191-d2be-45fd-9fb4-3c75b65578c5
ms.openlocfilehash: 25fff566868e792004a915fee195485c4a1f385f
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57474139"
---
# <a name="how-to-enable-text-trimming"></a>Procédure : Activer la suppression de texte

Cet exemple illustre l’utilisation et les effets des valeurs disponibles dans le <xref:System.Windows.TextTrimming> énumération.

## <a name="example"></a>Exemple

L’exemple suivant définit un <xref:System.Windows.Controls.TextBlock> élément avec la <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> ensemble d’attributs.

[!code-xaml[TextTrimmingSnippets#_TextTrimmingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml#_texttrimmingxaml)]

Définissant le correspondantes <xref:System.Windows.TextTrimming> propriété dans le code est illustrée ci-dessous.

[!code-csharp[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml.cs#_texttrimmingsettexttrimming)]
[!code-vb[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextTrimmingSnippets/VisualBasic/Window1.xaml.vb#_texttrimmingsettexttrimming)]

Il existe actuellement trois options pour supprimer du texte : **CharacterEllipsis**, **WordEllipsis**, et **aucun**.

Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **CharacterEllipsis**, texte est rogné et reprend avec des points de suspension au niveau du caractère le plus proche de la bordure de la suppression.  Ce paramètre tend à rogner le texte pour qu’il s’adapte mieux aux limites de la suppression, mais il peut provoquer la suppression partielle de certains mots.  La figure suivante montre l’effet de ce paramètre sur un <xref:System.Windows.Controls.TextBlock> similaire à celui défini ci-dessus.

![Exemple : TextTrimming.CharacterEllipsis](./media/texttrimming-character.png "TextTrimming_Character")

Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **WordEllipsis**, texte est rogné et reprend avec des points de suspension à la fin du premier mot complet le plus proche de la bordure de la suppression.  Ce paramètre n’affichera pas de mots partiellement rognés, mais ne tend ne pas à rogner le texte avec aussi près que le **CharacterEllipsis** paramètre.  La figure suivante montre l’effet de ce paramètre sur le <xref:System.Windows.Controls.TextBlock> définie ci-dessus.

![Exemple : TextTrimming.WordEllipsis](./media/texttrimming-word.png "TextTrimming_Word")

Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **aucun**, aucune suppression de texte est effectuée.  Dans ce cas, le texte est simplement rogné à la limite du conteneur de texte parent.  La figure suivante montre l’effet de ce paramètre sur un <xref:System.Windows.Controls.TextBlock> similaire à celui défini ci-dessus.

![Exemple : TextTrimming.None](./media/texttrimming-none.png "TextTrimming_None")
