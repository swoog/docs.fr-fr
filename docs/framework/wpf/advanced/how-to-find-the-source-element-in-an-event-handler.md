---
title: "Procédure : Rechercher l'élément source dans un gestionnaire d'événements"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- source element in event handlers [WPF]
- event handlers [WPF], finding source element in
ms.assetid: 85f71c5a-b714-4c65-9711-7d905c2bbe98
ms.openlocfilehash: 4cdf1434f2d341cbc1e65541fd02ab4b5cad194d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54536735"
---
# <a name="how-to-find-the-source-element-in-an-event-handler"></a>Procédure : Rechercher l'élément source dans un gestionnaire d'événements
Cet exemple montre comment rechercher l’élément source dans un gestionnaire d’événements.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements qui est déclaré dans un fichier code-behind. Lorsqu’un utilisateur clique sur le bouton que le gestionnaire est attaché à, le gestionnaire modifie une valeur de propriété. Le code du Gestionnaire utilise la <xref:System.Windows.RoutedEventArgs.Source%2A> propriété des données d’événement routé qui sont signalées dans les arguments d’événement pour modifier la <xref:System.Windows.FrameworkElement.Width%2A> valeur de propriété sur le <xref:System.Windows.RoutedEventArgs.Source%2A> élément.  
  
 [!code-xaml[RoutedEventSource#XAMLHandler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventSource/CSharp/default.xaml#xamlhandler)]  
  
 [!code-csharp[RoutedEventSource#Handler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventSource/CSharp/default.xaml.cs#handler)]
 [!code-vb[RoutedEventSource#Handler](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventSource/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.RoutedEventArgs>
- [Vue d’ensemble des événements routés](../../../../docs/framework/wpf/advanced/routed-events-overview.md)
- [Rubriques de guide pratique](../../../../docs/framework/wpf/advanced/events-how-to-topics.md)
