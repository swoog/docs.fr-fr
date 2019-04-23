---
title: 'Procédure : Créer un élément de grille'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], creating [WPF], grid instance
ms.assetid: b2f07626-9df8-43b8-8d36-492f3cb42837
ms.openlocfilehash: ebb9369da73bd595338e5b6ef42bda639bde6ed4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59134535"
---
# <a name="how-to-create-a-grid-element"></a><span data-ttu-id="d15dc-102">Procédure : Créer un élément de grille</span><span class="sxs-lookup"><span data-stu-id="d15dc-102">How to: Create a Grid Element</span></span>
## <a name="example"></a><span data-ttu-id="d15dc-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="d15dc-103">Example</span></span>  
 <span data-ttu-id="d15dc-104">L’exemple suivant montre comment créer et utiliser une instance de <xref:System.Windows.Controls.Grid> à l’aide [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] ou du code.</span><span class="sxs-lookup"><span data-stu-id="d15dc-104">The following example shows how to create and use an instance of <xref:System.Windows.Controls.Grid> by using either [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] or code.</span></span> <span data-ttu-id="d15dc-105">Cet exemple utilise trois <xref:System.Windows.Controls.ColumnDefinition> objets et trois <xref:System.Windows.Controls.RowDefinition> objets pour créer une grille qui a neuf cellules, comme dans une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="d15dc-105">This example uses three <xref:System.Windows.Controls.ColumnDefinition> objects and three <xref:System.Windows.Controls.RowDefinition> objects to create a grid that has nine cells, such as in a worksheet.</span></span> <span data-ttu-id="d15dc-106">Chaque cellule contient un <xref:System.Windows.Controls.TextBlock> élément qui représente les données et la ligne supérieure contient un <xref:System.Windows.Controls.TextBlock> avec le <xref:System.Windows.Controls.Grid.ColumnSpan%2A> propriété appliqué.</span><span class="sxs-lookup"><span data-stu-id="d15dc-106">Each cell contains a <xref:System.Windows.Controls.TextBlock> element that represents data, and the top row contains a <xref:System.Windows.Controls.TextBlock> with the <xref:System.Windows.Controls.Grid.ColumnSpan%2A> property applied.</span></span> <span data-ttu-id="d15dc-107">Pour afficher les limites de chaque cellule, le <xref:System.Windows.Controls.Grid.ShowGridLines%2A> propriété est activée.</span><span class="sxs-lookup"><span data-stu-id="d15dc-107">To show the boundaries of each cell, the <xref:System.Windows.Controls.Grid.ShowGridLines%2A> property is enabled.</span></span>  
  
 [!code-csharp[Grid#3](~/samples/snippets/csharp/VS_Snippets_Wpf/Grid/CSharp/Grid_Code.cs#3)]
 [!code-vb[Grid#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Grid/VisualBasic/grid_vb.vb#3)]
 [!code-xaml[Grid#3](~/samples/snippets/xaml/VS_Snippets_Wpf/Grid/XAML/default.xaml#3)]  
  
  <span data-ttu-id="d15dc-108">Chacune de ces approches génère une interface utilisateur qui ressemble beaucoup, comme celui ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d15dc-108">Either approach will generate a user interface that looks much the same, like the one below.</span></span>

  ![une capture d’écran illustre une interface utilisateur WPF qui contient une grille divisée en trois colonnes.](././media/how-to-create-a-grid-element/how-to-create-a-grid-element.png)
## <a name="see-also"></a><span data-ttu-id="d15dc-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d15dc-112">See also</span></span>

- <xref:System.Windows.Controls.Grid>
- [<span data-ttu-id="d15dc-113">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="d15dc-113">Panels Overview</span></span>](panels-overview.md)
