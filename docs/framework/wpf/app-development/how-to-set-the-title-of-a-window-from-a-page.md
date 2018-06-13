---
title: 'Comment : définir le titre d’une fenêtre à partir d’une Page'
ms.date: 03/30/2017
helpviewer_keywords:
- windows [WPF], setting title from a page
- title of window [WPF], setting from a page
- pages [WPF], setting window title from
ms.assetid: fecf0d19-3eb6-4f8c-a44f-ff1b6f2b34b3
ms.openlocfilehash: e69812b59783717b7b9c832d4e8ab01ab42827c8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33546183"
---
# <a name="how-to-set-the-title-of-a-window-from-a-page"></a>Comment : définir le titre d’une fenêtre à partir d’une Page
Cet exemple montre comment définir le titre de la fenêtre dans laquelle un <xref:System.Windows.Controls.Page> est hébergé.  
  
## <a name="example"></a>Exemple  
 Une page peut modifier le titre de la fenêtre qui l’héberge en définissant le <xref:System.Windows.Controls.Page.WindowTitle%2A> propriété, comme suit :  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowTitleXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowTitlePage.xaml#setpagewindowtitlexaml)]  
  
> [!NOTE]
>  Définition de la <xref:System.Windows.Controls.Page.Title%2A> propriété d’une page ne modifie pas la valeur du titre de la fenêtre. Au lieu de cela, <xref:System.Windows.Controls.Page.Title%2A> Spécifie le nom d’une entrée de page dans l’historique de navigation.
