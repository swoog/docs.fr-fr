---
title: 'Comment : naviguer par le biais de l’historique de Navigation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating back
- navigation [WPF], through navigation history (back)
ms.assetid: 9343234b-d864-441d-b8a7-d895cba80a87
ms.openlocfilehash: 7266c9486524e962a859c34c9be5ab8f6d7bf7d5
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2018
ms.locfileid: "46492105"
---
# <a name="how-to-navigate-back-through-navigation-history"></a>Comment : naviguer par le biais de l’historique de Navigation
Cet exemple illustre comment naviguer entrées vers l’arrière dans l’historique de navigation.  
  
## <a name="example"></a>Exemple  
 Code qui s’exécute à partir du contenu hébergé dans un <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame> à l’aide de <xref:System.Windows.Navigation.NavigationService>, ou [!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)] pouvez accéder par le biais de l’historique de navigation, une entrée à la fois.  
  
 Navigation de retour qu’une seule entrée nécessite tout d’abord vérifier qu’il existe des entrées dans l’historique de navigation arrière, en inspectant le **CanGoBack** propriété, avant de naviguer vers l’arrière une entrée, en appelant le **GoBack** méthode. Cela est illustré dans l’exemple suivant :  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 **CanGoBack** et **GoBack** sont implémentées par <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, et <xref:System.Windows.Navigation.NavigationService>.  
  
> [!NOTE]
>  Si vous appelez **GoBack**, et il y a aucune entrée dans l’historique de navigation arrière, un <xref:System.InvalidOperationException> est déclenché.
