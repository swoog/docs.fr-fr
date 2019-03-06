---
title: "Procédure : Transformer l'échelle d'un modèle 3D"
ms.date: 03/30/2017
helpviewer_keywords:
- scaling [WPF], 3-D objects
- 3-D objects [WPF], scaling
ms.assetid: f3fdfe33-f7dc-44b0-84a5-e43b89947f35
ms.openlocfilehash: afe18cea95be945313ef78a690c58950a3fff9b0
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57378780"
---
# <a name="how-to-transform-the-scale-of-a-3-d-model"></a><span data-ttu-id="ee1c7-102">Procédure : Transformer l'échelle d'un modèle 3D</span><span class="sxs-lookup"><span data-stu-id="ee1c7-102">How to: Transform the Scale of a 3-D Model</span></span>
<span data-ttu-id="ee1c7-103">Cet exemple montre comment mettre à l’échelle un objet 3D.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-103">This example shows how to scale a 3-D object.</span></span> <span data-ttu-id="ee1c7-104">Pour mettre à l’échelle un objet 3D, vous devez utiliser un <xref:System.Windows.Media.Media3D.ScaleTransform3D>.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-104">To scale a 3-D object, use a <xref:System.Windows.Media.Media3D.ScaleTransform3D>.</span></span> <span data-ttu-id="ee1c7-105">Le <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A>, <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A>, et <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleZ%2A> propriétés redimensionnent l’élément selon le facteur que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-105">The <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A>, <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A>, and <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleZ%2A> properties resize the element by the factor you specify.</span></span> <span data-ttu-id="ee1c7-106">Par exemple, un <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A> valeur de 1,5 étire un objet à 150 % de sa largeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-106">For example, a <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A> value of 1.5 stretches an object to 150 percent of its original width.</span></span> <span data-ttu-id="ee1c7-107">A <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A> la valeur 0,5 diminue la hauteur d’un objet de 50 %.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-107">A <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A> value of 0.5 shrinks the height of an object by 50 percent.</span></span> <span data-ttu-id="ee1c7-108">Le code ci-dessous montre à l’aide un <xref:System.Windows.Media.Media3D.ScaleTransform3D> en tant que la transformation pour un <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-108">The code below shows using a <xref:System.Windows.Media.Media3D.ScaleTransform3D> as the transform for a <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
 [!code-xaml[3DGallery_snip#ScaleTransform3DExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ScaleTransform3DExample.xaml#scaletransform3dexampleinline1)]  
  
## <a name="example"></a><span data-ttu-id="ee1c7-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="ee1c7-109">Example</span></span>  
 <span data-ttu-id="ee1c7-110">Le code suivant montre l’exemple complet.</span><span class="sxs-lookup"><span data-stu-id="ee1c7-110">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[3DGallery_snip#ScaleTransform3DExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ScaleTransform3DExample.xaml#scaletransform3dexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="ee1c7-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee1c7-111">See also</span></span>
- [<span data-ttu-id="ee1c7-112">Animer des translations 3D</span><span class="sxs-lookup"><span data-stu-id="ee1c7-112">Animate 3-D Translations</span></span>](how-to-animate-3-d-translations.md)
- [<span data-ttu-id="ee1c7-113">Créer une scène 3D</span><span class="sxs-lookup"><span data-stu-id="ee1c7-113">Create a 3-D Scene</span></span>](how-to-create-a-3-d-scene.md)
- [<span data-ttu-id="ee1c7-114">Vue d’ensemble des graphiques 3D</span><span class="sxs-lookup"><span data-stu-id="ee1c7-114">3-D Graphics Overview</span></span>](3-d-graphics-overview.md)
