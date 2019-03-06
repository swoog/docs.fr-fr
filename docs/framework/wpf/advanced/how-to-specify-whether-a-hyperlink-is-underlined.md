---
title: 'Procédure : Spécifier si un lien hypertexte est souligné ou non'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Hyperlink control type [WPF]
ms.assetid: 3996cfe6-1dac-4835-aeb3-c719ce9cfee5
ms.openlocfilehash: 9e8eb54d4710095a1aba052b16e49c528bd17c0e
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57371040"
---
# <a name="how-to-specify-whether-a-hyperlink-is-underlined"></a><span data-ttu-id="12442-102">Procédure : Spécifier si un lien hypertexte est souligné ou non</span><span class="sxs-lookup"><span data-stu-id="12442-102">How to: Specify Whether a Hyperlink is Underlined</span></span>
<span data-ttu-id="12442-103">Le <xref:System.Windows.Documents.Hyperlink> objet est un élément de contenu de flux inline qui permet d’héberger des liens hypertexte dans le contenu de flux.</span><span class="sxs-lookup"><span data-stu-id="12442-103">The <xref:System.Windows.Documents.Hyperlink> object is an inline-level flow content element that allows you to host hyperlinks within the flow content.</span></span> <span data-ttu-id="12442-104">Par défaut, <xref:System.Windows.Documents.Hyperlink> utilise un <xref:System.Windows.TextDecoration> objet pour afficher un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="12442-104">By default, <xref:System.Windows.Documents.Hyperlink> uses a <xref:System.Windows.TextDecoration> object to display an underline.</span></span> <span data-ttu-id="12442-105"><xref:System.Windows.TextDecoration> les objets peuvent être des performances, en particulier si vous disposez de nombreuses <xref:System.Windows.Documents.Hyperlink> objets.</span><span class="sxs-lookup"><span data-stu-id="12442-105"><xref:System.Windows.TextDecoration> objects can be performance intensive to instantiate, particularly if you have many <xref:System.Windows.Documents.Hyperlink> objects.</span></span> <span data-ttu-id="12442-106">Si vous utilisez beaucoup de <xref:System.Windows.Documents.Hyperlink> éléments, vous souhaiterez afficher un soulignement uniquement lors du déclenchement d’un événement, tel que le <xref:System.Windows.ContentElement.MouseEnter> événement.</span><span class="sxs-lookup"><span data-stu-id="12442-106">If you make extensive use of <xref:System.Windows.Documents.Hyperlink> elements, you may want to consider showing an underline only when triggering an event, such as the <xref:System.Windows.ContentElement.MouseEnter> event.</span></span>  
  
 <span data-ttu-id="12442-107">Dans l’exemple suivant, le trait de soulignement pour le lien « Mon MSN » est dynamique, il s’affiche uniquement quand le <xref:System.Windows.ContentElement.MouseEnter> est déclenché.</span><span class="sxs-lookup"><span data-stu-id="12442-107">In the following example, the underline for the "My MSN" link is dynamic—it only appears when the <xref:System.Windows.ContentElement.MouseEnter> event is triggered.</span></span>  
  
 <span data-ttu-id="12442-108">![Liens hypertexte affichant TextDecorations](./media/textdecoration03.png "TextDecoration03")</span><span class="sxs-lookup"><span data-stu-id="12442-108">![Hyperlinks displaying TextDecorations](./media/textdecoration03.png "TextDecoration03")</span></span>  
<span data-ttu-id="12442-109">Lien hypertexte est défini avec TextDecorations</span><span class="sxs-lookup"><span data-stu-id="12442-109">Hyperlinks defined with TextDecorations</span></span>  
  
## <a name="example"></a><span data-ttu-id="12442-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="12442-110">Example</span></span>  
 <span data-ttu-id="12442-111">L’exemple de balisage suivant montre un <xref:System.Windows.Documents.Hyperlink> défini avec et sans soulignement :</span><span class="sxs-lookup"><span data-stu-id="12442-111">The following markup sample shows a <xref:System.Windows.Documents.Hyperlink> defined with and without an underline:</span></span>  
  
 [!code-xaml[Performance#PerformanceSnippet11](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml#performancesnippet11)]  
  
 <span data-ttu-id="12442-112">L’exemple de code suivant montre comment créer un trait de soulignement pour le <xref:System.Windows.Documents.Hyperlink> sur le <xref:System.Windows.ContentElement.MouseEnter> événement et le supprimer sur le <xref:System.Windows.ContentElement.MouseLeave> événement.</span><span class="sxs-lookup"><span data-stu-id="12442-112">The following code sample shows how to create an underline for the <xref:System.Windows.Documents.Hyperlink> on the <xref:System.Windows.ContentElement.MouseEnter> event, and remove it on the <xref:System.Windows.ContentElement.MouseLeave> event.</span></span>  
  
 [!code-csharp[Performance#PerformanceSnippet15](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/Hyperlink.xaml.cs#performancesnippet15)]
 [!code-vb[Performance#PerformanceSnippet15](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Performance/visualbasic/hyperlink.xaml.vb#performancesnippet15)]  
  
## <a name="see-also"></a><span data-ttu-id="12442-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12442-113">See also</span></span>
- <xref:System.Windows.TextDecoration>
- <xref:System.Windows.Documents.Hyperlink>
- [<span data-ttu-id="12442-114">Optimisation des performances des applications WPF</span><span class="sxs-lookup"><span data-stu-id="12442-114">Optimizing WPF Application Performance</span></span>](optimizing-wpf-application-performance.md)
- [<span data-ttu-id="12442-115">Créer une décoration de texte</span><span class="sxs-lookup"><span data-stu-id="12442-115">Create a Text Decoration</span></span>](how-to-create-a-text-decoration.md)
