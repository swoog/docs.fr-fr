---
title: 'Comment : activer la suppression de texte'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [WPF], trimming
- documents [WPF], trimmng text
- trimmng text [WPF]
ms.assetid: dd8c9191-d2be-45fd-9fb4-3c75b65578c5
ms.openlocfilehash: 97bc88b298500892fcc7d26e61f8052a05d9e593
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33543538"
---
# <a name="how-to-enable-text-trimming"></a>Comment : activer la suppression de texte
Cet exemple illustre l’utilisation et les effets des valeurs disponibles dans le <xref:System.Windows.TextTrimming> énumération.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit un <xref:System.Windows.Controls.TextBlock> élément avec la <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> ensemble d’attributs.  
  
 [!code-xaml[TextTrimmingSnippets#_TextTrimmingXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml#_texttrimmingxaml)]  
  
## <a name="example"></a>Exemple  
 Paramètre correspondant <xref:System.Windows.TextTrimming> propriété dans le code est illustrée ci-dessous.  
  
 [!code-csharp[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml.cs#_texttrimmingsettexttrimming)]
 [!code-vb[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextTrimmingSnippets/VisualBasic/Window1.xaml.vb#_texttrimmingsettexttrimming)]  
  
 Il existe actuellement trois options pour le texte de la suppression : **CharacterEllipsis**, **WordEllipsis**, et **aucun**.  
  
 Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **CharacterEllipsis**, texte est tronqué et poursuivi avec les points de suspension du caractère le plus proche de la bordure de la suppression.  Ce paramètre tend à rogner le texte pour qu’il s’adapte mieux aux limites de la suppression, mais il peut provoquer la suppression partielle de certains mots.  L’illustration suivante montre l’effet de ce paramètre sur un <xref:System.Windows.Controls.TextBlock> similaire à celui défini ci-dessus.  
  
 ![Exemple : TextTrimming.CharacterEllipsis](../../../../docs/framework/wpf/advanced/media/texttrimming-character.png "TextTrimming_Character")  
  
 Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **WordEllipsis**, texte est tronqué et poursuivi avec les points de suspension à la fin du premier mot entier le plus proche de la bordure de la suppression.  Ce paramètre n’affiche pas les mots partiellement ajustées, mais ne tend ne pas à rogner le texte avec autant que la **CharacterEllipsis** paramètre.  L’illustration suivante montre l’effet de ce paramètre sur le <xref:System.Windows.Controls.TextBlock> défini ci-dessus.  
  
 ![Exemple : TextTrimming.WordEllipsis](../../../../docs/framework/wpf/advanced/media/texttrimming-word.png "TextTrimming_Word")  
  
 Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **aucun**, aucune suppression de texte n’est effectuée.  Dans ce cas, le texte est simplement rogné à la limite du conteneur de texte parent.  L’illustration suivante montre l’effet de ce paramètre sur un <xref:System.Windows.Controls.TextBlock> similaire à celui défini ci-dessus.  
  
 ![Exemple : TextTrimming.None](../../../../docs/framework/wpf/advanced/media/texttrimming-none.png "TextTrimming_None")
