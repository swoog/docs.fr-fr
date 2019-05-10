---
title: 'Procédure : Ajouter un gestionnaire d’événements à l’aide de code'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- event handlers [WPF], adding
- XAML [WPF], adding event handlers
ms.assetid: 269c61e0-6bd9-4291-9bed-1c5ee66da486
ms.openlocfilehash: 32e3926bb4c519b7be14a26484603d6d4ea88b6a
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64665797"
---
# <a name="how-to-add-an-event-handler-using-code"></a><span data-ttu-id="92546-102">Procédure : Ajouter un gestionnaire d’événements à l’aide de code</span><span class="sxs-lookup"><span data-stu-id="92546-102">How to: Add an Event Handler Using Code</span></span>
<span data-ttu-id="92546-103">Cet exemple montre comment ajouter un gestionnaire d’événements à un élément à l’aide de code.</span><span class="sxs-lookup"><span data-stu-id="92546-103">This example shows how to add an event handler to an element by using code.</span></span>  
  
 <span data-ttu-id="92546-104">Si vous souhaitez ajouter un gestionnaire d’événements à un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] élément et la page de balisage qui contient l’élément a déjà été chargé, vous devez ajouter le gestionnaire à l’aide de code.</span><span class="sxs-lookup"><span data-stu-id="92546-104">If you want to add an event handler to a [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] element, and the markup page that contains the element has already been loaded, you must add the handler using code.</span></span> <span data-ttu-id="92546-105">Vous pouvez également, si vous développez l’arborescence d’éléments pour une application entièrement à l’aide de code et ne déclare ne pas tous les éléments à l’aide de [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez appeler des méthodes spécifiques pour ajouter des gestionnaires d’événements à l’arborescence d’éléments construite.</span><span class="sxs-lookup"><span data-stu-id="92546-105">Alternatively, if you are building up the element tree for an application entirely using code and not declaring any elements using [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], you can call specific methods to add event handlers to the constructed element tree.</span></span>  
  
## <a name="example"></a><span data-ttu-id="92546-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="92546-106">Example</span></span>  
 <span data-ttu-id="92546-107">L’exemple suivant ajoute un nouveau <xref:System.Windows.Controls.Button> à une page existante définie initialement dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="92546-107">The following example adds a new <xref:System.Windows.Controls.Button> to an existing page that is initially defined in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].</span></span> <span data-ttu-id="92546-108">Un fichier code-behind implémente une méthode de gestionnaire d’événements et puis ajoute cette méthode comme un gestionnaire d’événements sur le <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="92546-108">A code-behind file implements an event handler method and then adds that method as a new event handler on the <xref:System.Windows.Controls.Button>.</span></span>  
  
 <span data-ttu-id="92546-109">Le C# exemple utilise le `+=` opérateur pour affecter un gestionnaire à un événement.</span><span class="sxs-lookup"><span data-stu-id="92546-109">The C# example uses the `+=` operator to assign a handler to an event.</span></span> <span data-ttu-id="92546-110">C’est le même opérateur qui est utilisé pour affecter un gestionnaire dans le [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] modèle de gestion d’événements.</span><span class="sxs-lookup"><span data-stu-id="92546-110">This is the same operator that is used to assign a handler in the [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] event handling model.</span></span> <span data-ttu-id="92546-111">Microsoft Visual Basic ne prend pas en charge cet opérateur comme un moyen d’ajouter des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="92546-111">Microsoft Visual Basic does not support this operator as a means of adding event handlers.</span></span> <span data-ttu-id="92546-112">Au lieu de cela, il requiert une des deux techniques :</span><span class="sxs-lookup"><span data-stu-id="92546-112">It instead requires one of two techniques:</span></span>  
  
- <span data-ttu-id="92546-113">Utilisez le <xref:System.Windows.UIElement.AddHandler%2A> (méthode), avec un `AddressOf` opérateur, pour faire référence à l’implémentation de gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="92546-113">Use the <xref:System.Windows.UIElement.AddHandler%2A> method, together with an `AddressOf` operator, to reference the event handler implementation.</span></span>  
  
- <span data-ttu-id="92546-114">Utilisez le `Handles` mot clé dans le cadre de la définition de gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="92546-114">Use the `Handles` keyword as part of the event handler definition.</span></span> <span data-ttu-id="92546-115">Cette technique n’est pas indiquée ici ; consultez [Visual Basic et la gestion des événements de WPF](visual-basic-and-wpf-event-handling.md).</span><span class="sxs-lookup"><span data-stu-id="92546-115">This technique is not shown here; see [Visual Basic and WPF Event Handling](visual-basic-and-wpf-event-handling.md).</span></span>  
  
 [!code-xaml[RoutedEventAddRemoveHandler#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[RoutedEventAddRemoveHandler#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/CSharp/default.xaml.cs#handler)]
 [!code-vb[RoutedEventAddRemoveHandler#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/VisualBasic/default.xaml.vb#handler)]  
  
> [!NOTE]
>  <span data-ttu-id="92546-116">Ajout d’un gestionnaire d’événements dans analysée initialement [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] page est beaucoup plus simple.</span><span class="sxs-lookup"><span data-stu-id="92546-116">Adding an event handler in the initially parsed [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] page is much simpler.</span></span> <span data-ttu-id="92546-117">Dans l’élément objet dans lequel vous souhaitez ajouter le Gestionnaire d’événements, ajoutez un attribut qui correspond au nom de l’événement que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="92546-117">Within the object element where you want to add the event handler, add an attribute that matches the name of the event that you want to handle.</span></span> <span data-ttu-id="92546-118">Puis spécifiez la valeur de cet attribut comme nom de la méthode de gestionnaire d’événements que vous avez défini dans le fichier code-behind de la [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] page.</span><span class="sxs-lookup"><span data-stu-id="92546-118">Then specify the value of that attribute as the name of the event handler method that you defined in the code-behind file of the [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] page.</span></span> <span data-ttu-id="92546-119">Pour plus d’informations, consultez [vue d’ensemble de XAML (WPF)](xaml-overview-wpf.md) ou [vue d’ensemble des événements routés](routed-events-overview.md).</span><span class="sxs-lookup"><span data-stu-id="92546-119">For more information, see [XAML Overview (WPF)](xaml-overview-wpf.md) or [Routed Events Overview](routed-events-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92546-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92546-120">See also</span></span>

- [<span data-ttu-id="92546-121">Vue d’ensemble des événements routés</span><span class="sxs-lookup"><span data-stu-id="92546-121">Routed Events Overview</span></span>](routed-events-overview.md)
- [<span data-ttu-id="92546-122">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="92546-122">How-to Topics</span></span>](events-how-to-topics.md)
