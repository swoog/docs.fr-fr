---
title: "Procédure : Naviguer vers l'avant ou vers l'arrière dans l'historique de navigation"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating forward
- navigation [WPF], through navigation history (forward)
ms.assetid: 5939d574-5f53-469e-85f5-1f2b13607caa
ms.openlocfilehash: 4c20ebfab45a24cf34b1476fb94dae6913fb4d99
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57366658"
---
# <a name="how-to-navigate-forward-or-back-through-navigation-history"></a><span data-ttu-id="40476-102">Procédure : Naviguer vers l'avant ou vers l'arrière dans l'historique de navigation</span><span class="sxs-lookup"><span data-stu-id="40476-102">How to: Navigate Forward or Back Through Navigation History</span></span>
<span data-ttu-id="40476-103">Cet exemple illustre comment naviguer vers l’avant ou arrière à des entrées de l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="40476-103">This example illustrates how to navigate forward or back to entries in navigation history.</span></span>  
  
## <a name="example"></a><span data-ttu-id="40476-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="40476-104">Example</span></span>  
 <span data-ttu-id="40476-105">Code qui s’exécute à partir du contenu dans les hôtes suivants peut naviguer vers l’avant ou arrière dans l’historique de navigation, une entrée à la fois.</span><span class="sxs-lookup"><span data-stu-id="40476-105">Code that runs from content in the following hosts can navigate forward or back through navigation history, one entry at a time.</span></span>  
  
-   <span data-ttu-id="40476-106"><xref:System.Windows.Navigation.NavigationWindow> À l’aide de <xref:System.Windows.Navigation.NavigationService></span><span class="sxs-lookup"><span data-stu-id="40476-106"><xref:System.Windows.Navigation.NavigationWindow> using <xref:System.Windows.Navigation.NavigationService></span></span>  
  
-   <span data-ttu-id="40476-107"><xref:System.Windows.Controls.Frame> À l’aide de <xref:System.Windows.Navigation.NavigationService></span><span class="sxs-lookup"><span data-stu-id="40476-107"><xref:System.Windows.Controls.Frame> using <xref:System.Windows.Navigation.NavigationService></span></span>  
  
-   [!INCLUDE[TLA#tla_iegeneric](../../../../includes/tlasharptla-iegeneric-md.md)]  
  
 <span data-ttu-id="40476-108">Avant que vous pouvez naviguer vers l’avant qu’une seule entrée, vous devez tout d’abord vérifier qu’il existe des entrées dans l’historique de navigation en inspectant le **CanGoForward** propriété.</span><span class="sxs-lookup"><span data-stu-id="40476-108">Before you can navigate forward one entry, you must first check that there are entries in forward navigation history by inspecting the **CanGoForward** property.</span></span> <span data-ttu-id="40476-109">Pour naviguer vers l’avant qu’une seule entrée, vous appelez le **GoForward** (méthode).</span><span class="sxs-lookup"><span data-stu-id="40476-109">To navigate forward one entry, you call the **GoForward** method.</span></span> <span data-ttu-id="40476-110">Cela est illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="40476-110">This is illustrated in the following example:</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateForwardCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigateforwardcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateForwardCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigateforwardcode)]  
  
 <span data-ttu-id="40476-111">Avant que vous puissiez naviguer arrière d’une entrée, vous devez tout d’abord vérifier qu’il existe des entrées dans l’historique de navigation arrière en inspectant le **CanGoBack** propriété.</span><span class="sxs-lookup"><span data-stu-id="40476-111">Before you can navigate back one entry, you must first check that there are entries in back navigation history by inspecting the **CanGoBack** property.</span></span> <span data-ttu-id="40476-112">Pour accéder à l’entrée du précédent, vous appelez le **GoBack** (méthode).</span><span class="sxs-lookup"><span data-stu-id="40476-112">To navigate back one entry, you call the **GoBack** method.</span></span> <span data-ttu-id="40476-113">Cela est illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="40476-113">This is illustrated in the following example:</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 <span data-ttu-id="40476-114">**CanGoForward**, **GoForward**, **CanGoBack**, et **GoBack** sont implémentées par <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, et <xref:System.Windows.Navigation.NavigationService>.</span><span class="sxs-lookup"><span data-stu-id="40476-114">**CanGoForward**, **GoForward**, **CanGoBack**, and **GoBack** are implemented by <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, and <xref:System.Windows.Navigation.NavigationService>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="40476-115">Si vous appelez **GoForward**, et il y a aucune entrée dans l’historique de navigation, ou si vous appelez **GoBack**, et il y a aucune entrée dans l’historique de navigation arrière, un <xref:System.InvalidOperationException> est levée.</span><span class="sxs-lookup"><span data-stu-id="40476-115">If you call **GoForward**, and there are no entries in forward navigation history, or if you call **GoBack**, and there are no entries in back navigation history, an <xref:System.InvalidOperationException> is thrown.</span></span>
