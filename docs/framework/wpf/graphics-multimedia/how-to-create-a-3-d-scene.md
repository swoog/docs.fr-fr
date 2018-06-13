---
title: 'Comment : créer une scène 3D'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- scenes [WPF], 3-D
- 3-D scenes
ms.assetid: adb4a598-71a2-4dd5-b677-ea3fc11b78b2
ms.openlocfilehash: e3c2ea803961ca57606f8ea8bec21d50a38dbe1f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559524"
---
# <a name="how-to-create-a-3-d-scene"></a><span data-ttu-id="5dc3f-102">Comment : créer une scène 3D</span><span class="sxs-lookup"><span data-stu-id="5dc3f-102">How to: Create a 3-D Scene</span></span>
<span data-ttu-id="5dc3f-103">Cet exemple montre comment créer un objet 3D qui ressemble à une feuille de papier ayant subi une rotation.</span><span class="sxs-lookup"><span data-stu-id="5dc3f-103">This example shows how to create a 3-D object that looks like a flat sheet of paper which has been rotated.</span></span> <span data-ttu-id="5dc3f-104">A <xref:System.Windows.Controls.Viewport3D> , ainsi que les composants suivants sont utilisés pour créer cette scène 3D simple :</span><span class="sxs-lookup"><span data-stu-id="5dc3f-104">A <xref:System.Windows.Controls.Viewport3D> along with the following components are used to create this simple 3-D scene:</span></span>  
  
-   <span data-ttu-id="5dc3f-105">Une caméra est créée à l’aide un <xref:System.Windows.Media.Media3D.PerspectiveCamera>.</span><span class="sxs-lookup"><span data-stu-id="5dc3f-105">A camera is created using a <xref:System.Windows.Media.Media3D.PerspectiveCamera>.</span></span> <span data-ttu-id="5dc3f-106">L’appareil photo spécifie quelle partie de la scène 3D est visible.</span><span class="sxs-lookup"><span data-stu-id="5dc3f-106">The camera specifies what part of the 3-D scene is viewable.</span></span>  
  
-   <span data-ttu-id="5dc3f-107">Un maillage est créé pour spécifier la forme de l’objet 3D (feuille de papier) à l’aide du <xref:System.Windows.Media.Media3D.GeometryModel3D.Geometry%2A> propriété du <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span><span class="sxs-lookup"><span data-stu-id="5dc3f-107">A mesh is created to specify the shape of 3-D object (sheet of paper) using the <xref:System.Windows.Media.Media3D.GeometryModel3D.Geometry%2A> property of <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
-   <span data-ttu-id="5dc3f-108">Un matériau est spécifié pour être affiché sur la surface de l’objet (dégradé linéaire dans cet exemple) en utilisant le <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> propriété du <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span><span class="sxs-lookup"><span data-stu-id="5dc3f-108">A material is specified to be displayed on the surface of the object (linear gradient in this sample) using the <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> property of <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
-   <span data-ttu-id="5dc3f-109">Un éclairage est créé pour éclairer sur l’objet à l’aide de <xref:System.Windows.Media.Media3D.DirectionalLight>.</span><span class="sxs-lookup"><span data-stu-id="5dc3f-109">A light is created to shine on the object using <xref:System.Windows.Media.Media3D.DirectionalLight>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5dc3f-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="5dc3f-110">Example</span></span>  
 <span data-ttu-id="5dc3f-111">Le code ci-dessous montre comment créer une scène 3D en XAML.</span><span class="sxs-lookup"><span data-stu-id="5dc3f-111">The code below shows how to create a 3-D scene in XAML.</span></span>  
  
 [!code-xaml[3DGallery_snip#Basic3DShapeExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/Basic3DShapeExample.xaml#basic3dshapeexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="5dc3f-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="5dc3f-112">Example</span></span>  
 <span data-ttu-id="5dc3f-113">Le code ci-dessous montre comment créer la même scène 3D en code procédural.</span><span class="sxs-lookup"><span data-stu-id="5dc3f-113">The code below shows how to create the same 3-D scene in procedural code.</span></span>  
  
 [!code-csharp[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/Basic3DShapeExample.cs#basic3dshapecodeexamplewholepage)]
 [!code-vb[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/basic3dshapeexample.vb#basic3dshapecodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="5dc3f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dc3f-114">See Also</span></span>  
 [<span data-ttu-id="5dc3f-115">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="5dc3f-115">3-D Graphics Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
