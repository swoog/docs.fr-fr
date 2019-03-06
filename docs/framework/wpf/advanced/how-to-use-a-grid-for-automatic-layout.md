---
title: 'Procédure : Utiliser une grille pour la disposition automatique'
ms.date: 03/30/2017
helpviewer_keywords:
- grids [WPF], automatic layout
- automatic layout [WPF], grid use
ms.assetid: ab9de407-e0c1-4047-bdf0-24951bf73879
ms.openlocfilehash: 5fa023002ac66a65e3c179434841c975287d170c
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357480"
---
# <a name="how-to-use-a-grid-for-automatic-layout"></a><span data-ttu-id="f2b7c-102">Procédure : Utiliser une grille pour la disposition automatique</span><span class="sxs-lookup"><span data-stu-id="f2b7c-102">How to: Use a Grid for Automatic Layout</span></span>
<span data-ttu-id="f2b7c-103">Cet exemple décrit comment utiliser une grille quand vous tirez parti de la disposition automatique pour créer une application localisable.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-103">This example describes how to use a grid in the automatic layout approach to creating a localizable application.</span></span>  
  
 <span data-ttu-id="f2b7c-104">Localisation d’un [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-104">Localization of a [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] can be a time consuming process.</span></span> <span data-ttu-id="f2b7c-105">Les localisateurs doivent souvent redimensionner et repositionner les éléments, en plus de traduire le texte.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-105">Often localizers need to re-size and reposition elements in addition to translating text.</span></span> <span data-ttu-id="f2b7c-106">Dans le passé chaque langue qu’un [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] était adaptée nécessitait un ajustement.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-106">In the past each language that a [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] was adapted for required adjustment.</span></span> <span data-ttu-id="f2b7c-107">Désormais avec les capacités de [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] vous pouvez concevoir des éléments qui réduisent les ajustements nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-107">Now with the capabilities of [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] you can design elements that reduce the need for adjustment.</span></span> <span data-ttu-id="f2b7c-108">L’approche consistant à écrire des applications qui peuvent être plus facilement redimensionnées et repositionnées est appelée `auto layout`.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-108">The approach to writing applications that can be more easily re-sized and repositioned is called `auto layout`.</span></span>  
  
 <span data-ttu-id="f2b7c-109">Ce qui suit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemple illustre l’utilisation d’une grille pour positionner des boutons et du texte.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-109">The following [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] example demonstrates using a grid to position some buttons and text.</span></span> <span data-ttu-id="f2b7c-110">Notez que la hauteur et la largeur des cellules sont définies sur `Auto`; par conséquent, la cellule qui contient le bouton avec une image s’ajuste pour s’ajuster à l’image.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-110">Notice that the height and width of the cells are set to `Auto`; therefore the cell that contains the button with an image adjusts to fit the image.</span></span> <span data-ttu-id="f2b7c-111">Étant donné que le <xref:System.Windows.Controls.Grid> élément pouvant s’ajuster à son contenu, il peut être utile lorsque vous effectuez l’approche de la disposition automatique pour concevoir des applications qui peuvent être localisées.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-111">Because the <xref:System.Windows.Controls.Grid> element can adjust to its content it can be useful when taking the automatic layout approach to designing applications that can be localized.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f2b7c-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2b7c-112">Example</span></span>  
 <span data-ttu-id="f2b7c-113">L’exemple suivant montre comment utiliser une grille.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-113">The following example shows how to use a grid.</span></span>  
  
 [!code-xaml[LocalizationGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationGrid/CS/Pane1.xaml#1)]  
  
 <span data-ttu-id="f2b7c-114">Le graphique suivant montre la sortie générée par l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="f2b7c-114">The following graphic shows the output of the code sample.</span></span>  
  
 <span data-ttu-id="f2b7c-115">![Exemple de grille](./media/glob-grid.png "glob_grid")</span><span class="sxs-lookup"><span data-stu-id="f2b7c-115">![Grid example](./media/glob-grid.png "glob_grid")</span></span>  
<span data-ttu-id="f2b7c-116">Grille</span><span class="sxs-lookup"><span data-stu-id="f2b7c-116">Grid</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2b7c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2b7c-117">See also</span></span>
- [<span data-ttu-id="f2b7c-118">Vue d’ensemble de l’utilisation de la disposition automatique</span><span class="sxs-lookup"><span data-stu-id="f2b7c-118">Use Automatic Layout Overview</span></span>](use-automatic-layout-overview.md)
- [<span data-ttu-id="f2b7c-119">Utiliser la disposition automatique pour créer un bouton</span><span class="sxs-lookup"><span data-stu-id="f2b7c-119">Use Automatic Layout to Create a Button</span></span>](how-to-use-automatic-layout-to-create-a-button.md)
