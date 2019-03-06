---
title: 'Procédure : Lier des données à un InkCanvas'
ms.date: 03/30/2017
helpviewer_keywords:
- InkCanvas [WPF], binding data to
- binding data [WPF], to InkCanvas
ms.assetid: 8d6b4d9e-ea7f-4412-ba83-3feccec5a515
ms.openlocfilehash: 5d3fc0ed7b6176d7bc68bf20af42c311b5563908
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57372943"
---
# <a name="how-to-data-bind-to-an-inkcanvas"></a>Procédure : Lier des données à un InkCanvas
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment lier le <xref:System.Windows.Controls.InkCanvas.Strokes%2A> propriété d’un <xref:System.Windows.Controls.InkCanvas> vers un autre <xref:System.Windows.Controls.InkCanvas>.  
  
 [!code-xaml[InkCanvasBindingSnippet#2](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#2)]  
  
 L’exemple suivant montre comment lier le <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> propriété à une source de données.  
  
 [!code-xaml[InkCanvasBindingSnippet#3](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#3)]  
[!code-xaml[InkCanvasBindingSnippet#4](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window2.xaml#4)]  
  
 L’exemple suivant déclare deux <xref:System.Windows.Controls.InkCanvas> objets dans XAML et établit la liaison de données entre eux et d’autres sources de données.  La première <xref:System.Windows.Controls.InkCanvas>, appelé `ic`, est lié à deux sources de données.  Le <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> et <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> propriétés sur `ic` sont liés aux <xref:System.Windows.Controls.ListBox> objets, qui sont liés à son tour à des tableaux définis dans le XAML.  Le <xref:System.Windows.Controls.InkCanvas.EditingMode%2A>, <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>, et <xref:System.Windows.Controls.InkCanvas.Strokes%2A> propriétés de la seconde <xref:System.Windows.Controls.InkCanvas> sont liés à la première <xref:System.Windows.Controls.InkCanvas>, `ic`.  
  
 [!code-xaml[InkCanvasBindingSnippet#1](~/samples/snippets/csharp/VS_Snippets_Wpf/InkCanvasBindingSnippet/CS/Window1.xaml#1)]
