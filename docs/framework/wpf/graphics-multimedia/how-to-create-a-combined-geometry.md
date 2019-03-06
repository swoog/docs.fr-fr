---
title: 'Procédure : Créer une géométrie combinée'
ms.date: 03/30/2017
helpviewer_keywords:
- combining geometries [WPF]
- graphics [WPF], combining geometries
- geometries [WPF], combining
ms.assetid: 54c3277c-6b6e-4b25-91be-fda0bbc706b4
ms.openlocfilehash: c5ebe87abd4c2cf70f8fa17f1fcc773293f3ad27
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57364786"
---
# <a name="how-to-create-a-combined-geometry"></a><span data-ttu-id="f6e02-102">Procédure : Créer une géométrie combinée</span><span class="sxs-lookup"><span data-stu-id="f6e02-102">How to: Create a Combined Geometry</span></span>
<span data-ttu-id="f6e02-103">Cet exemple montre comment combiner des géométries.</span><span class="sxs-lookup"><span data-stu-id="f6e02-103">This example shows how to combine geometries.</span></span> <span data-ttu-id="f6e02-104">Pour combiner deux géométries, utilisez un <xref:System.Windows.Media.CombinedGeometry> objet.</span><span class="sxs-lookup"><span data-stu-id="f6e02-104">To combine two geometries, use a <xref:System.Windows.Media.CombinedGeometry> object.</span></span> <span data-ttu-id="f6e02-105">Définir son <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> propriétés avec les deux géométries à combiner, puis définissez le <xref:System.Windows.Media.CombinedGeometry.GeometryCombineMode%2A> propriété, qui détermine la façon dont les géométries seront combinées ensemble, à `Union`, `Intersect`, `Exclude`, ou `Xor`.</span><span class="sxs-lookup"><span data-stu-id="f6e02-105">Set its <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> properties  with the two geometries to combine, and set the <xref:System.Windows.Media.CombinedGeometry.GeometryCombineMode%2A> property, which determines how the geometries will be combined together, to `Union`, `Intersect`, `Exclude`, or `Xor`.</span></span>  
  
 <span data-ttu-id="f6e02-106">Pour créer une géométrie composite à partir de deux ou plusieurs des géométries, utilisez un <xref:System.Windows.Media.GeometryGroup>.</span><span class="sxs-lookup"><span data-stu-id="f6e02-106">To create a composite geometry from two or more geometries, use a <xref:System.Windows.Media.GeometryGroup>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f6e02-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="f6e02-107">Example</span></span>  
 <span data-ttu-id="f6e02-108">Dans l’exemple suivant, un <xref:System.Windows.Media.CombinedGeometry> est défini avec un mode de géométrie combinée `Exclude`.</span><span class="sxs-lookup"><span data-stu-id="f6e02-108">In the following example, a <xref:System.Windows.Media.CombinedGeometry> is defined with a geometry combine mode of `Exclude`.</span></span>  <span data-ttu-id="f6e02-109">Les deux <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> sont définies comme des cercles de même rayon mais avec le décalage des centres par 50.</span><span class="sxs-lookup"><span data-stu-id="f6e02-109">Both <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and the <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> are defined as circles of the same radius, but with centers offset by 50.</span></span>  
  
 [!code-xaml[GeometrySample#21](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#21)]  
  
 <span data-ttu-id="f6e02-110">![Mode de combinaison de résultats de l’exclusion](./media/mil-task-combined-geometry-exclude.PNG "mil_task_combined_geometry_exclude")</span><span class="sxs-lookup"><span data-stu-id="f6e02-110">![Results of the Exclude combine mode](./media/mil-task-combined-geometry-exclude.PNG "mil_task_combined_geometry_exclude")</span></span>  
<span data-ttu-id="f6e02-111">Exclusion de la géométrie combinée</span><span class="sxs-lookup"><span data-stu-id="f6e02-111">Combined Geometry Exclude</span></span>  
  
 <span data-ttu-id="f6e02-112">Dans le balisage suivant, un <xref:System.Windows.Media.CombinedGeometry> est défini avec un mode d’association `Intersect`.</span><span class="sxs-lookup"><span data-stu-id="f6e02-112">In the following markup, a <xref:System.Windows.Media.CombinedGeometry> is defined with a combine mode of `Intersect`.</span></span>  <span data-ttu-id="f6e02-113">Les deux <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> sont définies comme des cercles de même rayon mais avec le décalage des centres par 50.</span><span class="sxs-lookup"><span data-stu-id="f6e02-113">Both <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and the <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> are defined as circles of the same radius, but with centers offset by 50.</span></span>  
  
 [!code-xaml[GeometrySample#22](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#22)]  
  
 <span data-ttu-id="f6e02-114">![Mode de combinaison de résultats de l’intersection](./media/mil-task-combined-geometry-intersect.PNG "mil_task_combined_geometry_intersect")</span><span class="sxs-lookup"><span data-stu-id="f6e02-114">![Results of the Intersect combine mode](./media/mil-task-combined-geometry-intersect.PNG "mil_task_combined_geometry_intersect")</span></span>  
<span data-ttu-id="f6e02-115">Géométrie combinée Intersect</span><span class="sxs-lookup"><span data-stu-id="f6e02-115">Combined Geometry Intersect</span></span>  
  
 <span data-ttu-id="f6e02-116">Dans le balisage suivant, un <xref:System.Windows.Media.CombinedGeometry> est défini avec un mode d’association `Union`.</span><span class="sxs-lookup"><span data-stu-id="f6e02-116">In the following markup, a <xref:System.Windows.Media.CombinedGeometry> is defined with a combine mode of `Union`.</span></span>  <span data-ttu-id="f6e02-117">Les deux <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> sont définies comme des cercles de même rayon mais avec le décalage des centres par 50.</span><span class="sxs-lookup"><span data-stu-id="f6e02-117">Both <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and the <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> are defined as circles of the same radius, but with centers offset by 50.</span></span>  
  
 [!code-xaml[GeometrySample#23](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#23)]  
  
 <span data-ttu-id="f6e02-118">![Résultats du mode d’association Union](./media/mil-task-combined-geometry-union.PNG "mil_task_combined_geometry_union")</span><span class="sxs-lookup"><span data-stu-id="f6e02-118">![Results of the Union combine mode](./media/mil-task-combined-geometry-union.PNG "mil_task_combined_geometry_union")</span></span>  
<span data-ttu-id="f6e02-119">Géométrie combinée Union</span><span class="sxs-lookup"><span data-stu-id="f6e02-119">Combined Geometry Union</span></span>  
  
 <span data-ttu-id="f6e02-120">Dans le balisage suivant, un <xref:System.Windows.Media.CombinedGeometry> est défini avec un mode d’association `Xor`.</span><span class="sxs-lookup"><span data-stu-id="f6e02-120">In the following markup, a <xref:System.Windows.Media.CombinedGeometry> is defined with a combine mode of `Xor`.</span></span>  <span data-ttu-id="f6e02-121">Les deux <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> et <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> sont définies comme des cercles de même rayon mais avec le décalage des centres par 50.</span><span class="sxs-lookup"><span data-stu-id="f6e02-121">Both <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and the <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> are defined as circles of the same radius, but with centers offset by 50.</span></span>  
  
 [!code-xaml[GeometrySample#24](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#24)]  
  
 <span data-ttu-id="f6e02-122">![Résultats du mode d’association Xor](./media/mil-task-combined-geometry-xor.PNG "mil_task_combined_geometry_xor")</span><span class="sxs-lookup"><span data-stu-id="f6e02-122">![Results of the Xor combine mode](./media/mil-task-combined-geometry-xor.PNG "mil_task_combined_geometry_xor")</span></span>  
<span data-ttu-id="f6e02-123">Géométrie combinée Xor</span><span class="sxs-lookup"><span data-stu-id="f6e02-123">Combined Geometry Xor</span></span>
