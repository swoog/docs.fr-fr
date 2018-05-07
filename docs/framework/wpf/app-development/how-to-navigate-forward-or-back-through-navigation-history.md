---
title: "Comment : naviguer vers l'avant ou vers l'arrière dans l'historique de navigation"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating forward
- navigation [WPF], through navigation history (forward)
ms.assetid: 5939d574-5f53-469e-85f5-1f2b13607caa
ms.openlocfilehash: ac3b8b71b6adf04d71cf35edbb042b82c57d8e1f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-navigate-forward-or-back-through-navigation-history"></a>Comment : naviguer vers l'avant ou vers l'arrière dans l'historique de navigation
Cet exemple illustre comment naviguer vers l’avant ou vers l’arrière à des entrées de l’historique de navigation.  
  
## <a name="example"></a>Exemple  
 Code qui s’exécute à partir du contenu dans les hôtes suivants peut naviguer vers l’avant ou vers l’historique de navigation, une entrée à la fois.  
  
-   <xref:System.Windows.Navigation.NavigationWindow> À l’aide de <xref:System.Windows.Navigation.NavigationService>  
  
-   <xref:System.Windows.Controls.Frame> À l’aide de <xref:System.Windows.Navigation.NavigationService>  
  
-   [!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)]  
  
 Avant que vous pouvez naviguer vers l’avant à une entrée, vous devez tout d’abord vérifier que sont entrées dans l’historique de navigation avant en inspectant le **CanGoForward** propriété. Pour naviguer vers l’avant à une entrée, vous appelez le **GoForward** (méthode). Ceci est illustré dans l’exemple suivant :  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateForwardCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigateforwardcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateForwardCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigateforwardcode)]  
  
 Avant que vous puissiez naviguer arrière d’une entrée, vous devez tout d’abord vérifier que sont entrées dans l’historique de navigation arrière en inspectant le **CanGoBack** propriété. Pour accéder à l’arrière d’une entrée, vous appelez le **GoBack** (méthode). Ceci est illustré dans l’exemple suivant :  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 **CanGoForward**, **GoForward**, **CanGoBack**, et **GoBack** sont implémentées par <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, et <xref:System.Windows.Navigation.NavigationService>.  
  
> [!NOTE]
>  Si vous appelez **GoForward**, et il n’y aucune entrée dans l’historique de navigation avant, ou si vous appelez **GoBack**, et il n’y aucune entrée dans l’historique de navigation précédent, un <xref:System.InvalidOperationException> est levée.
