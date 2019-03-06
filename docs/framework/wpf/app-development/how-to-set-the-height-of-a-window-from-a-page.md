---
title: 'Procédure : Définir la hauteur d’une fenêtre à partir d’une Page'
ms.date: 03/30/2017
helpviewer_keywords:
- windows [WPF], setting height from a page
- pages [WPF], setting window height from
- height of window [WPF], setting from a page
ms.assetid: 4e4488ff-ab5c-4ee9-81a4-e1addb55c5cc
ms.openlocfilehash: c99ea134478635f368b71443f43e4d8f772cb5aa
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57370961"
---
# <a name="how-to-set-the-height-of-a-window-from-a-page"></a>Procédure : Définir la hauteur d’une fenêtre à partir d’une Page
Cet exemple montre comment définir la hauteur de la fenêtre à partir d’un <xref:System.Windows.Controls.Page>.  
  
## <a name="example"></a>Exemple  
 Un <xref:System.Windows.Controls.Page> pouvez définir la hauteur de sa fenêtre hôte en définissant <xref:System.Windows.Controls.Page.WindowHeight%2A>. Cette propriété autorise la <xref:System.Windows.Controls.Page> ne pas avoir connaissance explicite du type de fenêtre qui l’héberge.  
  
> [!NOTE]
>  Pour définir la hauteur d’une fenêtre <xref:System.Windows.Controls.Page.WindowHeight%2A>, un <xref:System.Windows.Controls.Page> doit être l’enfant d’une fenêtre.  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowHeightXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowHeightPage.xaml#setpagewindowheightxaml)]
