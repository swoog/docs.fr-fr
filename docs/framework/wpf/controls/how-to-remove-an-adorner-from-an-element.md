---
title: "Comment : supprimer un ornement d'un élément"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: 97cf4d9f-0596-429e-8526-32a30aa4ae99
ms.openlocfilehash: a3e1b08a9ec5e2cd60c063ced5e5f0d5874f8184
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33551841"
---
# <a name="how-to-remove-an-adorner-from-an-element"></a><span data-ttu-id="5af41-102">Comment : supprimer un ornement d'un élément</span><span class="sxs-lookup"><span data-stu-id="5af41-102">How to: Remove an Adorner from an Element</span></span>
<span data-ttu-id="5af41-103">Cet exemple montre comment supprimer par programme un ornement spécifique d’un <xref:System.Windows.UIElement>.</span><span class="sxs-lookup"><span data-stu-id="5af41-103">This example shows how to programmatically remove a specific adorner from a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5af41-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5af41-104">Example</span></span>  
 <span data-ttu-id="5af41-105">Cet exemple de code en clair supprime le premier ornement du tableau des ornements retourné par <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span><span class="sxs-lookup"><span data-stu-id="5af41-105">This verbose code example removes the first adorner in the array of adorners returned by <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span></span>  <span data-ttu-id="5af41-106">Cet exemple se trouve récupère les ornements d’un <xref:System.Windows.UIElement> nommé *myTextBox*.</span><span class="sxs-lookup"><span data-stu-id="5af41-106">This example happens to retrieve the adorners on a <xref:System.Windows.UIElement> named *myTextBox*.</span></span>  <span data-ttu-id="5af41-107">Si l’élément spécifié dans l’appel à <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> n’a pas d’ornements, `null` est retourné.</span><span class="sxs-lookup"><span data-stu-id="5af41-107">If the element specified in the call to <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> has no adorners, `null` is returned.</span></span>  <span data-ttu-id="5af41-108">Ce code vérifie un tableau null explicitement et est idéale pour les applications où un tableau null est censé être relativement courante.</span><span class="sxs-lookup"><span data-stu-id="5af41-108">This code explicitly checks for a null array, and is best suited for applications where a null array is expected to be relatively common.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerLong](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornerlong)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerLong](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornerlong)]  
  
## <a name="example"></a><span data-ttu-id="5af41-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="5af41-109">Example</span></span>  
 <span data-ttu-id="5af41-110">Cet exemple de code condensé est fonctionnellement équivalent à l’exemple détaillé ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="5af41-110">This condensed code example is functionally equivalent to the verbose example shown above.</span></span> <span data-ttu-id="5af41-111">Ce code ne vérifie pas explicitement un tableau null, il est donc possible qu’un <xref:System.NullReferenceException> exception peut être déclenchée.</span><span class="sxs-lookup"><span data-stu-id="5af41-111">This code does not explicitly check for a null array, so it is possible that a <xref:System.NullReferenceException> exception may be raised.</span></span>  <span data-ttu-id="5af41-112">Ce code est mieux adapté aux applications où un tableau null est supposé être rares.</span><span class="sxs-lookup"><span data-stu-id="5af41-112">This code is best suited for applications where a null array is expected to be rare.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerShort](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornershort)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerShort](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornershort)]  
  
## <a name="see-also"></a><span data-ttu-id="5af41-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5af41-113">See Also</span></span>  
 [<span data-ttu-id="5af41-114">Vue d’ensemble des ornements</span><span class="sxs-lookup"><span data-stu-id="5af41-114">Adorners Overview</span></span>](../../../../docs/framework/wpf/controls/adorners-overview.md)
