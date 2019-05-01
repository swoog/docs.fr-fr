---
title: 'Procédure : Définir les marges des éléments et contrôles'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- setting [WPF], Margin property
- properties [WPF], Margin property
- Margin property [WPF], setting
ms.assetid: 70ebee01-6f87-4352-8dd4-402c65eaaed6
ms.openlocfilehash: 3263810806b6b4bbec15eadfd1f1da3a57d12698
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052363"
---
# <a name="how-to-set-margins-of-elements-and-controls"></a>Procédure : Définir les marges des éléments et contrôles
Cet exemple explique comment définir le <xref:System.Windows.FrameworkElement.Margin%2A> propriété, en modifiant une valeur de propriété existante de la marge dans code-behind. Le <xref:System.Windows.FrameworkElement.Margin%2A> propriété est une propriété de la <xref:System.Windows.FrameworkElement> élément de base et est donc hérité par une variété de contrôles et d’autres éléments.  
  
 Cet exemple est écrit en [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], avec un code-behind de fichiers qui le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] fait référence à. Le code-behind est illustré à la fois dans un C# et une version de Microsoft Visual Basic.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[FEMarginProgrammatic#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FEMarginProgrammatic/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[FEMarginProgrammatic#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/FEMarginProgrammatic/CSharp/default.xaml.cs#handler)]
 [!code-vb[FEMarginProgrammatic#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FEMarginProgrammatic/VisualBasic/default.xaml.vb#handler)]
