---
title: 'Procédure : Faire pivoter un objet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rotating objects [WPF]
- rotating objects [WPF]
ms.assetid: ee3466cd-e66f-4e8f-8a5a-71d77bc1e390
ms.openlocfilehash: 49de419f22980ab9101c388079e0348b4c1113f4
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57360366"
---
# <a name="how-to-rotate-an-object"></a><span data-ttu-id="91243-102">Procédure : Faire pivoter un objet</span><span class="sxs-lookup"><span data-stu-id="91243-102">How to: Rotate an Object</span></span>
<span data-ttu-id="91243-103">Cet exemple montre comment faire pivoter un objet.</span><span class="sxs-lookup"><span data-stu-id="91243-103">This example shows how to rotate an object.</span></span> <span data-ttu-id="91243-104">L’exemple crée d’abord un <xref:System.Windows.Media.RotateTransform> puis spécifie sa <xref:System.Windows.Media.RotateTransform.Angle%2A> en degrés.</span><span class="sxs-lookup"><span data-stu-id="91243-104">The example first creates a <xref:System.Windows.Media.RotateTransform> and then specifies its <xref:System.Windows.Media.RotateTransform.Angle%2A> in degrees.</span></span>  
  
 <span data-ttu-id="91243-105">L’exemple suivant fait pivoter un <xref:System.Windows.Shapes.Polyline> 45 degrés autour de son coin supérieur gauche de l’objet.</span><span class="sxs-lookup"><span data-stu-id="91243-105">The following example rotates a <xref:System.Windows.Shapes.Polyline> object 45 degrees about its upper-left corner.</span></span>  
  
## <a name="example"></a><span data-ttu-id="91243-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="91243-106">Example</span></span>  
 [!code-xaml[Transforms_snip#RotatePolylineAboutTopLeft](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineabouttopleft)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineabouttopleft)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineabouttopleft)]  
  
 <span data-ttu-id="91243-107">Le <xref:System.Windows.Media.RotateTransform.CenterX%2A> et <xref:System.Windows.Media.RotateTransform.CenterY%2A> propriétés de la <xref:System.Windows.Media.RotateTransform> spécifier le point sur lequel l’objet est pivoté.</span><span class="sxs-lookup"><span data-stu-id="91243-107">The <xref:System.Windows.Media.RotateTransform.CenterX%2A> and <xref:System.Windows.Media.RotateTransform.CenterY%2A> properties of the <xref:System.Windows.Media.RotateTransform> specify the point about which the object is rotated.</span></span> <span data-ttu-id="91243-108">Ce point central est exprimé dans l’espace de coordonnées de l’élément transformé.</span><span class="sxs-lookup"><span data-stu-id="91243-108">This center point is expressed in the coordinate space of the element that is transformed.</span></span> <span data-ttu-id="91243-109">Par défaut, la rotation est appliquée à (0,0), qui correspond à l’angle supérieur gauche de l’objet à transformer.</span><span class="sxs-lookup"><span data-stu-id="91243-109">By default, the rotation is applied to (0,0), which is the upper-left corner of the object to transform.</span></span>  
  
 <span data-ttu-id="91243-110">L’exemple suivant fait pivoter un <xref:System.Windows.Shapes.Polyline> de l’objet dans le sens horaire 45 degrés autour du point (25,50).</span><span class="sxs-lookup"><span data-stu-id="91243-110">The next example rotates a <xref:System.Windows.Shapes.Polyline> object clockwise 45 degrees about the point (25,50).</span></span>  
  
 [!code-xaml[Transforms_snip#RotatePolylineAboutCenter](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineaboutcenter)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutCenter](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineaboutcenter)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutCenter](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineaboutcenter)]  
  
 <span data-ttu-id="91243-111">L’illustration suivante montre les résultats de l’application un <xref:System.Windows.Media.Transform> aux deux objets.</span><span class="sxs-lookup"><span data-stu-id="91243-111">The following illustration shows the results of applying a <xref:System.Windows.Media.Transform> to the two objects.</span></span>  
  
 <span data-ttu-id="91243-112">![rotations de 45 degrés par rapport à différents points centraux](./media/wcpsdk-graphicsmm-rotatetransform45degrees.gif "wcpsdk_graphicsmm_rotatetransform45degrees")</span><span class="sxs-lookup"><span data-stu-id="91243-112">![45 degree rotations with different center points](./media/wcpsdk-graphicsmm-rotatetransform45degrees.gif "wcpsdk_graphicsmm_rotatetransform45degrees")</span></span>  
<span data-ttu-id="91243-113">Deux objets en rotation de 45 degrés à partir de différents centres de rotation</span><span class="sxs-lookup"><span data-stu-id="91243-113">Two objects that rotate 45 degrees from different rotational centers</span></span>  
  
 <span data-ttu-id="91243-114">Le <xref:System.Windows.Shapes.Polyline> dans les exemples précédents est un <xref:System.Windows.UIElement>.</span><span class="sxs-lookup"><span data-stu-id="91243-114">The <xref:System.Windows.Shapes.Polyline> in the previous examples is a <xref:System.Windows.UIElement>.</span></span> <span data-ttu-id="91243-115">Lorsque vous appliquez un <xref:System.Windows.Media.Transform> à la <xref:System.Windows.UIElement.RenderTransform%2A> propriété d’un <xref:System.Windows.UIElement>, vous pouvez utiliser la <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété pour spécifier une origine pour chaque <xref:System.Windows.Media.Transform> que vous appliquez à l’élément.</span><span class="sxs-lookup"><span data-stu-id="91243-115">When you apply a <xref:System.Windows.Media.Transform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of a <xref:System.Windows.UIElement>, you can use the <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property to specify an origin for every <xref:System.Windows.Media.Transform> that you apply to the element.</span></span> <span data-ttu-id="91243-116">Étant donné que le <xref:System.Windows.UIElement.RenderTransformOrigin%2A> propriété utilise des coordonnées relatives, vous pouvez appliquer une transformation au centre de l’élément, même si vous ne connaissez pas sa taille.</span><span class="sxs-lookup"><span data-stu-id="91243-116">Because the <xref:System.Windows.UIElement.RenderTransformOrigin%2A> property uses relative coordinates, you can apply a transformation to the center of the element even if you do not know its size.</span></span> <span data-ttu-id="91243-117">Pour plus d’informations et pour obtenir un exemple, consultez [spécifier l’origine d’une transformation à l’aide des valeurs relatives](how-to-specify-the-origin-of-a-transform-by-using-relative-values.md).</span><span class="sxs-lookup"><span data-stu-id="91243-117">For more information and for an example, see [Specify the Origin of a Transform by Using Relative Values](how-to-specify-the-origin-of-a-transform-by-using-relative-values.md).</span></span>  
  
 <span data-ttu-id="91243-118">Pour voir l’exemple complet, consultez la page [2-D Transforms Sample](https://go.microsoft.com/fwlink/?LinkID=158252) (Exemple de transformations 2D).</span><span class="sxs-lookup"><span data-stu-id="91243-118">For the complete sample, see [2-D Transforms Sample](https://go.microsoft.com/fwlink/?LinkID=158252).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91243-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91243-119">See also</span></span>
- <xref:System.Windows.Media.Transform>
- [<span data-ttu-id="91243-120">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="91243-120">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="91243-121">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="91243-121">How-to Topics</span></span>](transformations-how-to-topics.md)
