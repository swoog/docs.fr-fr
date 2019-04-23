---
title: 'Procédure : Supprimer tous les ornements d’un élément'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: fe5303a3-b76e-4643-aafb-51419032b47b
ms.openlocfilehash: 8504bb1ec70de188033b2b092bbb66cf9da3dc11
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59116792"
---
# <a name="how-to-remove-all-adorners-from-an-element"></a><span data-ttu-id="3d8a2-102">Procédure : Supprimer tous les ornements d’un élément</span><span class="sxs-lookup"><span data-stu-id="3d8a2-102">How to: Remove all Adorners from an Element</span></span>
<span data-ttu-id="3d8a2-103">Cet exemple montre comment supprimer par programme tous les ornements d’un <xref:System.Windows.UIElement>.</span><span class="sxs-lookup"><span data-stu-id="3d8a2-103">This example shows how to programmatically remove all adorners from a specified <xref:System.Windows.UIElement>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3d8a2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="3d8a2-104">Example</span></span>  
 <span data-ttu-id="3d8a2-105">Cet exemple de code en clair supprime tous les ornements dans le tableau des ornements retourné par <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span><span class="sxs-lookup"><span data-stu-id="3d8a2-105">This verbose code example removes all of the adorners in the array of adorners returned by <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A>.</span></span>  <span data-ttu-id="3d8a2-106">Cet exemple se produit pour récupérer les ornements sur un <xref:System.Windows.UIElement> nommé *myTextBox*.</span><span class="sxs-lookup"><span data-stu-id="3d8a2-106">This example happens to retrieve the adorners on a <xref:System.Windows.UIElement> named *myTextBox*.</span></span>  <span data-ttu-id="3d8a2-107">Si l’élément spécifié dans l’appel à <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> a pas d’ornements, `null` est retournée.</span><span class="sxs-lookup"><span data-stu-id="3d8a2-107">If the element specified in the call to <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> has no adorners, `null` is returned.</span></span>  <span data-ttu-id="3d8a2-108">Ce code vérifie un tableau null explicitement et est mieux adapté aux applications où un tableau null est censé être relativement courante.</span><span class="sxs-lookup"><span data-stu-id="3d8a2-108">This code explicitly checks for a null array, and is best suited for applications where a null array is expected to be relatively common.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornerslong)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornerslong)]  
  
## <a name="example"></a><span data-ttu-id="3d8a2-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="3d8a2-109">Example</span></span>  
 <span data-ttu-id="3d8a2-110">Cet exemple de code condensé est fonctionnellement équivalent à l’exemple détaillé ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="3d8a2-110">This condensed code example is functionally equivalent to the verbose example shown above.</span></span> <span data-ttu-id="3d8a2-111">Ce code ne vérifie pas explicitement un tableau null, il est donc possible qu’un <xref:System.NullReferenceException> exception peut être déclenchée.</span><span class="sxs-lookup"><span data-stu-id="3d8a2-111">This code does not explicitly check for a null array, so it is possible that a <xref:System.NullReferenceException> exception may be raised.</span></span>  <span data-ttu-id="3d8a2-112">Ce code est mieux adapté aux applications où un tableau null est censé être rares.</span><span class="sxs-lookup"><span data-stu-id="3d8a2-112">This code is best suited for applications where a null array is expected to be rare.</span></span>  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornersshort)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornersshort)]  
  
## <a name="see-also"></a><span data-ttu-id="3d8a2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d8a2-113">See also</span></span>

- [<span data-ttu-id="3d8a2-114">Vue d’ensemble des ornements</span><span class="sxs-lookup"><span data-stu-id="3d8a2-114">Adorners Overview</span></span>](adorners-overview.md)
