---
title: 'Procédure : Utiliser la disposition automatique pour créer un bouton'
ms.date: 03/30/2017
helpviewer_keywords:
- Button controls [WPF], creating with automatic layout
- automatic layout [WPF], creating buttons
ms.assetid: 96c206d0-9e77-4784-9d2d-5045aed2021c
ms.openlocfilehash: 8eb1e93dd87c210812c9b7758c744a616ef2d862
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052389"
---
# <a name="how-to-use-automatic-layout-to-create-a-button"></a><span data-ttu-id="a0507-102">Procédure : Utiliser la disposition automatique pour créer un bouton</span><span class="sxs-lookup"><span data-stu-id="a0507-102">How to: Use Automatic Layout to Create a Button</span></span>
<span data-ttu-id="a0507-103">Cet exemple décrit comment tirer parti de la disposition automatique pour créer un bouton dans une application localisable.</span><span class="sxs-lookup"><span data-stu-id="a0507-103">This example describes how to use the automatic layout approach to create a button in a localizable application.</span></span>  
  
 <span data-ttu-id="a0507-104">Localisation d’un [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="a0507-104">Localization of a [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] can be a time consuming process.</span></span> <span data-ttu-id="a0507-105">Les localisateurs doivent souvent redimensionner et repositionner les éléments, en plus de traduire le texte.</span><span class="sxs-lookup"><span data-stu-id="a0507-105">Often localizers need to resize and reposition elements in addition to translating text.</span></span> <span data-ttu-id="a0507-106">Dans le passé chaque langue qu’un [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] était adaptée nécessitait un ajustement.</span><span class="sxs-lookup"><span data-stu-id="a0507-106">In the past each language that a [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] was adapted for required adjustment.</span></span> <span data-ttu-id="a0507-107">Désormais avec les capacités de [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] vous pouvez concevoir des éléments qui réduisent les ajustements nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a0507-107">Now with the capabilities of [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] you can design elements that reduce the need for adjustment.</span></span> <span data-ttu-id="a0507-108">L’approche consistant à écrire des applications qui peuvent être plus facilement redimensionnées et repositionnées est appelée `automatic layout`.</span><span class="sxs-lookup"><span data-stu-id="a0507-108">The approach to writing applications that can be more easily resized and repositioned is called `automatic layout`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a0507-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="a0507-109">Example</span></span>  

<span data-ttu-id="a0507-110">Les deux [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples créent des applications qui instancient un bouton ; une en anglais et une en espagnol.</span><span class="sxs-lookup"><span data-stu-id="a0507-110">The following two [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] examples create applications that instantiate a button; one with English text and one with Spanish text.</span></span> <span data-ttu-id="a0507-111">Notez que le code est identique à l’exception du texte ; le bouton s’ajuste pour s’adapter au texte.</span><span class="sxs-lookup"><span data-stu-id="a0507-111">Notice that the code is the same except for the text; the button adjusts to fit the text.</span></span>

[!code-xaml[LocalizationBtn_snip#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn_snip/CS/Pane1.xaml#1)]  
  
[!code-xaml[LocalizationBtn#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn/CS/Pane1.xaml#1)]  
  
 <span data-ttu-id="a0507-112">Le graphique suivant illustre la sortie des exemples de code avec des boutons redimensionnable automatiquement :</span><span class="sxs-lookup"><span data-stu-id="a0507-112">The following graphic shows the output of the code samples with auto-resizable buttons:</span></span>
  
 ![Même bouton avec le texte dans différentes langues](./media/use-automatic-layout-overview/auto-resizable-button.png)  
  
## <a name="see-also"></a><span data-ttu-id="a0507-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0507-114">See also</span></span>

- [<span data-ttu-id="a0507-115">Vue d’ensemble de l’utilisation de la disposition automatique</span><span class="sxs-lookup"><span data-stu-id="a0507-115">Use Automatic Layout Overview</span></span>](use-automatic-layout-overview.md)
- [<span data-ttu-id="a0507-116">Utiliser une grille pour la disposition automatique</span><span class="sxs-lookup"><span data-stu-id="a0507-116">Use a Grid for Automatic Layout</span></span>](how-to-use-a-grid-for-automatic-layout.md)
