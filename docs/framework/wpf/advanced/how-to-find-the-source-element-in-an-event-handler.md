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
ms.openlocfilehash: 8c1ff53e5af1ddfda17328291c5e22b57a8fe0e2
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57359463"
---
# <a name="how-to-find-the-source-element-in-an-event-handler"></a>Procédure : Rechercher l'élément source dans un gestionnaire d'événements
Cet exemple montre comment rechercher l’élément source dans un gestionnaire d’événements.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements qui est déclaré dans un fichier code-behind. Lorsqu’un utilisateur clique sur le bouton que le gestionnaire est attaché à, le gestionnaire modifie une valeur de propriété. Le code du Gestionnaire utilise la <xref:System.Windows.RoutedEventArgs.Source%2A> propriété des données d’événement routé qui sont signalées dans les arguments d’événement pour modifier la <xref:System.Windows.FrameworkElement.Width%2A> valeur de propriété sur le <xref:System.Windows.RoutedEventArgs.Source%2A> élément.  
  
 [!code-xaml[RoutedEventSource#XAMLHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventSource/CSharp/default.xaml#xamlhandler)]  
  
 [!code-csharp[RoutedEventSource#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventSource/CSharp/default.xaml.cs#handler)]
 [!code-vb[RoutedEventSource#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventSource/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.RoutedEventArgs>
- [Vue d’ensemble des événements routés](routed-events-overview.md)
- [Rubriques de guide pratique](events-how-to-topics.md)
