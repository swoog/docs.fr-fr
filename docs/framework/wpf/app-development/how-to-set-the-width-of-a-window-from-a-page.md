---
title: 'Procédure : Définir la largeur d’une fenêtre à partir d’une Page'
ms.date: 03/30/2017
helpviewer_keywords:
- width of windows [WPF], setting from a page
- windows [WPF], setting width from a page
- pages [WPF], setting window width from
ms.assetid: 31601c92-7889-472a-b07e-bf675ad21c92
ms.openlocfilehash: fee6d4c9ae9dae03e81cc4be56576763cb59958b
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57379352"
---
# <a name="how-to-set-the-width-of-a-window-from-a-page"></a>Procédure : Définir la largeur d’une fenêtre à partir d’une Page
Cet exemple illustre comment définir la largeur de la fenêtre à partir d’un <xref:System.Windows.Controls.Page>.  
  
## <a name="example"></a>Exemple  
 Un <xref:System.Windows.Controls.Page> pouvez définir la largeur de sa fenêtre hôte en définissant <xref:System.Windows.Controls.Page.WindowWidth%2A>. Cette propriété autorise la <xref:System.Windows.Controls.Page> ne pas avoir connaissance explicite du type de fenêtre qui l’héberge.  
  
> [!NOTE]
>  Pour définir la largeur d’une fenêtre <xref:System.Windows.Controls.Page.WindowWidth%2A>, un <xref:System.Windows.Controls.Page> doit être l’enfant d’une fenêtre.  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowWidthXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowWidthPage.xaml#setpagewindowwidthxaml)]
