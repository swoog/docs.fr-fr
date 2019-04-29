---
title: 'Procédure : Créer un événement routé personnalisé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- routed events [WPF], creating
- events [WPF], routing
ms.assetid: b79f459a-1c3f-4045-b2d4-1659cc8eaa3c
ms.openlocfilehash: a3850875c8ca747f8709b55f8fe721d25be24304
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776686"
---
# <a name="how-to-create-a-custom-routed-event"></a><span data-ttu-id="0c35c-102">Procédure : Créer un événement routé personnalisé</span><span class="sxs-lookup"><span data-stu-id="0c35c-102">How to: Create a Custom Routed Event</span></span>
<span data-ttu-id="0c35c-103">Pour votre événement personnalisé prendre en charge le routage d’événement, vous devez inscrire un <xref:System.Windows.RoutedEvent> à l’aide de la <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="0c35c-103">For your custom event to support event routing, you need to register a <xref:System.Windows.RoutedEvent> using the <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> method.</span></span> <span data-ttu-id="0c35c-104">Cet exemple montre les principes de base de la création d’un événement routé personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0c35c-104">This example demonstrates the basics of creating a custom routed event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0c35c-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="0c35c-105">Example</span></span>  
 <span data-ttu-id="0c35c-106">Comme indiqué dans l’exemple suivant, vous inscrire tout d’abord un <xref:System.Windows.RoutedEvent> à l’aide de la <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="0c35c-106">As shown in the following example, you first register a <xref:System.Windows.RoutedEvent> using the <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> method.</span></span> <span data-ttu-id="0c35c-107">Par convention, le <xref:System.Windows.RoutedEvent> nom de champ statique doit se terminer par le suffixe ***événement***.</span><span class="sxs-lookup"><span data-stu-id="0c35c-107">By convention, the <xref:System.Windows.RoutedEvent> static field name should end with the suffix ***Event***.</span></span> <span data-ttu-id="0c35c-108">Dans cet exemple, le nom de l’événement est `Tap` et la stratégie de routage de l’événement est <xref:System.Windows.RoutingStrategy.Bubble>.</span><span class="sxs-lookup"><span data-stu-id="0c35c-108">In this example, the name of the event is `Tap` and the routing strategy of the event is <xref:System.Windows.RoutingStrategy.Bubble>.</span></span> <span data-ttu-id="0c35c-109">Après l’appel d’inscription, vous pouvez fournir des accesseurs d’événement de [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] add et remove pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="0c35c-109">After the registration call, you can provide add-and-remove [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] event accessors for the event.</span></span>  
  
 <span data-ttu-id="0c35c-110">Notez que, même si l’événement est déclenché au moyen de la méthode virtuelle `OnTap` dans cet exemple, la manière dont vous déclenchez votre événement ou dont votre événement répond aux modifications dépend de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="0c35c-110">Note that even though the event is raised through the `OnTap` virtual method in this particular example, how you raise your event or how your event responds to changes depends on your needs.</span></span>  
  
 <span data-ttu-id="0c35c-111">Notez également que cet exemple implémente fondamentalement toute une sous-classe de <xref:System.Windows.Controls.Button>; cette sous-classe est construite comme un assembly distinct, puis instanciée comme une classe personnalisée sur un distinct [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] page.</span><span class="sxs-lookup"><span data-stu-id="0c35c-111">Note also that this example basically implements an entire subclass of <xref:System.Windows.Controls.Button>; that subclass is built as a separate assembly and then instantiated as a custom class on a separate [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] page.</span></span> <span data-ttu-id="0c35c-112">Pour illustrer le concept, les contrôles sous-classés peuvent être insérés dans des arborescences composées d’autres contrôles. Dans cette situation, les événements personnalisés de ces contrôles ont exactement les mêmes fonctionnalités de routage d’événement que tout élément [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] natif.</span><span class="sxs-lookup"><span data-stu-id="0c35c-112">This is to illustrate the concept that subclassed controls can be inserted into trees composed of other controls, and that in this situation, custom events on these controls have the very same event routing capabilities as any native [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] element does.</span></span>  
  
 [!code-csharp[RoutedEventCustom#CustomClass](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventCustom/CSharp/SDKSampleLibrary/class1.cs#customclass)]
 [!code-vb[RoutedEventCustom#CustomClass](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventCustom/VB/SDKSampleLibrary/Class1.vb#customclass)]  
  
 [!code-xaml[RoutedEventCustom#Page](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventCustom/CSharp/RoutedEventCustomApp/default.xaml#page)]  
  
 <span data-ttu-id="0c35c-113">Les événements de tunneling sont créés de la même manière, mais avec <xref:System.Windows.RoutedEvent.RoutingStrategy%2A> la valeur <xref:System.Windows.RoutingStrategy.Tunnel> dans l’appel d’inscription.</span><span class="sxs-lookup"><span data-stu-id="0c35c-113">Tunneling events are created the same way, but with <xref:System.Windows.RoutedEvent.RoutingStrategy%2A> set to <xref:System.Windows.RoutingStrategy.Tunnel> in the registration call.</span></span> <span data-ttu-id="0c35c-114">Par convention, les événements de tunneling dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] sont précédés du préfixe « Preview ».</span><span class="sxs-lookup"><span data-stu-id="0c35c-114">By convention, tunneling events in [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] are prefixed with the word "Preview".</span></span>  
  
 <span data-ttu-id="0c35c-115">Pour voir un exemple du fonctionnement des événements de propagation, consultez [Guide pratique pour gérer un événement routé](how-to-handle-a-routed-event.md).</span><span class="sxs-lookup"><span data-stu-id="0c35c-115">To see an example of how bubbling events work, see [Handle a Routed Event](how-to-handle-a-routed-event.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c35c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c35c-116">See also</span></span>

- [<span data-ttu-id="0c35c-117">Vue d’ensemble des événements routés</span><span class="sxs-lookup"><span data-stu-id="0c35c-117">Routed Events Overview</span></span>](routed-events-overview.md)
- [<span data-ttu-id="0c35c-118">Vue d’ensemble des entrées</span><span class="sxs-lookup"><span data-stu-id="0c35c-118">Input Overview</span></span>](input-overview.md)
- [<span data-ttu-id="0c35c-119">Vue d’ensemble de la création de contrôles</span><span class="sxs-lookup"><span data-stu-id="0c35c-119">Control Authoring Overview</span></span>](../controls/control-authoring-overview.md)
