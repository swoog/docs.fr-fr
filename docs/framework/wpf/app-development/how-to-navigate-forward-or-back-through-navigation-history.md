---
title: 'Procédure : Naviguer en avant ou en arrière dans l’historique de navigation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating forward
- navigation [WPF], through navigation history (forward)
ms.assetid: 5939d574-5f53-469e-85f5-1f2b13607caa
ms.openlocfilehash: 4c20ebfab45a24cf34b1476fb94dae6913fb4d99
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947756"
---
# <a name="how-to-navigate-forward-or-back-through-navigation-history"></a>Procédure : Naviguer en avant ou en arrière dans l’historique de navigation
Cet exemple illustre comment naviguer vers l’avant ou arrière à des entrées de l’historique de navigation.  
  
## <a name="example"></a>Exemple  
 Code qui s’exécute à partir du contenu dans les hôtes suivants peut naviguer vers l’avant ou arrière dans l’historique de navigation, une entrée à la fois.  
  
- <xref:System.Windows.Navigation.NavigationWindow> À l’aide de <xref:System.Windows.Navigation.NavigationService>  
  
- <xref:System.Windows.Controls.Frame> À l’aide de <xref:System.Windows.Navigation.NavigationService>  
  
- [!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)]  
  
 Avant que vous pouvez naviguer vers l’avant qu’une seule entrée, vous devez tout d’abord vérifier qu’il existe des entrées dans l’historique de navigation en inspectant le **CanGoForward** propriété. Pour naviguer vers l’avant qu’une seule entrée, vous appelez le **GoForward** (méthode). Cela est illustré dans l’exemple suivant :  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateForwardCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigateforwardcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateForwardCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigateforwardcode)]  
  
 Avant que vous puissiez naviguer arrière d’une entrée, vous devez tout d’abord vérifier qu’il existe des entrées dans l’historique de navigation arrière en inspectant le **CanGoBack** propriété. Pour accéder à l’entrée du précédent, vous appelez le **GoBack** (méthode). Cela est illustré dans l’exemple suivant :  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 **CanGoForward**, **GoForward**, **CanGoBack**, et **GoBack** sont implémentées par <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, et <xref:System.Windows.Navigation.NavigationService>.  
  
> [!NOTE]
>  Si vous appelez **GoForward**, et il y a aucune entrée dans l’historique de navigation, ou si vous appelez **GoBack**, et il y a aucune entrée dans l’historique de navigation arrière, un <xref:System.InvalidOperationException> est levée.
