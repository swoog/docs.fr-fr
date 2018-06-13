---
title: Dessiner du texte à l'aide de glyphes
ms.date: 03/30/2017
helpviewer_keywords:
- text [WPF], drawing with Glyphs objects
- Glyphs objects [WPF], drawing text
- typography [WPF], Glyphs objects
ms.assetid: 587ab17e-a419-4ad5-b6da-8933a8e83d97
ms.openlocfilehash: e2b35eb6df140551d5db7d597826df53e37182fe
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33542524"
---
# <a name="draw-text-using-glyphs"></a><span data-ttu-id="90a34-102">Dessiner du texte à l'aide de glyphes</span><span class="sxs-lookup"><span data-stu-id="90a34-102">Draw Text Using Glyphs</span></span>
<span data-ttu-id="90a34-103">Cette rubrique explique comment utiliser le plus bas niveau <xref:System.Windows.Documents.Glyphs> objet pour afficher le texte dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="90a34-103">This topic explains how to use the low-level <xref:System.Windows.Documents.Glyphs> object to display text in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span></span>  
  
## <a name="example"></a><span data-ttu-id="90a34-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="90a34-104">Example</span></span>  
 <span data-ttu-id="90a34-105">Les exemples suivants montrent comment définir des propriétés pour un <xref:System.Windows.Documents.Glyphs> dans l’objet [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="90a34-105">The following examples show how to define properties for a <xref:System.Windows.Documents.Glyphs> object in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span></span> <span data-ttu-id="90a34-106">Le <xref:System.Windows.Documents.Glyphs> objet représente la sortie d’un <xref:System.Windows.Media.GlyphRun> dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="90a34-106">The <xref:System.Windows.Documents.Glyphs> object represents the output of a <xref:System.Windows.Media.GlyphRun> in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].</span></span> <span data-ttu-id="90a34-107">Ces exemples supposent que les polices Arial, Courrier New et Times New Roman sont installées dans le dossier C:\WINDOWS\Fonts sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="90a34-107">The examples assume that the Arial, Courier New, and Times New Roman fonts are installed in the C:\WINDOWS\Fonts folder on the local computer.</span></span>  
  
 [!code-xaml[GlyphsOvwSample1#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GlyphsOvwSample1/CS/default.xaml#1)]  
  
 <span data-ttu-id="90a34-108">Cet exemple montre comment définir les autres propriétés de <xref:System.Windows.Documents.Glyphs> dans des objets [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="90a34-108">This example shows how to define other properties of <xref:System.Windows.Documents.Glyphs> objects in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].</span></span>  
  
 [!code-xaml[GlyphsOvwSamp2#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GlyphsOvwSamp2/CS/default.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="90a34-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90a34-109">See Also</span></span>  
 [<span data-ttu-id="90a34-110">Typographie dans WPF</span><span class="sxs-lookup"><span data-stu-id="90a34-110">Typography in WPF</span></span>](../../../../docs/framework/wpf/advanced/typography-in-wpf.md)
