---
title: 'Comment : définir la hauteur d’une fenêtre à partir d’une Page'
ms.date: 03/30/2017
helpviewer_keywords:
- windows [WPF], setting height from a page
- pages [WPF], setting window height from
- height of window [WPF], setting from a page
ms.assetid: 4e4488ff-ab5c-4ee9-81a4-e1addb55c5cc
ms.openlocfilehash: e25bc3cf2f5de01177f79f671390bac39875d079
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33546053"
---
# <a name="how-to-set-the-height-of-a-window-from-a-page"></a>Comment : définir la hauteur d’une fenêtre à partir d’une Page
Cet exemple illustre comment définir la hauteur de la fenêtre à partir d’un <xref:System.Windows.Controls.Page>.  
  
## <a name="example"></a>Exemple  
 A <xref:System.Windows.Controls.Page> pouvez définir la hauteur de sa fenêtre hôte en définissant <xref:System.Windows.Controls.Page.WindowHeight%2A>. Cette propriété autorise le <xref:System.Windows.Controls.Page> ne pas avoir une connaissance explicite du type de fenêtre qui l’héberge.  
  
> [!NOTE]
>  Pour définir la hauteur d’une fenêtre en utilisant <xref:System.Windows.Controls.Page.WindowHeight%2A>, un <xref:System.Windows.Controls.Page> doit être l’enfant d’une fenêtre.  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowHeightXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowHeightPage.xaml#setpagewindowheightxaml)]
