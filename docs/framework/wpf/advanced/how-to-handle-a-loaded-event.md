---
title: 'Procédure : Gérer un événement chargé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- XAML [WPF], Loaded events
- events [WPF], Loaded
- Loaded events [WPF]
ms.assetid: 0cf8d003-8441-4df4-807a-6db09347e829
ms.openlocfilehash: b8cd2f5e9d848cebb712e7b4930ca39efe48ecc0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59122549"
---
# <a name="how-to-handle-a-loaded-event"></a><span data-ttu-id="657a4-102">Procédure : Gérer un événement chargé</span><span class="sxs-lookup"><span data-stu-id="657a4-102">How to: Handle a Loaded Event</span></span>
<span data-ttu-id="657a4-103">Cet exemple montre comment gérer les <xref:System.Windows.FrameworkElement.Loaded?displayProperty=nameWithType> événement et un scénario approprié pour gérer cet événement.</span><span class="sxs-lookup"><span data-stu-id="657a4-103">This example shows how to handle the <xref:System.Windows.FrameworkElement.Loaded?displayProperty=nameWithType> event, and an appropriate scenario for handling that event.</span></span> <span data-ttu-id="657a4-104">Le gestionnaire crée un <xref:System.Windows.Controls.Button> lorsque la page se charge.</span><span class="sxs-lookup"><span data-stu-id="657a4-104">The handler  creates a <xref:System.Windows.Controls.Button> when the page loads.</span></span>  
  
## <a name="example"></a><span data-ttu-id="657a4-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="657a4-105">Example</span></span>  
 <span data-ttu-id="657a4-106">L’exemple suivant utilise [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] avec un fichier code-behind.</span><span class="sxs-lookup"><span data-stu-id="657a4-106">The following example uses [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] together with a code-behind file.</span></span>  
  
 [!code-xaml[FELoaded#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[FELoaded#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml.cs#handler)]
 [!code-vb[FELoaded#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FELoaded/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a><span data-ttu-id="657a4-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="657a4-107">See also</span></span>

- <xref:System.Windows.FrameworkElement>
- [<span data-ttu-id="657a4-108">Événements de la durée de vie d'un objet</span><span class="sxs-lookup"><span data-stu-id="657a4-108">Object Lifetime Events</span></span>](object-lifetime-events.md)
- [<span data-ttu-id="657a4-109">Vue d'ensemble des événements routés</span><span class="sxs-lookup"><span data-stu-id="657a4-109">Routed Events Overview</span></span>](routed-events-overview.md)
- [<span data-ttu-id="657a4-110">Rubriques Comment</span><span class="sxs-lookup"><span data-stu-id="657a4-110">How-to Topics</span></span>](base-elements-how-to-topics.md)
