---
title: "Comment : définir les marges d'éléments et de contrôles"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- setting [WPF], Margin property
- properties [WPF], Margin property
- Margin property [WPF], setting
ms.assetid: 70ebee01-6f87-4352-8dd4-402c65eaaed6
ms.openlocfilehash: 41a0f1d025061cc7c1472a831fbbd5ed2f01b043
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-set-margins-of-elements-and-controls"></a>Comment : définir les marges d'éléments et de contrôles
Cet exemple explique comment définir le <xref:System.Windows.FrameworkElement.Margin%2A> propriété, en modifiant une valeur de propriété existante de la marge dans code-behind. Le <xref:System.Windows.FrameworkElement.Margin%2A> propriété est une propriété de la <xref:System.Windows.FrameworkElement> élément de base et est par conséquent héritée par un grand nombre de contrôles et autres éléments.  
  
 Cet exemple est écrit [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], avec un code-behind du fichier qui le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] fait référence à. Le code-behind est affiché dans c# et une version de Microsoft Visual Basic.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[FEMarginProgrammatic#XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FEMarginProgrammatic/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[FEMarginProgrammatic#Handler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FEMarginProgrammatic/CSharp/default.xaml.cs#handler)]
 [!code-vb[FEMarginProgrammatic#Handler](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FEMarginProgrammatic/VisualBasic/default.xaml.vb#handler)]
