---
title: 'Procédure : Supprimer un ornement d’un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: 97cf4d9f-0596-429e-8526-32a30aa4ae99
ms.openlocfilehash: 256dd6fa0117f88aec2ef6b60c6dcd4c33b57855
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212399"
---
# <a name="how-to-remove-an-adorner-from-an-element"></a><span data-ttu-id="653d1-102">Procédure : Supprimer un ornement d’un élément</span><span class="sxs-lookup"><span data-stu-id="653d1-102">How to: Remove an Adorner from an Element</span></span>
<span data-ttu-id="653d1-103">Cet exemple montre comment supprimer par programme un ornement spécifique à partir d’une certaine <xref:System.Windows.UIElement>.</span><span class="sxs-lookup"><span data-stu-id="653d1-103">This example shows how to programmatically remove a specific adorner from a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="653d1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="653d1-104">Example</span></span>  
 <span data-ttu-id="653d1-105">Cet exemple de code en clair supprime le premier ornement dans le tableau des ornements retourné par <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span><span class="sxs-lookup"><span data-stu-id="653d1-105">This verbose code example removes the first adorner in the array of adorners returned by <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span></span>  <span data-ttu-id="653d1-106">Cet exemple se produit pour récupérer les ornements sur un <xref:System.Windows.UIElement> nommé *myTextBox*.</span><span class="sxs-lookup"><span data-stu-id="653d1-106">This example happens to retrieve the adorners on a <xref:System.Windows.UIElement> named *myTextBox*.</span></span>  <span data-ttu-id="653d1-107">Si l’élément spécifié dans l’appel à <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> a pas d’ornements, `null` est retournée.</span><span class="sxs-lookup"><span data-stu-id="653d1-107">If the element specified in the call to <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> has no adorners, `null` is returned.</span></span>  <span data-ttu-id="653d1-108">Ce code vérifie un tableau null explicitement et est mieux adapté aux applications où un tableau null est censé être relativement courante.</span><span class="sxs-lookup"><span data-stu-id="653d1-108">This code explicitly checks for a null array, and is best suited for applications where a null array is expected to be relatively common.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornerlong)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornerlong)]  
  
## <a name="example"></a><span data-ttu-id="653d1-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="653d1-109">Example</span></span>  
 <span data-ttu-id="653d1-110">Cet exemple de code condensé est fonctionnellement équivalent à l’exemple détaillé ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="653d1-110">This condensed code example is functionally equivalent to the verbose example shown above.</span></span> <span data-ttu-id="653d1-111">Ce code ne vérifie pas explicitement un tableau null, il est donc possible qu’un <xref:System.NullReferenceException> exception peut être déclenchée.</span><span class="sxs-lookup"><span data-stu-id="653d1-111">This code does not explicitly check for a null array, so it is possible that a <xref:System.NullReferenceException> exception may be raised.</span></span>  <span data-ttu-id="653d1-112">Ce code est mieux adapté aux applications où un tableau null est censé être rares.</span><span class="sxs-lookup"><span data-stu-id="653d1-112">This code is best suited for applications where a null array is expected to be rare.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornershort)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornershort)]  
  
## <a name="see-also"></a><span data-ttu-id="653d1-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="653d1-113">See also</span></span>

- [<span data-ttu-id="653d1-114">Vue d’ensemble des ornements</span><span class="sxs-lookup"><span data-stu-id="653d1-114">Adorners Overview</span></span>](adorners-overview.md)
