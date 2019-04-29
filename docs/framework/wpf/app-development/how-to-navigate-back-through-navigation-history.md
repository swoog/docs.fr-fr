---
title: 'Procédure : Revenir en arrière dans l’historique de navigation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating back
- navigation [WPF], through navigation history (back)
ms.assetid: 9343234b-d864-441d-b8a7-d895cba80a87
ms.openlocfilehash: c489a1593b3d1f22fe1ad6e648d3f8a3f7a6cd44
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947782"
---
# <a name="how-to-navigate-back-through-navigation-history"></a>Procédure : Revenir en arrière dans l’historique de navigation
Cet exemple illustre comment naviguer entrées vers l’arrière dans l’historique de navigation.  
  
## <a name="example"></a>Exemple  
 Code qui s’exécute à partir du contenu hébergé dans un <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame> à l’aide de <xref:System.Windows.Navigation.NavigationService>, ou [!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)] pouvez accéder par le biais de l’historique de navigation, une entrée à la fois.  
  
 Navigation de retour qu’une seule entrée nécessite tout d’abord vérifier qu’il existe des entrées dans l’historique de navigation arrière, en inspectant le **CanGoBack** propriété, avant de naviguer vers l’arrière une entrée, en appelant le **GoBack** méthode. Cela est illustré dans l’exemple suivant :  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 **CanGoBack** et **GoBack** sont implémentées par <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, et <xref:System.Windows.Navigation.NavigationService>.  
  
> [!NOTE]
>  Si vous appelez **GoBack**, et il y a aucune entrée dans l’historique de navigation arrière, un <xref:System.InvalidOperationException> est déclenché.
