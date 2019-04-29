---
title: 'Procédure : Améliorer les performances de défilement d’un contrôle ListBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListBox control [WPF], reusing item containers
- ListBox control [WPF], improving scrolling performance
ms.assetid: 1e2bf8f3-c8ce-47f7-a400-a7fe11d1a848
ms.openlocfilehash: a9d1ca1d8ac2ef830984408f3052eb0ed0987c5d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770862"
---
# <a name="how-to-improve-the-scrolling-performance-of-a-listbox"></a>Procédure : Améliorer les performances de défilement d’un contrôle ListBox
Si un <xref:System.Windows.Controls.ListBox> contient de nombreux éléments, la réponse de l’interface utilisateur peut être lente lorsqu’un utilisateur fait défiler le <xref:System.Windows.Controls.ListBox> à l’aide de la roulette de souris ou en faisant glisser le curseur d’une barre de défilement. Vous pouvez améliorer les performances de la <xref:System.Windows.Controls.ListBox> lorsque l’utilisateur fait défiler en définissant le `VirtualizingStackPanel.VirtualizationMode` propriété jointe <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>.  
  
## <a name="example"></a>Exemple  
  
## <a name="description"></a>Description  
L’exemple suivant crée un <xref:System.Windows.Controls.ListBox> et définit le `VirtualizingStackPanel.VirtualizationMode` propriété jointe <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> pour améliorer les performances pendant le défilement.  
  
## <a name="code"></a>Code  
 [!code-xaml[RecycleItemContainerShippets#VirtualizationMode](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizationmode)]  
  
 L’exemple suivant montre les données que l’exemple précédent utilise.  
  
 [!code-csharp[RecycleItemContainerShippets#ListBoxData](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#listboxdata)]
 [!code-vb[RecycleItemContainerShippets#ListBoxData](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#listboxdata)]
