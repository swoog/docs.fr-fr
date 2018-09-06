---
title: 'Comment : spécifier une position de menu contextuel personnalisée'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Popup control [WPF], specifying custom position
ms.assetid: 28c24f39-d3aa-4ee2-b950-384b4a5dab92
ms.openlocfilehash: e6e81a6e0819ba3eb39a1c568e6872414e671544
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43724017"
---
# <a name="how-to-specify-a-custom-popup-position"></a><span data-ttu-id="900da-102">Comment : spécifier une position de menu contextuel personnalisée</span><span class="sxs-lookup"><span data-stu-id="900da-102">How to: Specify a Custom Popup Position</span></span>
<span data-ttu-id="900da-103">Cet exemple montre comment spécifier un emplacement personnalisé pour un <xref:System.Windows.Controls.Primitives.Popup> contrôler quand le <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> propriété est définie sur <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>.</span><span class="sxs-lookup"><span data-stu-id="900da-103">This example shows how to specify a custom position for a <xref:System.Windows.Controls.Primitives.Popup> control when the <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> property is set to <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="900da-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="900da-104">Example</span></span>  
 <span data-ttu-id="900da-105">Lorsque le <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> propriété est définie sur <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>, le <xref:System.Windows.Controls.Primitives.Popup> appelle une instance définie de la <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> déléguer.</span><span class="sxs-lookup"><span data-stu-id="900da-105">When the <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> property is set to <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>, the <xref:System.Windows.Controls.Primitives.Popup> calls a defined instance of the <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> delegate.</span></span> <span data-ttu-id="900da-106">Ce délégué retourne un jeu de points possibles qui sont par rapport à l’angle supérieur gauche de la zone cible et le coin supérieur gauche de la <xref:System.Windows.Controls.Primitives.Popup>.</span><span class="sxs-lookup"><span data-stu-id="900da-106">This delegate returns a set of possible points that are relative to the top left corner of the target area and the top left corner of the <xref:System.Windows.Controls.Primitives.Popup>.</span></span> <span data-ttu-id="900da-107">Le <xref:System.Windows.Controls.Primitives.Popup> placement se produit au point qui fournit la meilleure visibilité.</span><span class="sxs-lookup"><span data-stu-id="900da-107">The <xref:System.Windows.Controls.Primitives.Popup> placement occurs at the point that provides the best visibility.</span></span>  
  
 <span data-ttu-id="900da-108">L’exemple suivant montre comment définir la position d’un <xref:System.Windows.Controls.Primitives.Popup> en définissant le <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> propriété <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>.</span><span class="sxs-lookup"><span data-stu-id="900da-108">The following example shows how to define the position of a <xref:System.Windows.Controls.Primitives.Popup> by setting the <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> property to <xref:System.Windows.Controls.Primitives.PlacementMode.Custom>.</span></span> <span data-ttu-id="900da-109">Il montre également comment créer et affecter un <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> délégué afin de positionner le <xref:System.Windows.Controls.Primitives.Popup>.</span><span class="sxs-lookup"><span data-stu-id="900da-109">It also shows how to create and assign a <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> delegate in order to position the <xref:System.Windows.Controls.Primitives.Popup>.</span></span>  <span data-ttu-id="900da-110">Le délégué de rappel retourne deux <xref:System.Windows.Controls.Primitives.CustomPopupPlacement> objets.</span><span class="sxs-lookup"><span data-stu-id="900da-110">The callback delegate returns two <xref:System.Windows.Controls.Primitives.CustomPopupPlacement> objects.</span></span>  <span data-ttu-id="900da-111">Si le <xref:System.Windows.Controls.Primitives.Popup> est masqué par un bord d’écran à la première position, le <xref:System.Windows.Controls.Primitives.Popup> est placé à la deuxième position.</span><span class="sxs-lookup"><span data-stu-id="900da-111">If the <xref:System.Windows.Controls.Primitives.Popup> is hidden by a screen edge at the first position, the <xref:System.Windows.Controls.Primitives.Popup> is placed at the second position.</span></span>  
  
 [!code-xaml[PopupCustomPlacement#CustomPlacement](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml#customplacement)]  
  
 [!code-csharp[PopupCustomPlacement#DelegateInstance](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml.cs#delegateinstance)]
 [!code-vb[PopupCustomPlacement#DelegateInstance](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PopupCustomPlacement/visualbasic/window1.xaml.vb#delegateinstance)]  
  
 [!code-csharp[PopupCustomPlacement#DelegateDefinition](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml.cs#delegatedefinition)]
 [!code-vb[PopupCustomPlacement#DelegateDefinition](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PopupCustomPlacement/visualbasic/window1.xaml.vb#delegatedefinition)]  
  
 <span data-ttu-id="900da-112">Pour obtenir un exemple complet, consultez [positionnement de Popup, exemple](https://go.microsoft.com/fwlink/?LinkID=160032).</span><span class="sxs-lookup"><span data-stu-id="900da-112">For the complete sample, see [Popup Placement Sample](https://go.microsoft.com/fwlink/?LinkID=160032).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="900da-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="900da-113">See Also</span></span>  
 <xref:System.Windows.Controls.Primitives.Popup>  
 [<span data-ttu-id="900da-114">Vue d’ensemble de Popup</span><span class="sxs-lookup"><span data-stu-id="900da-114">Popup Overview</span></span>](../../../../docs/framework/wpf/controls/popup-overview.md)  
 [<span data-ttu-id="900da-115">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="900da-115">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/popup-how-to-topics.md)
