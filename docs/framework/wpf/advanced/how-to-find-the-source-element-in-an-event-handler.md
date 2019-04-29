---
title: 'Procédure : Rechercher l’élément source dans un gestionnaire d’événements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- source element in event handlers [WPF]
- event handlers [WPF], finding source element in
ms.assetid: 85f71c5a-b714-4c65-9711-7d905c2bbe98
ms.openlocfilehash: 9a49878c9ad8313903df4506796998fd43e2e749
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61757506"
---
# <a name="how-to-find-the-source-element-in-an-event-handler"></a><span data-ttu-id="be869-102">Procédure : Rechercher l’élément source dans un gestionnaire d’événements</span><span class="sxs-lookup"><span data-stu-id="be869-102">How to: Find the Source Element in an Event Handler</span></span>
<span data-ttu-id="be869-103">Cet exemple montre comment rechercher l’élément source dans un gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="be869-103">This example shows how to find the source element in an event handler.</span></span>  
  
## <a name="example"></a><span data-ttu-id="be869-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="be869-104">Example</span></span>  
 <span data-ttu-id="be869-105">L’exemple suivant montre un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements qui est déclaré dans un fichier code-behind.</span><span class="sxs-lookup"><span data-stu-id="be869-105">The following example shows a <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event handler that is declared in a code-behind file.</span></span> <span data-ttu-id="be869-106">Lorsqu’un utilisateur clique sur le bouton que le gestionnaire est attaché à, le gestionnaire modifie une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="be869-106">When a user clicks the button that the handler is attached to, the handler changes a property value.</span></span> <span data-ttu-id="be869-107">Le code du Gestionnaire utilise la <xref:System.Windows.RoutedEventArgs.Source%2A> propriété des données d’événement routé qui sont signalées dans les arguments d’événement pour modifier la <xref:System.Windows.FrameworkElement.Width%2A> valeur de propriété sur le <xref:System.Windows.RoutedEventArgs.Source%2A> élément.</span><span class="sxs-lookup"><span data-stu-id="be869-107">The handler code uses the <xref:System.Windows.RoutedEventArgs.Source%2A> property of the routed event data that is reported in the event arguments to change the <xref:System.Windows.FrameworkElement.Width%2A> property value on the <xref:System.Windows.RoutedEventArgs.Source%2A> element.</span></span>  
  
 [!code-xaml[RoutedEventSource#XAMLHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventSource/CSharp/default.xaml#xamlhandler)]  
  
 [!code-csharp[RoutedEventSource#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventSource/CSharp/default.xaml.cs#handler)]
 [!code-vb[RoutedEventSource#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventSource/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a><span data-ttu-id="be869-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be869-108">See also</span></span>

- <xref:System.Windows.RoutedEventArgs>
- [<span data-ttu-id="be869-109">Vue d’ensemble des événements routés</span><span class="sxs-lookup"><span data-stu-id="be869-109">Routed Events Overview</span></span>](routed-events-overview.md)
- [<span data-ttu-id="be869-110">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="be869-110">How-to Topics</span></span>](events-how-to-topics.md)
