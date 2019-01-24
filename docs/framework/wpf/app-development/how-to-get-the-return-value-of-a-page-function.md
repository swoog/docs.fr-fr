---
title: "Procédure : Obtenir la valeur de retour d'une fonction de page"
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
ms.openlocfilehash: 8ac1b59330790432ac29edd63a37db44283ba542
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54724211"
---
# <a name="how-to-get-the-return-value-of-a-page-function"></a>Procédure : Obtenir la valeur de retour d'une fonction de page
Cet exemple montre comment obtenir le résultat retourné par une fonction de page.  
  
## <a name="example"></a>Exemple  
 Pour obtenir le résultat est retourné à partir d’une fonction de page, vous devez gérer <xref:System.Windows.Navigation.PageFunction%601.Return> de la fonction de page que vous appelez.  
  
 [!code-xaml[HOWTOPageFunctionSnippets#CallAPageFunctionXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml#callapagefunctionxaml)]  
  
 [!code-csharp[HOWTOPageFunctionSnippets#GetPageFunctionResultCODEBEHIND](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml.cs#getpagefunctionresultcodebehind)]
 [!code-vb[HOWTOPageFunctionSnippets#GetPageFunctionResultCODEBEHIND](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/VisualBasic/CallingPage.xaml.vb#getpagefunctionresultcodebehind)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Navigation.PageFunction%601>
