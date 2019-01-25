---
title: 'Procédure : Utiliser la disposition automatique pour créer un bouton'
ms.date: 03/30/2017
helpviewer_keywords:
- Button controls [WPF], creating with automatic layout
- automatic layout [WPF], creating buttons
ms.assetid: 96c206d0-9e77-4784-9d2d-5045aed2021c
ms.openlocfilehash: 501341f0e71e6e5a224c51e4ae01c68ce6b845cb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54543485"
---
# <a name="how-to-use-automatic-layout-to-create-a-button"></a><span data-ttu-id="4e99a-102">Procédure : Utiliser la disposition automatique pour créer un bouton</span><span class="sxs-lookup"><span data-stu-id="4e99a-102">How to: Use Automatic Layout to Create a Button</span></span>
<span data-ttu-id="4e99a-103">Cet exemple décrit comment tirer parti de la disposition automatique pour créer un bouton dans une application localisable.</span><span class="sxs-lookup"><span data-stu-id="4e99a-103">This example describes how to use the automatic layout approach to create a button in a localizable application.</span></span>  
  
 <span data-ttu-id="4e99a-104">Localisation d’un [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="4e99a-104">Localization of a [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] can be a time consuming process.</span></span> <span data-ttu-id="4e99a-105">Les localisateurs doivent souvent redimensionner et repositionner les éléments, en plus de traduire le texte.</span><span class="sxs-lookup"><span data-stu-id="4e99a-105">Often localizers need to resize and reposition elements in addition to translating text.</span></span> <span data-ttu-id="4e99a-106">Dans le passé chaque langue qu’un [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] était adaptée nécessitait un ajustement.</span><span class="sxs-lookup"><span data-stu-id="4e99a-106">In the past each language that a [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] was adapted for required adjustment.</span></span> <span data-ttu-id="4e99a-107">Désormais avec les capacités de [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] vous pouvez concevoir des éléments qui réduisent les ajustements nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4e99a-107">Now with the capabilities of [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] you can design elements that reduce the need for adjustment.</span></span> <span data-ttu-id="4e99a-108">L’approche consistant à écrire des applications qui peuvent être plus facilement redimensionnées et repositionnées est appelée `automatic layout`.</span><span class="sxs-lookup"><span data-stu-id="4e99a-108">The approach to writing applications that can be more easily resized and repositioned is called `automatic layout`.</span></span>  
  
 <span data-ttu-id="4e99a-109">Les deux [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] exemples créent des applications qui instancient un bouton ; une en anglais et une en espagnol.</span><span class="sxs-lookup"><span data-stu-id="4e99a-109">The following two [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] examples create applications that instantiate a button; one with English text and one with Spanish text.</span></span> <span data-ttu-id="4e99a-110">Notez que le code est identique à l’exception du texte ; le bouton s’ajuste pour s’adapter au texte.</span><span class="sxs-lookup"><span data-stu-id="4e99a-110">Notice that the code is the same except for the text; the button adjusts to fit the text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4e99a-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="4e99a-111">Example</span></span>  
 [!code-xaml[LocalizationBtn_snip#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn_snip/CS/Pane1.xaml#1)]  
  
 [!code-xaml[LocalizationBtn#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn/CS/Pane1.xaml#1)]  
  
 <span data-ttu-id="4e99a-112">Le graphique suivant illustre la sortie des exemples de code.</span><span class="sxs-lookup"><span data-stu-id="4e99a-112">The following graphic shows the output of the code samples.</span></span>  
  
 <span data-ttu-id="4e99a-113">![Même bouton avec le texte dans différentes langues](../../../../docs/framework/wpf/advanced/media/globalizationbutton.png "GlobalizationButton")</span><span class="sxs-lookup"><span data-stu-id="4e99a-113">![The same button with text in different languages](../../../../docs/framework/wpf/advanced/media/globalizationbutton.png "GlobalizationButton")</span></span>  
<span data-ttu-id="4e99a-114">Bouton redimensionnable automatiquement</span><span class="sxs-lookup"><span data-stu-id="4e99a-114">Auto Resizable Button</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e99a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e99a-115">See also</span></span>
- [<span data-ttu-id="4e99a-116">Vue d’ensemble de l’utilisation de la disposition automatique</span><span class="sxs-lookup"><span data-stu-id="4e99a-116">Use Automatic Layout Overview</span></span>](../../../../docs/framework/wpf/advanced/use-automatic-layout-overview.md)
- [<span data-ttu-id="4e99a-117">Utiliser une grille pour la disposition automatique</span><span class="sxs-lookup"><span data-stu-id="4e99a-117">Use a Grid for Automatic Layout</span></span>](../../../../docs/framework/wpf/advanced/how-to-use-a-grid-for-automatic-layout.md)
