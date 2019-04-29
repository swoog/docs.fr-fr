---
title: 'Procédure : Obtenir et définir la fenêtre principale de l’application'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- windows objects [WPF], setting
- setting windows objects [WPF]
- windows objects [WPF], getting
- getting windows objects [WPF]
ms.assetid: ec902bc4-4a59-46f5-8ec1-963b46789356
ms.openlocfilehash: ea8333aa82f1159afb438215940ee1e7c2605e96
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947795"
---
# <a name="how-to-get-and-set-the-main-application-window"></a>Procédure : Obtenir et définir la fenêtre principale de l’application
Cet exemple montre comment obtenir et définir la fenêtre d’application principale.  
  
## <a name="example"></a>Exemple  
 La première <xref:System.Windows.Window> qui est instancié dans un Windows Presentation Foundation (WPF) application est définie automatiquement par <xref:System.Windows.Application> en tant que fenêtre d’application principale. La première <xref:System.Windows.Window> être instancié sera certainement la fenêtre qui est spécifiée comme le démarrage [!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)] (voir <xref:System.Windows.Application.StartupUri%2A>).  
  
 Le premier <xref:System.Windows.Window> peut également être instancié à l’aide de code. Par exemple s’ouvre une fenêtre pendant le démarrage de l’application, comme suit :  
  
 [!code-csharp[HOWTOWindowManagementSnippets#FirstWindowUsingCodeCODEBEHIND](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/App.xaml.cs#firstwindowusingcodecodebehind)]
 [!code-vb[HOWTOWindowManagementSnippets#FirstWindowUsingCodeCODEBEHIND](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/application.xaml.vb#firstwindowusingcodecodebehind)]  
  
 Parfois, le premier instancié <xref:System.Windows.Window> est en fait pas la fenêtre principale de l’application, par exemple un écran de démarrage. Dans ce cas, vous pouvez spécifier la fenêtre principale de l’application à l’aide de balisage, comme suit :  
  
 [!code-xaml[ApplicationMainWindowSnippets#SetApplicationMainWindowXAML](~/samples/snippets/xaml/VS_Snippets_Wpf/ApplicationMainWindowSnippets/XAML/App.xaml#setapplicationmainwindowxaml)]  
  
 Si la fenêtre principale est spécifiée automatiquement ou manuellement, vous pouvez obtenir la fenêtre principale à partir de <xref:System.Windows.Application.MainWindow%2A> utilisant le code suivant, comme suit :  
  
 [!code-csharp[ApplicationMainWindowSnippets#GetApplicationMainWindowCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/ApplicationMainWindowSnippets/CSharp/App.xaml.cs#getapplicationmainwindowcode)]
 [!code-vb[ApplicationMainWindowSnippets#GetApplicationMainWindowCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ApplicationMainWindowSnippets/visualbasic/application.xaml.vb#getapplicationmainwindowcode)]
