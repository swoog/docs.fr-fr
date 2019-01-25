---
title: 'Procédure : Mettre un Freezable en lecture seule'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: e0cc5d73f9b9f15fc02bf20a70c84da1a7c535c9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671666"
---
# <a name="how-to-make-a-freezable-read-only"></a><span data-ttu-id="3a951-102">Procédure : Mettre un Freezable en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3a951-102">How to: Make a Freezable Read-Only</span></span>
<span data-ttu-id="3a951-103">Cet exemple montre comment rendre un <xref:System.Windows.Freezable> en lecture seule en appelant son <xref:System.Windows.Freezable.Freeze%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="3a951-103">This example shows how to make a <xref:System.Windows.Freezable> read-only by calling its <xref:System.Windows.Freezable.Freeze%2A> method.</span></span>  
  
 <span data-ttu-id="3a951-104">Vous ne pouvez pas figer un <xref:System.Windows.Freezable> objet si l’une des conditions suivantes est `true` sur l’objet :</span><span class="sxs-lookup"><span data-stu-id="3a951-104">You cannot freeze a <xref:System.Windows.Freezable> object if any one of the following conditions is `true` about the object:</span></span>  
  
-   <span data-ttu-id="3a951-105">Il a animé ou propriétés liées aux données.</span><span class="sxs-lookup"><span data-stu-id="3a951-105">It has animated or data bound properties.</span></span>  
  
-   <span data-ttu-id="3a951-106">Il possède des propriétés qui sont définies par une ressource dynamique.</span><span class="sxs-lookup"><span data-stu-id="3a951-106">It has properties that are set by a dynamic resource.</span></span> <span data-ttu-id="3a951-107">Pour plus d’informations sur les ressources dynamiques, consultez le [XAML ressources](../../../../docs/framework/wpf/advanced/xaml-resources.md).</span><span class="sxs-lookup"><span data-stu-id="3a951-107">For more information about dynamic resources, see the [XAML Resources](../../../../docs/framework/wpf/advanced/xaml-resources.md).</span></span>  
  
-   <span data-ttu-id="3a951-108">Il contient <xref:System.Windows.Freezable> sous-objets qui ne peut pas être figés.</span><span class="sxs-lookup"><span data-stu-id="3a951-108">It contains <xref:System.Windows.Freezable> sub-objects that cannot be frozen.</span></span>  
  
 <span data-ttu-id="3a951-109">Si ces conditions sont `false` pour votre <xref:System.Windows.Freezable> objet et que vous ne souhaitez pas modifier, envisagez de geler pour profiter des avantages de performances.</span><span class="sxs-lookup"><span data-stu-id="3a951-109">If these conditions are `false` for your <xref:System.Windows.Freezable> object and you do not intend to modify it, consider freezing it to gain performance benefits.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3a951-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a951-110">Example</span></span>  
 <span data-ttu-id="3a951-111">L’exemple suivant se fige un <xref:System.Windows.Media.SolidColorBrush>, qui est un type de <xref:System.Windows.Freezable> objet.</span><span class="sxs-lookup"><span data-stu-id="3a951-111">The following example freezes a <xref:System.Windows.Media.SolidColorBrush>, which is a type of <xref:System.Windows.Freezable> object.</span></span>  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 <span data-ttu-id="3a951-112">Pour plus d’informations sur <xref:System.Windows.Freezable> , voir la [vue d’ensemble des objets Freezable](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3a951-112">For more information about <xref:System.Windows.Freezable> objects, see the [Freezable Objects Overview](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a951-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a951-113">See also</span></span>
- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CanFreeze%2A>
- <xref:System.Windows.Freezable.Freeze%2A>
- [<span data-ttu-id="3a951-114">Vue d’ensemble des objets Freezable</span><span class="sxs-lookup"><span data-stu-id="3a951-114">Freezable Objects Overview</span></span>](../../../../docs/framework/wpf/advanced/freezable-objects-overview.md)
- [<span data-ttu-id="3a951-115">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="3a951-115">How-to Topics</span></span>](../../../../docs/framework/wpf/advanced/base-elements-how-to-topics.md)
