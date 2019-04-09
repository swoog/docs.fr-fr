---
title: 'Procédure : Implémenter un ornement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], implementing
ms.assetid: 56ae32b6-0599-455c-b52f-2ff97e6f1ec2
ms.openlocfilehash: da318fee42b4628351217774de2a2225cfb21ee1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59120807"
---
# <a name="how-to-implement-an-adorner"></a><span data-ttu-id="bfacf-102">Procédure : Implémenter un ornement</span><span class="sxs-lookup"><span data-stu-id="bfacf-102">How to: Implement an Adorner</span></span>
<span data-ttu-id="bfacf-103">Cet exemple montre une implémentation d’ornement minimale.</span><span class="sxs-lookup"><span data-stu-id="bfacf-103">This example shows a minimal adorner implementation.</span></span>  
  
## <a name="notes-for-implementers"></a><span data-ttu-id="bfacf-104">Notes de publication pour les implémenteurs</span><span class="sxs-lookup"><span data-stu-id="bfacf-104">Notes for Implementers</span></span>  
 <span data-ttu-id="bfacf-105">Il est important de noter que les ornements n’incluent aucun comportement de rendu inhérent ; il appartient donc à l’implémenteur d’un ornement de vérifier son rendu.</span><span class="sxs-lookup"><span data-stu-id="bfacf-105">It is important to note that adorners do not include any inherent rendering behavior; ensuring that an adorner renders is the responsibility of the adorner implementer.</span></span>   <span data-ttu-id="bfacf-106">Une façon courante d’implémentation du comportement de rendu consiste à remplacer le <xref:System.Windows.UIElement.OnRender%2A> méthode et l’utilisation d’un ou plusieurs <xref:System.Windows.Media.DrawingContext> objets pour restituer les visuels de l’ornement en fonction des besoins (comme indiqué dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="bfacf-106">A common way of implementing rendering behavior is to override the <xref:System.Windows.UIElement.OnRender%2A> method and use one or more <xref:System.Windows.Media.DrawingContext> objects to render the adorner's visuals as needed (as shown in this example).</span></span>  
  
## <a name="example"></a><span data-ttu-id="bfacf-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="bfacf-107">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="bfacf-108">Description</span><span class="sxs-lookup"><span data-stu-id="bfacf-108">Description</span></span>  
 <span data-ttu-id="bfacf-109">Un ornement personnalisé est créé en implémentant une classe qui hérite de la classe abstraite <xref:System.Windows.Documents.Adorner> classe.</span><span class="sxs-lookup"><span data-stu-id="bfacf-109">A custom adorner is created by implementing a class that inherits from the abstract <xref:System.Windows.Documents.Adorner> class.</span></span>  <span data-ttu-id="bfacf-110">L’orne simplement les angles d’un <xref:System.Windows.UIElement> avec des cercles en substituant le <xref:System.Windows.UIElement.OnRender%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="bfacf-110">The example adorner simply adorns the corners of a <xref:System.Windows.UIElement> with circles by overriding the <xref:System.Windows.UIElement.OnRender%2A> method.</span></span>  
  
### <a name="code"></a><span data-ttu-id="bfacf-111">Code</span><span class="sxs-lookup"><span data-stu-id="bfacf-111">Code</span></span>  
 [!code-csharp[Adorners_SimpleCircleAdorner#_SimpleCircleAdornerBody](~/samples/snippets/csharp/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/CSharp/Window1.xaml.cs#_simplecircleadornerbody)]
 [!code-vb[Adorners_SimpleCircleAdorner#_SimpleCircleAdornerBody](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Adorners_SimpleCircleAdorner/VisualBasic/Window1.xaml.vb#_simplecircleadornerbody)]  
  
## <a name="see-also"></a><span data-ttu-id="bfacf-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfacf-112">See also</span></span>

- [<span data-ttu-id="bfacf-113">Vue d'ensemble des ornements</span><span class="sxs-lookup"><span data-stu-id="bfacf-113">Adorners Overview</span></span>](adorners-overview.md)
