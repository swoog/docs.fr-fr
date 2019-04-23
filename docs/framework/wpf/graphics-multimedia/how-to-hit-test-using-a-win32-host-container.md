---
title: 'Procédure : Test de positionnement à l’aide d’un conteneur hôte Win32'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [WPF], using Win32 host containers
- visual objects [WPF], hit tests on
- Win32 host containers [WPF], hit tests using
ms.assetid: 9491f7f3-d8ba-4573-a888-2f064d1349dc
ms.openlocfilehash: ac5cae5bcd94dc8bf80ff95b8971914e1fa5ba2c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59081461"
---
# <a name="how-to-hit-test-using-a-win32-host-container"></a><span data-ttu-id="d03da-102">Procédure : Test de positionnement à l’aide d’un conteneur hôte Win32</span><span class="sxs-lookup"><span data-stu-id="d03da-102">How to: Hit Test Using a Win32 Host Container</span></span>
<span data-ttu-id="d03da-103">Vous pouvez créer des objets visuels dans un [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] fenêtre en fournissant un hôte de conteneur de fenêtre pour les objets visuels.</span><span class="sxs-lookup"><span data-stu-id="d03da-103">You can create visual objects within a [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] window by providing a host window container for the visual objects.</span></span> <span data-ttu-id="d03da-104">Pour assurer la gestion des événements des objets visuels du conteneur, vous devez traiter les messages transmis à la boucle de filtre de messages du conteneur de fenêtre hôte.</span><span class="sxs-lookup"><span data-stu-id="d03da-104">To provide event handling for the contained visual objects you process the messages passed to the host window container’s message filter loop.</span></span> <span data-ttu-id="d03da-105">Reportez-vous à [didacticiel : Hébergement d’objets visuels dans une Application Win32](tutorial-hosting-visual-objects-in-a-win32-application.md) pour plus d’informations sur l’hébergement d’objets visuels dans un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d03da-105">Refer to [Tutorial: Hosting Visual Objects in a Win32 Application](tutorial-hosting-visual-objects-in-a-win32-application.md) for more information on how to host visual objects in a [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d03da-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="d03da-106">Example</span></span>  
 <span data-ttu-id="d03da-107">Le code suivant montre comment définir des gestionnaires d’événements de souris pour un [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] fenêtre qui est utilisé comme un conteneur hôte pour des objets visuels.</span><span class="sxs-lookup"><span data-stu-id="d03da-107">The following code shows how to set up mouse event handlers for a [!INCLUDE[TLA2#tla_win32](../../../../includes/tla2sharptla-win32-md.md)] window that is used as a host container for visual objects.</span></span>  
  
 [!code-csharp[VisualsHitTesting#103](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyWindow.cs#103)]
 [!code-vb[VisualsHitTesting#103](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyWindow.vb#103)]  
  
 <span data-ttu-id="d03da-108">L’exemple suivant montre comment configurer un test de positionnement en réponse à l’interception d’événements de souris spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d03da-108">The following example shows how to set up a hit test in response to trapping specific mouse events.</span></span>  
  
 [!code-csharp[VisualsHitTesting#104](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsHitTesting/CSharp/MyCircle.cs#104)]
 [!code-vb[VisualsHitTesting#104](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsHitTesting/VisualBasic/MyCircle.vb#104)]  
  
 <span data-ttu-id="d03da-109">Le <xref:System.Windows.Interop.HwndSource> objet présente [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] contenu dans un [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d03da-109">The <xref:System.Windows.Interop.HwndSource> object presents [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] content within a [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] window.</span></span> <span data-ttu-id="d03da-110">La valeur de la <xref:System.Windows.Interop.HwndSource.RootVisual%2A> propriété de la <xref:System.Windows.Interop.HwndSource> objet représente le nœud supérieur dans la hiérarchie d’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="d03da-110">The value of the <xref:System.Windows.Interop.HwndSource.RootVisual%2A> property of the <xref:System.Windows.Interop.HwndSource> object represents the top-most node in the visual tree hierarchy.</span></span>  
  
 <span data-ttu-id="d03da-111">Pour l’exemple complet sur le test de positionnement des objets à l’aide d’un conteneur hôte Win32, consultez [Test de positionnement avec interopérabilité Win32, exemple](https://go.microsoft.com/fwlink/?LinkID=159995).</span><span class="sxs-lookup"><span data-stu-id="d03da-111">For the complete sample on hit testing objects using a Win32 host container, see [Hit Test with Win32 Interoperation Sample](https://go.microsoft.com/fwlink/?LinkID=159995).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d03da-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d03da-112">See also</span></span>

- <xref:System.Windows.Interop.HwndSource>
- [<span data-ttu-id="d03da-113">Test de positionnement dans la couche visuelle</span><span class="sxs-lookup"><span data-stu-id="d03da-113">Hit Testing in the Visual Layer</span></span>](hit-testing-in-the-visual-layer.md)
- [<span data-ttu-id="d03da-114">Tutoriel : Hébergement d’objets visuels dans une Application Win32</span><span class="sxs-lookup"><span data-stu-id="d03da-114">Tutorial: Hosting Visual Objects in a Win32 Application</span></span>](tutorial-hosting-visual-objects-in-a-win32-application.md)
