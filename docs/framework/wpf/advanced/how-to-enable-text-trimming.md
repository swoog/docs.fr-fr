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
# <a name="how-to-enable-text-trimming"></a><span data-ttu-id="a99dd-102">Procédure : Activer la suppression de texte</span><span class="sxs-lookup"><span data-stu-id="a99dd-102">How to: Enable Text Trimming</span></span>

<span data-ttu-id="a99dd-103">Cet exemple illustre l’utilisation et les effets des valeurs disponibles dans le <xref:System.Windows.TextTrimming> énumération.</span><span class="sxs-lookup"><span data-stu-id="a99dd-103">This example demonstrates the usage and effects of the values available in the <xref:System.Windows.TextTrimming> enumeration.</span></span>

## <a name="example"></a><span data-ttu-id="a99dd-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a99dd-104">Example</span></span>

<span data-ttu-id="a99dd-105">L’exemple suivant définit un <xref:System.Windows.Controls.TextBlock> élément avec la <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> ensemble d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a99dd-105">The following example defines a <xref:System.Windows.Controls.TextBlock> element with the <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> attribute set.</span></span>

[!code-xaml[TextTrimmingSnippets#_TextTrimmingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml#_texttrimmingxaml)]

<span data-ttu-id="a99dd-106">Définissant le correspondantes <xref:System.Windows.TextTrimming> propriété dans le code est illustrée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a99dd-106">Setting the corresponding <xref:System.Windows.TextTrimming> property in code is demonstrated below.</span></span>

[!code-csharp[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml.cs#_texttrimmingsettexttrimming)]
[!code-vb[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextTrimmingSnippets/VisualBasic/Window1.xaml.vb#_texttrimmingsettexttrimming)]

<span data-ttu-id="a99dd-107">Il existe actuellement trois options pour supprimer du texte : **CharacterEllipsis**, **WordEllipsis**, et **aucun**.</span><span class="sxs-lookup"><span data-stu-id="a99dd-107">There are currently three options for trimming text: **CharacterEllipsis**, **WordEllipsis**, and **None**.</span></span>

<span data-ttu-id="a99dd-108">Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **CharacterEllipsis**, texte est rogné et reprend avec des points de suspension au niveau du caractère le plus proche de la bordure de la suppression.</span><span class="sxs-lookup"><span data-stu-id="a99dd-108">When <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> is set to **CharacterEllipsis**, text is trimmed and continued with an ellipsis at the character closest to the trimming edge.</span></span>  <span data-ttu-id="a99dd-109">Ce paramètre tend à rogner le texte pour qu’il s’adapte mieux aux limites de la suppression, mais il peut provoquer la suppression partielle de certains mots.</span><span class="sxs-lookup"><span data-stu-id="a99dd-109">This setting tends to trim text to fit more closely to the trimming boundary, but may result in words being partially trimmed.</span></span>  <span data-ttu-id="a99dd-110">La figure suivante montre l’effet de ce paramètre sur un <xref:System.Windows.Controls.TextBlock> similaire à celui défini ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a99dd-110">The following figure shows the effect of this setting on a <xref:System.Windows.Controls.TextBlock> similar to the one defined above.</span></span>

<span data-ttu-id="a99dd-111">![Exemple : TextTrimming.CharacterEllipsis](./media/texttrimming-character.png "TextTrimming_Character")</span><span class="sxs-lookup"><span data-stu-id="a99dd-111">![Example: TextTrimming.CharacterEllipsis](./media/texttrimming-character.png "TextTrimming_Character")</span></span>

<span data-ttu-id="a99dd-112">Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **WordEllipsis**, texte est rogné et reprend avec des points de suspension à la fin du premier mot complet le plus proche de la bordure de la suppression.</span><span class="sxs-lookup"><span data-stu-id="a99dd-112">When <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> is set to **WordEllipsis**, text is trimmed and continued with an ellipsis at the end of the first full word closest to the trimming edge.</span></span>  <span data-ttu-id="a99dd-113">Ce paramètre n’affichera pas de mots partiellement rognés, mais ne tend ne pas à rogner le texte avec aussi près que le **CharacterEllipsis** paramètre.</span><span class="sxs-lookup"><span data-stu-id="a99dd-113">This setting will not show partially trimmed words, but tends not to trim text as closely to the trimming edge as the **CharacterEllipsis** setting.</span></span>  <span data-ttu-id="a99dd-114">La figure suivante montre l’effet de ce paramètre sur le <xref:System.Windows.Controls.TextBlock> définie ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a99dd-114">The following figure shows the effect of this setting on the <xref:System.Windows.Controls.TextBlock> defined above.</span></span>

<span data-ttu-id="a99dd-115">![Exemple : TextTrimming.WordEllipsis](./media/texttrimming-word.png "TextTrimming_Word")</span><span class="sxs-lookup"><span data-stu-id="a99dd-115">![Example: TextTrimming.WordEllipsis](./media/texttrimming-word.png "TextTrimming_Word")</span></span>

<span data-ttu-id="a99dd-116">Lorsque <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> a la valeur **aucun**, aucune suppression de texte est effectuée.</span><span class="sxs-lookup"><span data-stu-id="a99dd-116">When <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> is set to **None**, no text trimming is performed.</span></span>  <span data-ttu-id="a99dd-117">Dans ce cas, le texte est simplement rogné à la limite du conteneur de texte parent.</span><span class="sxs-lookup"><span data-stu-id="a99dd-117">In this case, text is simply cropped to the boundary of the parent text container.</span></span>  <span data-ttu-id="a99dd-118">La figure suivante montre l’effet de ce paramètre sur un <xref:System.Windows.Controls.TextBlock> similaire à celui défini ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a99dd-118">The following figure shows the effect of this setting on a <xref:System.Windows.Controls.TextBlock> similar to the one defined above.</span></span>

<span data-ttu-id="a99dd-119">![Exemple : TextTrimming.None](./media/texttrimming-none.png "TextTrimming_None")</span><span class="sxs-lookup"><span data-stu-id="a99dd-119">![Example: TextTrimming.None](./media/texttrimming-none.png "TextTrimming_None")</span></span>
