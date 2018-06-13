---
title: 'Comment : créer une grille complexe'
ms.date: 03/30/2017
helpviewer_keywords:
- calendar [WPF], creating
- monthly calendar [WPF], creating
- Grid control [WPF], creating [WPF], complex grid
ms.assetid: 4ce3040a-a156-4364-9596-98ca1eca5550
ms.openlocfilehash: 49bf9781d56b93fd4529f3c9b62deb171e69155f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33553593"
---
# <a name="how-to-create-a-complex-grid"></a><span data-ttu-id="41818-102">Comment : créer une grille complexe</span><span class="sxs-lookup"><span data-stu-id="41818-102">How to: Create a Complex Grid</span></span>
<span data-ttu-id="41818-103">Cet exemple montre comment utiliser un <xref:System.Windows.Controls.Grid> pour créer une disposition qui ressemble à un calendrier mensuel.</span><span class="sxs-lookup"><span data-stu-id="41818-103">This example shows how to use a <xref:System.Windows.Controls.Grid> to create layout that looks like a monthly calendar.</span></span>  
  
## <a name="example"></a><span data-ttu-id="41818-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="41818-104">Example</span></span>  
 <span data-ttu-id="41818-105">L’exemple suivant définit huit lignes et huit colonnes à l’aide de la <xref:System.Windows.Controls.RowDefinition> et <xref:System.Windows.Controls.ColumnDefinition> classes.</span><span class="sxs-lookup"><span data-stu-id="41818-105">The following example defines eight rows and eight columns by using the <xref:System.Windows.Controls.RowDefinition> and <xref:System.Windows.Controls.ColumnDefinition> classes.</span></span> <span data-ttu-id="41818-106">Elle utilise le <xref:System.Windows.Controls.Grid.ColumnSpan%2A?displayProperty=nameWithType> et <xref:System.Windows.Controls.Grid.RowSpan%2A?displayProperty=nameWithType> propriétés jointes avec <xref:System.Windows.Shapes.Rectangle> éléments, qui remplissent les arrière-plans des différentes colonnes et lignes.</span><span class="sxs-lookup"><span data-stu-id="41818-106">It uses the <xref:System.Windows.Controls.Grid.ColumnSpan%2A?displayProperty=nameWithType> and <xref:System.Windows.Controls.Grid.RowSpan%2A?displayProperty=nameWithType> attached properties, together with <xref:System.Windows.Shapes.Rectangle> elements, which fill the backgrounds of various columns and rows.</span></span> <span data-ttu-id="41818-107">Cette conception est possible car plusieurs éléments peuvent exister dans chaque cellule dans un <xref:System.Windows.Controls.Grid>, une différence de principe entre <xref:System.Windows.Controls.Grid> et <xref:System.Windows.Documents.Table>.</span><span class="sxs-lookup"><span data-stu-id="41818-107">This design is possible because more than one element can exist in each cell in a <xref:System.Windows.Controls.Grid>, a principle difference between <xref:System.Windows.Controls.Grid> and <xref:System.Windows.Documents.Table>.</span></span>  
  
 <span data-ttu-id="41818-108">L’exemple utilise des dégradés verticaux pour <xref:System.Windows.Shapes.Shape.Fill%2A> les colonnes et les lignes afin d’améliorer la présentation visuelle et la lisibilité du calendrier.</span><span class="sxs-lookup"><span data-stu-id="41818-108">The example uses vertical gradients to <xref:System.Windows.Shapes.Shape.Fill%2A> the columns and rows in order to improve the visual presentation and readability of the calendar.</span></span> <span data-ttu-id="41818-109">Style <xref:System.Windows.Controls.TextBlock> éléments représentent les dates et les jours de la semaine.</span><span class="sxs-lookup"><span data-stu-id="41818-109">Styled <xref:System.Windows.Controls.TextBlock> elements represent the dates and days of the week.</span></span> <span data-ttu-id="41818-110"><xref:System.Windows.Controls.TextBlock> éléments sont absolues dans leurs cellules à l’aide de la <xref:System.Windows.FrameworkElement.Margin%2A> propriété et les propriétés d’alignement sont définies dans le style de l’application.</span><span class="sxs-lookup"><span data-stu-id="41818-110"><xref:System.Windows.Controls.TextBlock> elements are absolutely positioned within their cells by using the <xref:System.Windows.FrameworkElement.Margin%2A> property and alignment properties that are defined within the style for the application.</span></span>  
  
 [!code-xaml[GridComplex#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridComplex/CS/default.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="41818-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41818-111">See Also</span></span>  
 <xref:System.Windows.Controls.Grid>  
 <xref:System.Windows.Documents.TableCell>  
 [<span data-ttu-id="41818-112">Vue d’ensemble de la peinture avec des couleurs unies ou des dégradés</span><span class="sxs-lookup"><span data-stu-id="41818-112">Painting with Solid Colors and Gradients Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)  
 [<span data-ttu-id="41818-113">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="41818-113">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [<span data-ttu-id="41818-114">Vue d’ensemble de Table</span><span class="sxs-lookup"><span data-stu-id="41818-114">Table Overview</span></span>](../../../../docs/framework/wpf/advanced/table-overview.md)
