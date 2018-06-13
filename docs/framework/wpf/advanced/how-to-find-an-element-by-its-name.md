---
title: 'Comment : rechercher un élément par son nom'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- elements [WPF], finding by name
ms.assetid: cfa7cf35-8aa2-4060-9454-872ed4af3f0e
ms.openlocfilehash: e2d176c9334c0a1d4c10819e0dc9f2c408e41d5d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33543574"
---
# <a name="how-to-find-an-element-by-its-name"></a><span data-ttu-id="8092c-102">Comment : rechercher un élément par son nom</span><span class="sxs-lookup"><span data-stu-id="8092c-102">How to: Find an Element by Its Name</span></span>
<span data-ttu-id="8092c-103">Cet exemple explique comment utiliser le <xref:System.Windows.FrameworkElement.FindName%2A> méthode pour rechercher un élément par son <xref:System.Windows.FrameworkElement.Name%2A> valeur.</span><span class="sxs-lookup"><span data-stu-id="8092c-103">This example describes how to use the <xref:System.Windows.FrameworkElement.FindName%2A> method to find an element by its <xref:System.Windows.FrameworkElement.Name%2A> value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8092c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="8092c-104">Example</span></span>  
 <span data-ttu-id="8092c-105">Dans cet exemple, la méthode à rechercher un élément particulier par son nom est écrit en tant que le Gestionnaire d’événements d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="8092c-105">In this example, the method to find a particular element by its name is written as the event handler of a button.</span></span> <span data-ttu-id="8092c-106">`stackPanel` est la <xref:System.Windows.FrameworkElement.Name%2A> de la racine de <xref:System.Windows.FrameworkElement> recherché, et la méthode d’exemple indique ensuite visuellement l’élément trouvé en effectuant un cast en tant que <xref:System.Windows.Controls.TextBlock> et modifier l’un de le <xref:System.Windows.Controls.TextBlock> visible [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] propriétés.</span><span class="sxs-lookup"><span data-stu-id="8092c-106">`stackPanel` is the <xref:System.Windows.FrameworkElement.Name%2A> of the root <xref:System.Windows.FrameworkElement> being searched, and the example method then visually indicates the found element by casting it as <xref:System.Windows.Controls.TextBlock> and changing one of the <xref:System.Windows.Controls.TextBlock> visible [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] properties.</span></span>  
  
 [!code-csharp[FEFindName#Find](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FEFindName/CSharp/default.xaml.cs#find)]
 [!code-vb[FEFindName#Find](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FEFindName/VisualBasic/default.xaml.vb#find)]
