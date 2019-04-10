---
title: 'Procédure : Configurer la notification de mises à jour de liaisons'
ms.date: 03/30/2017
helpviewer_keywords:
- notifications [WPF], binding updates
- data binding [WPF], notification of binding updates
- binding [WPF], updates [WPF], notifications of
ms.assetid: 5673073e-dbe1-49da-980a-484a88f9595a
ms.openlocfilehash: 4185198312ed98f9aaa1388626600d9f21abae55
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59213960"
---
# <a name="how-to-set-up-notification-of-binding-updates"></a><span data-ttu-id="b6d8a-102">Procédure : Configurer la notification de mises à jour de liaisons</span><span class="sxs-lookup"><span data-stu-id="b6d8a-102">How to: Set Up Notification of Binding Updates</span></span>
<span data-ttu-id="b6d8a-103">Cet exemple montre comment configurer l’envoi d’une notification lorsque la propriété de la cible de liaison (cible) ou de la source de liaison (source) d’une liaison a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b6d8a-103">This example shows how to set up to be notified when the binding target (target) or the binding source (source) property of a binding has been updated.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b6d8a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6d8a-104">Example</span></span>  
 [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] <span data-ttu-id="b6d8a-105">déclenche un événement de mise à jour de données chaque fois que la source de liaison ou la cible a été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="b6d8a-105">raises a data update event each time that the binding source or target has been updated.</span></span> <span data-ttu-id="b6d8a-106">En interne, cet événement est utilisé pour informer l’[!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] qu’elle doit se mettre à jour, car les données liées ont changé.</span><span class="sxs-lookup"><span data-stu-id="b6d8a-106">Internally, this event is used to inform the [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] that it should update, because the bound data has changed.</span></span> <span data-ttu-id="b6d8a-107">Notez que pour ces événements fonctionnent et également pour la liaison unidirectionnelle ou bidirectionnelle fonctionne correctement, vous devez implémenter votre classe de données à l’aide de la <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span><span class="sxs-lookup"><span data-stu-id="b6d8a-107">Note that for these events to work, and also for one-way or two-way binding to work properly, you need to implement your data class using the <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span></span> <span data-ttu-id="b6d8a-108">Pour plus d’informations, consultez [Implémenter la notification des modifications de propriétés](how-to-implement-property-change-notification.md).</span><span class="sxs-lookup"><span data-stu-id="b6d8a-108">For more information, see [Implement Property Change Notification](how-to-implement-property-change-notification.md).</span></span>  
  
 <span data-ttu-id="b6d8a-109">Définir le <xref:System.Windows.Data.Binding.NotifyOnTargetUpdated%2A> ou <xref:System.Windows.Data.Binding.NotifyOnSourceUpdated%2A> propriété (ou les deux) à `true` dans la liaison.</span><span class="sxs-lookup"><span data-stu-id="b6d8a-109">Set the <xref:System.Windows.Data.Binding.NotifyOnTargetUpdated%2A> or <xref:System.Windows.Data.Binding.NotifyOnSourceUpdated%2A> property (or both) to `true` in the binding.</span></span> <span data-ttu-id="b6d8a-110">Le gestionnaire que vous fournissez pour écouter cet événement doit être directement attaché à l’élément sur lequel vous souhaitez être informé des modifications, ou au contexte de données global si vous souhaitez savoir que quelque chose dans le contexte a changé.</span><span class="sxs-lookup"><span data-stu-id="b6d8a-110">The handler you provide to listen for this event must be attached directly to the element where you want to be informed of changes, or to the overall data context if you want to be aware that anything in the context has changed.</span></span>  
  
 <span data-ttu-id="b6d8a-111">Voici un exemple qui montre comment configurer la notification lorsqu’une propriété cible a été mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b6d8a-111">Here is an example that shows how to set up for notification when a target property has been updated.</span></span>  
  
 [!code-xaml[DirectionalBinding#2](~/samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml#2)]  
  
 <span data-ttu-id="b6d8a-112">Vous pouvez ensuite affecter un gestionnaire basé sur le délégué EventHandler\<T >, *OnTargetUpdated* dans cet exemple, pour gérer l’événement :</span><span class="sxs-lookup"><span data-stu-id="b6d8a-112">You can then assign a handler based on the EventHandler\<T> delegate, *OnTargetUpdated* in this example, to handle the event:</span></span>  
  
 [!code-csharp[DirectionalBinding#3](~/samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml.cs#3)]  
[!code-csharp[DirectionalBinding#EndEvent](~/samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml.cs#endevent)]  
  
 <span data-ttu-id="b6d8a-113">Les paramètres de l’événement peuvent être utilisés pour déterminer les détails de la propriété qui ont changé (par exemple, le type ou l’élément spécifique si le même gestionnaire est attaché à plusieurs éléments), ce qui peut être utile si plusieurs propriétés sont liées sur un seul élément.</span><span class="sxs-lookup"><span data-stu-id="b6d8a-113">Parameters of the event can be used to determine details about the property that changed (such as the type or the specific element if the same handler is attached to more than one element), which can be useful if there are multiple bound properties on a single element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6d8a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6d8a-114">See also</span></span>

- [<span data-ttu-id="b6d8a-115">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="b6d8a-115">Data Binding Overview</span></span>](data-binding-overview.md)
- [<span data-ttu-id="b6d8a-116">Rubriques Comment</span><span class="sxs-lookup"><span data-stu-id="b6d8a-116">How-to Topics</span></span>](data-binding-how-to-topics.md)
