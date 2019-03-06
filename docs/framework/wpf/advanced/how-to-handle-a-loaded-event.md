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
ms.openlocfilehash: a4916d3cfd20d082a8466f61fc74e16db2f0f346
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57353346"
---
# <a name="how-to-handle-a-loaded-event"></a>Procédure : Gérer un événement chargé
Cet exemple montre comment gérer les <xref:System.Windows.FrameworkElement.Loaded?displayProperty=nameWithType> événement et un scénario approprié pour gérer cet événement. Le gestionnaire crée un <xref:System.Windows.Controls.Button> lorsque la page se charge.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] avec un fichier code-behind.  
  
 [!code-xaml[FELoaded#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[FELoaded#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/FELoaded/CSharp/default.xaml.cs#handler)]
 [!code-vb[FELoaded#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FELoaded/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.FrameworkElement>
- [Événements de la durée de vie d’un objet](object-lifetime-events.md)
- [Vue d’ensemble des événements routés](routed-events-overview.md)
- [Rubriques de guide pratique](base-elements-how-to-topics.md)
