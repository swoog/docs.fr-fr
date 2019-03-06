---
title: 'Procédure : Déterminer si une Page est hébergées dans un navigateur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hosted pages in browser [WPF]
- pages [WPF], hosted in browser
ms.assetid: 737e0f26-8371-49b4-9579-70879e51e1aa
ms.openlocfilehash: ebc5612f059a6cf26f2568bbc08e705b4b3014c1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57359989"
---
# <a name="how-to-determine-if-a-page-is-browser-hosted"></a>Procédure : Déterminer si une Page est hébergées dans un navigateur
Cet exemple montre comment déterminer si un <xref:System.Windows.Controls.Page> est hébergée dans un navigateur.  
  
## <a name="example"></a>Exemple  
 Un <xref:System.Windows.Controls.Page> peut être indépendante de l’hôte et, par conséquent, peut être chargé dans différents types d’hôtes, y compris un <xref:System.Windows.Controls.Frame>, un <xref:System.Windows.Navigation.NavigationWindow>, ou un navigateur. Cela peut se produire lorsque vous avez un assembly de bibliothèque qui contient une ou plusieurs pages, et qui est référencé par plusieurs autonome et peut être explorée ([!INCLUDE[TLA#tla_xbap](../../../../includes/tlasharptla-xbap-md.md)]) héberger des applications.  
  
 L’exemple suivant montre comment utiliser <xref:System.Windows.Interop.BrowserInteropHelper.IsBrowserHosted%2A?displayProperty=nameWithType> pour déterminer si un <xref:System.Windows.Controls.Page> est hébergée dans un navigateur.  
  
 [!code-csharp[HOWTOBrowserInteropHelperSnippets#IsBrowserHostedCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOBrowserInteropHelperSnippets/CSharp/Page1.xaml.cs#isbrowserhostedcode)]
 [!code-vb[HOWTOBrowserInteropHelperSnippets#IsBrowserHostedCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOBrowserInteropHelperSnippets/visualbasic/page1.xaml.vb#isbrowserhostedcode)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.Frame>
- <xref:System.Windows.Controls.Page>
