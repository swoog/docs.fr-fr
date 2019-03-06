---
title: 'Procédure : Rechercher un élément par son nom'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- elements [WPF], finding by name
ms.assetid: cfa7cf35-8aa2-4060-9454-872ed4af3f0e
ms.openlocfilehash: 7405f9ba8db5d4db0ce35ca250f13e456685f39b
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351043"
---
# <a name="how-to-find-an-element-by-its-name"></a><span data-ttu-id="38a08-102">Procédure : Rechercher un élément par son nom</span><span class="sxs-lookup"><span data-stu-id="38a08-102">How to: Find an Element by Its Name</span></span>
<span data-ttu-id="38a08-103">Cet exemple explique comment utiliser le <xref:System.Windows.FrameworkElement.FindName%2A> méthode pour rechercher un élément par son <xref:System.Windows.FrameworkElement.Name%2A> valeur.</span><span class="sxs-lookup"><span data-stu-id="38a08-103">This example describes how to use the <xref:System.Windows.FrameworkElement.FindName%2A> method to find an element by its <xref:System.Windows.FrameworkElement.Name%2A> value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="38a08-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="38a08-104">Example</span></span>  
 <span data-ttu-id="38a08-105">Dans cet exemple, la méthode à rechercher un élément particulier par son nom est écrit en tant que le Gestionnaire d’événements d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="38a08-105">In this example, the method to find a particular element by its name is written as the event handler of a button.</span></span> <span data-ttu-id="38a08-106">`stackPanel` est le <xref:System.Windows.FrameworkElement.Name%2A> de la racine <xref:System.Windows.FrameworkElement> recherché, et la méthode exemple indique ensuite visuellement l’élément trouvé en effectuant un cast en tant que <xref:System.Windows.Controls.TextBlock> et modifier l’un de le <xref:System.Windows.Controls.TextBlock> visible [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] propriétés.</span><span class="sxs-lookup"><span data-stu-id="38a08-106">`stackPanel` is the <xref:System.Windows.FrameworkElement.Name%2A> of the root <xref:System.Windows.FrameworkElement> being searched, and the example method then visually indicates the found element by casting it as <xref:System.Windows.Controls.TextBlock> and changing one of the <xref:System.Windows.Controls.TextBlock> visible [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] properties.</span></span>  
  
 [!code-csharp[FEFindName#Find](~/samples/snippets/csharp/VS_Snippets_Wpf/FEFindName/CSharp/default.xaml.cs#find)]
 [!code-vb[FEFindName#Find](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FEFindName/VisualBasic/default.xaml.vb#find)]
