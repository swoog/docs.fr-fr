---
title: 'Comment : manipuler des éléments de contenu de flux avec la propriété Blocks'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- documents [WPF], manipulating flow content elements through Blocks property
- flow content elements [WPF], manipulating through Blocks property
- properties [WPF], Blocks [WPF], manipulating flow content elements
- Blocks property [WPF], manipulating flow content elements
ms.assetid: aeda4ece-b979-4818-a093-ef938e908751
ms.openlocfilehash: 74710c4a6dd58cf2836cd7671a3e39401a5ea774
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33544548"
---
# <a name="how-to-manipulate-flow-content-elements-through-the-blocks-property"></a><span data-ttu-id="929f8-102">Comment : manipuler des éléments de contenu de flux avec la propriété Blocks</span><span class="sxs-lookup"><span data-stu-id="929f8-102">How to: Manipulate Flow Content Elements through the Blocks Property</span></span>
<span data-ttu-id="929f8-103">Ces exemples montrent quelques-unes des opérations plus courantes qui peuvent être effectuées sur les éléments de contenu de flux avec le **blocs** propriété.</span><span class="sxs-lookup"><span data-stu-id="929f8-103">These examples demonstrate some of the more common operations that can be performed on flow content elements through the **Blocks** property.</span></span> <span data-ttu-id="929f8-104">Cette propriété est utilisée pour ajouter et supprimer des éléments de <xref:System.Windows.Documents.BlockCollection>.</span><span class="sxs-lookup"><span data-stu-id="929f8-104">This property is used to add and remove items from <xref:System.Windows.Documents.BlockCollection>.</span></span> <span data-ttu-id="929f8-105">Éléments de contenu flux cette fonctionnalité une **blocs** propriété incluent :</span><span class="sxs-lookup"><span data-stu-id="929f8-105">Flow content elements that feature a **Blocks** property include:</span></span>  
  
-   <xref:System.Windows.Documents.Figure>  
  
-   <xref:System.Windows.Documents.Floater>  
  
-   <xref:System.Windows.Documents.ListItem>  
  
-   <xref:System.Windows.Documents.Section>  
  
-   <xref:System.Windows.Documents.TableCell>  
  
 <span data-ttu-id="929f8-106">Il arrive que ces exemples utilisent <xref:System.Windows.Documents.Section> en tant que flux de l’élément de contenu, mais ces techniques sont applicables à tous les éléments qui hébergent une collection d’éléments de contenu de flux.</span><span class="sxs-lookup"><span data-stu-id="929f8-106">These examples happen to use <xref:System.Windows.Documents.Section> as the flow content element, but these techniques are applicable to all elements that host a flow content element collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="929f8-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="929f8-107">Example</span></span>  
 <span data-ttu-id="929f8-108">L’exemple suivant crée un nouveau <xref:System.Windows.Documents.Section> , puis utilise le **ajouter** méthode pour ajouter un nouveau paragraphe à la **Section** contenu.</span><span class="sxs-lookup"><span data-stu-id="929f8-108">The following example creates a new <xref:System.Windows.Documents.Section> and then uses the **Add** method to add a new Paragraph to the **Section** contents.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksAdd](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksadd)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksAdd](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksadd)]  
  
## <a name="example"></a><span data-ttu-id="929f8-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="929f8-109">Example</span></span>  
 <span data-ttu-id="929f8-110">L’exemple suivant crée un nouveau <xref:System.Windows.Documents.Paragraph> élément et l’insère au début de la <xref:System.Windows.Documents.Section>.</span><span class="sxs-lookup"><span data-stu-id="929f8-110">The following example creates a new <xref:System.Windows.Documents.Paragraph> element and inserts it at the beginning of the <xref:System.Windows.Documents.Section>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksInsert](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksinsert)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksInsert](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksinsert)]  
  
## <a name="example"></a><span data-ttu-id="929f8-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="929f8-111">Example</span></span>  
 <span data-ttu-id="929f8-112">L’exemple suivant obtient le nombre de niveau supérieur <xref:System.Windows.Documents.Block> éléments contenus dans le <xref:System.Windows.Documents.Section>.</span><span class="sxs-lookup"><span data-stu-id="929f8-112">The following example gets the number of top-level <xref:System.Windows.Documents.Block> elements contained in the <xref:System.Windows.Documents.Section>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksCount](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblockscount)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksCount](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblockscount)]  
  
## <a name="example"></a><span data-ttu-id="929f8-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="929f8-113">Example</span></span>  
 <span data-ttu-id="929f8-114">L’exemple suivant supprime le dernier <xref:System.Windows.Documents.Block> élément dans le <xref:System.Windows.Documents.Section>.</span><span class="sxs-lookup"><span data-stu-id="929f8-114">The following example deletes the last <xref:System.Windows.Documents.Block> element in the <xref:System.Windows.Documents.Section>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksRemoveLast](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksremovelast)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksRemoveLast](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksremovelast)]  
  
## <a name="example"></a><span data-ttu-id="929f8-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="929f8-115">Example</span></span>  
 <span data-ttu-id="929f8-116">L’exemple suivant efface tout le contenu (<xref:System.Windows.Documents.Block> éléments) à partir de la <xref:System.Windows.Documents.Section>.</span><span class="sxs-lookup"><span data-stu-id="929f8-116">The following example clears all of the contents (<xref:System.Windows.Documents.Block> elements) from the <xref:System.Windows.Documents.Section>.</span></span>  
  
 [!code-csharp[FlowDocumentSnippets#_SectionBlocksClear](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentSnippets/CSharp/Window1.xaml.cs#_sectionblocksclear)]
 [!code-vb[FlowDocumentSnippets#_SectionBlocksClear](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentSnippets/visualbasic/window1.xaml.vb#_sectionblocksclear)]  
  
## <a name="see-also"></a><span data-ttu-id="929f8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="929f8-117">See Also</span></span>  
 <xref:System.Windows.Documents.BlockCollection>  
 <xref:System.Windows.Documents.InlineCollection>  
 <xref:System.Windows.Documents.ListItemCollection>  
 [<span data-ttu-id="929f8-118">Vue d’ensemble des documents dynamiques</span><span class="sxs-lookup"><span data-stu-id="929f8-118">Flow Document Overview</span></span>](../../../../docs/framework/wpf/advanced/flow-document-overview.md)  
 [<span data-ttu-id="929f8-119">Manipuler les groupes de lignes d’un tableau avec la propriété RowGroups</span><span class="sxs-lookup"><span data-stu-id="929f8-119">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](../../../../docs/framework/wpf/advanced/how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)  
 [<span data-ttu-id="929f8-120">Manipuler les colonnes d’un tableau avec la propriété Columns</span><span class="sxs-lookup"><span data-stu-id="929f8-120">Manipulate a Table's Columns through the Columns Property</span></span>](../../../../docs/framework/wpf/advanced/how-to-manipulate-table-columns-through-the-columns-property.md)  
 [<span data-ttu-id="929f8-121">Manipuler les groupes de lignes d’un tableau avec la propriété RowGroups</span><span class="sxs-lookup"><span data-stu-id="929f8-121">Manipulate a Table's Row Groups through the RowGroups Property</span></span>](../../../../docs/framework/wpf/advanced/how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
