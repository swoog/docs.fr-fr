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
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2018
ms.locfileid: "44367912"
---
# <a name="how-to-navigate-back-through-navigation-history"></a><span data-ttu-id="bb8de-102">Comment : naviguer par le biais de l’historique de Navigation</span><span class="sxs-lookup"><span data-stu-id="bb8de-102">How to: Navigate Back Through Navigation History</span></span>
<span data-ttu-id="bb8de-103">Cet exemple illustre comment naviguer entrées vers l’arrière dans l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="bb8de-103">This example illustrates how to navigate to entries in back navigation history.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bb8de-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="bb8de-104">Example</span></span>  
 <span data-ttu-id="bb8de-105">Code qui s’exécute à partir du contenu hébergé dans un <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame> à l’aide de <xref:System.Windows.Navigation.NavigationService>, ou [!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)] pouvez accéder par le biais de l’historique de navigation, une entrée à la fois.</span><span class="sxs-lookup"><span data-stu-id="bb8de-105">Code that is running from content that is hosted in a <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame> using <xref:System.Windows.Navigation.NavigationService>, or [!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)] can navigate back through navigation history, one entry at a time.</span></span>  
  
 <span data-ttu-id="bb8de-106">Navigation de retour qu’une seule entrée nécessite tout d’abord vérifier qu’il existe des entrées dans l’historique de navigation arrière, en inspectant le **CanGoBack** propriété, avant de naviguer vers l’arrière une entrée, en appelant le **GoBack** méthode.</span><span class="sxs-lookup"><span data-stu-id="bb8de-106">Navigating back one entry requires first checking that there are entries in back navigation history, by inspecting the **CanGoBack** property, before navigating back one entry, by calling the **GoBack** method.</span></span> <span data-ttu-id="bb8de-107">Cela est illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="bb8de-107">This is illustrated in the following example:</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 <span data-ttu-id="bb8de-108">**CanGoBack** et **GoBack** sont implémentées par <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, et <xref:System.Windows.Navigation.NavigationService>.</span><span class="sxs-lookup"><span data-stu-id="bb8de-108">**CanGoBack** and **GoBack** are implemented by <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, and <xref:System.Windows.Navigation.NavigationService>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bb8de-109">Si vous appelez **GoBack**, et il y a aucune entrée dans l’historique de navigation arrière, un <xref:System.InvalidOperationException> est déclenché.</span><span class="sxs-lookup"><span data-stu-id="bb8de-109">If you call **GoBack**, and there are no entries in back navigation history, an <xref:System.InvalidOperationException> is raised.</span></span>
