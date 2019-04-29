---
title: 'Procédure : Obtenir toutes les fenêtres dans une application'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- window objects [WPF], getting
ms.assetid: f120f06e-993b-4a97-9657-af0d1986981f
ms.openlocfilehash: 34316f0c6f81b960a8e00131a30b9a237b9ca938
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947769"
---
# <a name="how-to-get-all-windows-in-an-application"></a>Procédure : Obtenir toutes les fenêtres dans une application
Cet exemple montre comment obtenir tous les <xref:System.Windows.Window> objets dans une application.  
  
## <a name="example"></a>Exemple  
 Chaque instancié <xref:System.Windows.Window> de l’objet, si elle est visible ou non, est automatiquement ajouté à une collection de références de fenêtre qui est géré par <xref:System.Windows.Application>et il est exposé à partir de <xref:System.Windows.Application.Windows%2A>.  
  
 Vous pouvez énumérer <xref:System.Windows.Application.Windows%2A> pour obtenir des fenêtres instanciées tout en utilisant le code suivant :  
  
 [!code-csharp[HOWTOWindowManagementSnippets#GetAllWindows](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/CustomWindow.xaml.cs#getallwindows)]
 [!code-vb[HOWTOWindowManagementSnippets#GetAllWindows](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/customwindow.xaml.vb#getallwindows)]
