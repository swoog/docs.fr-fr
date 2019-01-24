---
title: "Procédure : Supprimer tous les ornements d'un élément"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: fe5303a3-b76e-4643-aafb-51419032b47b
ms.openlocfilehash: 310b0249c215801b2634d51a1a1117bd7df83526
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680186"
---
# <a name="how-to-remove-all-adorners-from-an-element"></a><span data-ttu-id="ce383-102">Procédure : Supprimer tous les ornements d'un élément</span><span class="sxs-lookup"><span data-stu-id="ce383-102">How to: Remove all Adorners from an Element</span></span>
<span data-ttu-id="ce383-103">Cet exemple montre comment supprimer par programme tous les ornements d’un <xref:System.Windows.UIElement>.</span><span class="sxs-lookup"><span data-stu-id="ce383-103">This example shows how to programmatically remove all adorners from a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ce383-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="ce383-104">Example</span></span>  
 <span data-ttu-id="ce383-105">Cet exemple de code en clair supprime tous les ornements dans le tableau des ornements retourné par <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span><span class="sxs-lookup"><span data-stu-id="ce383-105">This verbose code example removes all of the adorners in the array of adorners returned by <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span></span>  <span data-ttu-id="ce383-106">Cet exemple se produit pour récupérer les ornements sur un <xref:System.Windows.UIElement> nommé *myTextBox*.</span><span class="sxs-lookup"><span data-stu-id="ce383-106">This example happens to retrieve the adorners on a <xref:System.Windows.UIElement> named *myTextBox*.</span></span>  <span data-ttu-id="ce383-107">Si l’élément spécifié dans l’appel à <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> a pas d’ornements, `null` est retournée.</span><span class="sxs-lookup"><span data-stu-id="ce383-107">If the element specified in the call to <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> has no adorners, `null` is returned.</span></span>  <span data-ttu-id="ce383-108">Ce code vérifie un tableau null explicitement et est mieux adapté aux applications où un tableau null est censé être relativement courante.</span><span class="sxs-lookup"><span data-stu-id="ce383-108">This code explicitly checks for a null array, and is best suited for applications where a null array is expected to be relatively common.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersLong](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornerslong)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersLong](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornerslong)]  
  
## <a name="example"></a><span data-ttu-id="ce383-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="ce383-109">Example</span></span>  
 <span data-ttu-id="ce383-110">Cet exemple de code condensé est fonctionnellement équivalent à l’exemple détaillé ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ce383-110">This condensed code example is functionally equivalent to the verbose example shown above.</span></span> <span data-ttu-id="ce383-111">Ce code ne vérifie pas explicitement un tableau null, il est donc possible qu’un <xref:System.NullReferenceException> exception peut être déclenchée.</span><span class="sxs-lookup"><span data-stu-id="ce383-111">This code does not explicitly check for a null array, so it is possible that a <xref:System.NullReferenceException> exception may be raised.</span></span>  <span data-ttu-id="ce383-112">Ce code est mieux adapté aux applications où un tableau null est censé être rares.</span><span class="sxs-lookup"><span data-stu-id="ce383-112">This code is best suited for applications where a null array is expected to be rare.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersShort](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornersshort)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersShort](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornersshort)]  
  
## <a name="see-also"></a><span data-ttu-id="ce383-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce383-113">See also</span></span>
- [<span data-ttu-id="ce383-114">Vue d’ensemble des ornements</span><span class="sxs-lookup"><span data-stu-id="ce383-114">Adorners Overview</span></span>](../../../../docs/framework/wpf/controls/adorners-overview.md)
