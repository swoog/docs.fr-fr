---
title: 'Procédure : Énumérer les polices système'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- typography [WPF], enumerating system fonts
- fonts [WPF], enumerating
- system fonts [WPF], enumerating
- enumerating [WPF], system fonts
ms.assetid: 36e37791-55b9-4f01-a496-5cc10335e6a6
ms.openlocfilehash: c7e81b5d1b70ba911a0b505219f7977e019038cf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62001596"
---
# <a name="how-to-enumerate-system-fonts"></a><span data-ttu-id="a3f05-102">Procédure : Énumérer les polices système</span><span class="sxs-lookup"><span data-stu-id="a3f05-102">How to: Enumerate System Fonts</span></span>
## <a name="example"></a><span data-ttu-id="a3f05-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3f05-103">Example</span></span>  
 <span data-ttu-id="a3f05-104">L’exemple suivant montre comment énumérer les polices dans la collection de polices système.</span><span class="sxs-lookup"><span data-stu-id="a3f05-104">The following example shows how to enumerate the fonts in the system font collection.</span></span> <span data-ttu-id="a3f05-105">Le nom de famille de polices de chaque <xref:System.Windows.Media.FontFamily> dans <xref:System.Windows.Media.Fonts.SystemFontFamilies%2A> est ajouté en tant qu’élément à une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="a3f05-105">The font family name of each <xref:System.Windows.Media.FontFamily> within <xref:System.Windows.Media.Fonts.SystemFontFamilies%2A> is added as an item to a combo box.</span></span>  
  
 [!code-csharp[TextOverview#100](~/samples/snippets/csharp/VS_Snippets_Wpf/TextOverview/CSharp/Window1.xaml.cs#100)]
 [!code-vb[TextOverview#100](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextOverview/visualbasic/window1.xaml.vb#100)]  
  
 <span data-ttu-id="a3f05-106">Si plusieurs versions de la même famille de polices résident dans le même répertoire, le [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] énumération de police retourne la version la plus récente de la police.</span><span class="sxs-lookup"><span data-stu-id="a3f05-106">If multiple versions of the same font family reside in the same directory, the [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] font enumeration returns the most recent version of the font.</span></span> <span data-ttu-id="a3f05-107">Si les informations de version ne fournissent pas de résolution, la police avec l’horodateur le plus récent est retournée.</span><span class="sxs-lookup"><span data-stu-id="a3f05-107">If the version information does not provide resolution, the font with latest timestamp is returned.</span></span> <span data-ttu-id="a3f05-108">Si les informations d’horodatage sont équivalentes, le fichier de police qui apparaît en premier dans l’ordre alphabétique est retourné.</span><span class="sxs-lookup"><span data-stu-id="a3f05-108">If the timestamp information is equivalent, the font file that is first in alphabetical order is returned.</span></span>
