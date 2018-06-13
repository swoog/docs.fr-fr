---
title: "Comment : ajouter un gestionnaire d'événements à l'aide de code"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- event handlers [WPF], adding
- XAML [WPF], adding event handlers
ms.assetid: 269c61e0-6bd9-4291-9bed-1c5ee66da486
ms.openlocfilehash: 782f668557c3cb081d30e7835006af63c9ca4df5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33542621"
---
# <a name="how-to-add-an-event-handler-using-code"></a>Comment : ajouter un gestionnaire d'événements à l'aide de code
Cet exemple montre comment ajouter un gestionnaire d’événements à un élément à l’aide de code.  
  
 Si vous souhaitez ajouter un gestionnaire d’événements à un [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] élément et la page de balisage qui contient l’élément a déjà été chargé, vous devez ajouter le gestionnaire à l’aide de code. Vous pouvez également, si vous développez l’arborescence d’éléments pour une application entièrement à l’aide de code et ne déclare ne pas tous les éléments à l’aide de [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], vous pouvez appeler des méthodes spécifiques pour ajouter des gestionnaires d’événements à l’arborescence d’éléments construite.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant ajoute un nouveau <xref:System.Windows.Controls.Button> à une page existante définie initialement dans [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]. Un fichier code-behind implémente une méthode de gestionnaire d’événements et puis ajoute cette méthode comme un gestionnaire d’événements sur le <xref:System.Windows.Controls.Button>.  
  
 L’exemple c# utilise le `+=` opérateur pour assigner un gestionnaire à un événement. C’est le même opérateur qui est utilisé pour affecter un gestionnaire dans le [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] modèle de gestion d’événements. Microsoft Visual Basic ne prend pas en charge cet opérateur comme un moyen d’ajouter des gestionnaires d’événements. Au lieu de cela, il requiert une des deux techniques :  
  
-   Utilisez le <xref:System.Windows.UIElement.AddHandler%2A> méthode, avec un `AddressOf` (opérateur), pour faire référence à l’implémentation de gestionnaire d’événements.  
  
-   Utilisez le `Handles` mot clé dans le cadre de la définition de gestionnaire d’événements. Cette technique n’est pas indiquée ici ; consultez [Visual Basic et la gestion des événements de WPF](../../../../docs/framework/wpf/advanced/visual-basic-and-wpf-event-handling.md).  
  
 [!code-xaml[RoutedEventAddRemoveHandler#XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[RoutedEventAddRemoveHandler#Handler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/CSharp/default.xaml.cs#handler)]
 [!code-vb[RoutedEventAddRemoveHandler#Handler](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventAddRemoveHandler/VisualBasic/default.xaml.vb#handler)]  
  
> [!NOTE]
>  Ajout d’un gestionnaire d’événements dans analysée initialement [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] page est beaucoup plus simple. Dans l’élément d’objet sur lequel vous souhaitez ajouter le Gestionnaire d’événements, ajoutez un attribut qui correspond au nom de l’événement que vous souhaitez gérer. Puis spécifiez la valeur de cet attribut comme nom de la méthode de gestionnaire d’événements que vous avez définie dans le fichier code-behind de la [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] page. Pour plus d’informations, consultez [vue d’ensemble du XAML (WPF)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md) ou [vue d’ensemble des événements routés](../../../../docs/framework/wpf/advanced/routed-events-overview.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble des événements routés](../../../../docs/framework/wpf/advanced/routed-events-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/advanced/events-how-to-topics.md)
