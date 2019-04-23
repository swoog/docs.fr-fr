---
title: 'Procédure : Obtenir la valeur de retour d’une fonction de page'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- functions [WPF], getting return values of
- page functions [WPF], getting return values of
- return values of page functions [WPF]
- getting [WPF], return values of page functions
ms.assetid: 75470af6-256c-4c46-87e7-705080723a1c
ms.openlocfilehash: 054ffe16690425e118fcac481b2a5ff63f9450f2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59973302"
---
# <a name="how-to-get-the-return-value-of-a-page-function"></a><span data-ttu-id="7305a-102">Procédure : Obtenir la valeur de retour d’une fonction de page</span><span class="sxs-lookup"><span data-stu-id="7305a-102">How to: Get the Return Value of a Page Function</span></span>
<span data-ttu-id="7305a-103">Cet exemple montre comment obtenir le résultat retourné par une fonction de page.</span><span class="sxs-lookup"><span data-stu-id="7305a-103">This example shows how to get the result that is returned by a page function.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7305a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="7305a-104">Example</span></span>  
 <span data-ttu-id="7305a-105">Pour obtenir le résultat est retourné à partir d’une fonction de page, vous devez gérer <xref:System.Windows.Navigation.PageFunction%601.Return> de la fonction de page que vous appelez.</span><span class="sxs-lookup"><span data-stu-id="7305a-105">To get the result that is returned from a page function, you need to handle <xref:System.Windows.Navigation.PageFunction%601.Return> of the page function you are calling.</span></span>  
  
 [!code-xaml[HOWTOPageFunctionSnippets#CallAPageFunctionXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml#callapagefunctionxaml)]  
  
 [!code-csharp[HOWTOPageFunctionSnippets#GetPageFunctionResultCODEBEHIND](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml.cs#getpagefunctionresultcodebehind)]
 [!code-vb[HOWTOPageFunctionSnippets#GetPageFunctionResultCODEBEHIND](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/VisualBasic/CallingPage.xaml.vb#getpagefunctionresultcodebehind)]  
  
## <a name="see-also"></a><span data-ttu-id="7305a-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7305a-106">See also</span></span>

- <xref:System.Windows.Navigation.PageFunction%601>
