---
title: 'Procédure : Définir le titre d’une fenêtre à partir d’une page'
ms.date: 03/30/2017
helpviewer_keywords:
- windows [WPF], setting title from a page
- title of window [WPF], setting from a page
- pages [WPF], setting window title from
ms.assetid: fecf0d19-3eb6-4f8c-a44f-ff1b6f2b34b3
ms.openlocfilehash: 55444de6c61107979307b94910ba944e7001cf9e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62054001"
---
# <a name="how-to-set-the-title-of-a-window-from-a-page"></a>Procédure : Définir le titre d’une fenêtre à partir d’une page
Cet exemple montre comment définir le titre de la fenêtre dans laquelle un <xref:System.Windows.Controls.Page> est hébergé.  
  
## <a name="example"></a>Exemple  
 Une page peut modifier le titre de la fenêtre qui l’héberge en définissant le <xref:System.Windows.Controls.Page.WindowTitle%2A> propriété, comme suit :  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowTitleXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowTitlePage.xaml#setpagewindowtitlexaml)]  
  
> [!NOTE]
>  Définition de la <xref:System.Windows.Controls.Page.Title%2A> propriété d’une page ne change pas la valeur de titre de la fenêtre. Au lieu de cela, <xref:System.Windows.Controls.Page.Title%2A> Spécifie le nom d’une entrée de page dans l’historique de navigation.
