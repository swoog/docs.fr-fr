---
title: 'Procédure : Supprimer des liaisons'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bindings [WPF], clearing
- clearing bindings [WPF]
- data binding [WPF], clearing bindings
ms.assetid: 73962a93-32a9-4bcd-9240-bcfbb239093a
ms.openlocfilehash: bd0f42b868c316cb9a6344134d4aaf01930519ac
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54508429"
---
# <a name="how-to-clear-bindings"></a><span data-ttu-id="e0e8b-102">Procédure : Supprimer des liaisons</span><span class="sxs-lookup"><span data-stu-id="e0e8b-102">How to: Clear Bindings</span></span>
<span data-ttu-id="e0e8b-103">Cet exemple montre comment supprimer des liaisons d’un objet.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-103">This example shows how to clear bindings from an object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e0e8b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0e8b-104">Example</span></span>  
 <span data-ttu-id="e0e8b-105">Pour supprimer une liaison à partir d’une propriété individuelle sur un objet, appelez <xref:System.Windows.Data.BindingOperations.ClearBinding%2A> comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-105">To clear a binding from an individual property on an object, call <xref:System.Windows.Data.BindingOperations.ClearBinding%2A> as shown in the following example.</span></span> <span data-ttu-id="e0e8b-106">L’exemple suivant supprime la liaison à partir de la <xref:System.Windows.Controls.TextBlock.TextProperty> de *mytext*, un <xref:System.Windows.Controls.TextBlock> objet.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-106">The following example removes the binding from the <xref:System.Windows.Controls.TextBlock.TextProperty> of *mytext*, a <xref:System.Windows.Controls.TextBlock> object.</span></span>  
  
 [!code-csharp[CodeOnlyBinding#ClearBinding](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#clearbinding)]
 [!code-vb[CodeOnlyBinding#ClearBinding](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#clearbinding)]  
  
 <span data-ttu-id="e0e8b-107">La suppression de liaison a pour effet de supprimer la liaison de sorte que la valeur de la propriété de dépendance est modifiée pour apparaître telle qu’elle aurait été sans la liaison.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-107">Clearing the binding removes the binding so that the value of the dependency property is changed to whatever it would have been without the binding.</span></span> <span data-ttu-id="e0e8b-108">Cette valeur peut être une valeur par défaut, une valeur héritée ou une valeur dérivée d’une liaison de modèle de données.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-108">This value could be a default value, an inherited value, or a value from a data template binding.</span></span>  
  
 <span data-ttu-id="e0e8b-109">Pour effacer les liaisons à partir de toutes les propriétés possibles sur un objet, utilisez <xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A>.</span><span class="sxs-lookup"><span data-stu-id="e0e8b-109">To clear bindings from all possible properties on an object, use <xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e0e8b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0e8b-110">See also</span></span>
- <xref:System.Windows.Data.BindingOperations>
- [<span data-ttu-id="e0e8b-111">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="e0e8b-111">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [<span data-ttu-id="e0e8b-112">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="e0e8b-112">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
