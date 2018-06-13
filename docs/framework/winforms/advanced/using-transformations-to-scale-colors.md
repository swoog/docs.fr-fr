---
title: Utilisation de transformations pour mettre à l'échelle des couleurs
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- transformations [Windows Forms], for scaling colors
- colors [Windows Forms], scaling
ms.assetid: df23c887-7fd6-4b15-ad94-e30b5bd4b849
ms.openlocfilehash: 6cfe90cef42086672990c45c99961db3d29c3ff3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33525965"
---
# <a name="using-transformations-to-scale-colors"></a><span data-ttu-id="03939-102">Utilisation de transformations pour mettre à l'échelle des couleurs</span><span class="sxs-lookup"><span data-stu-id="03939-102">Using Transformations to Scale Colors</span></span>
<span data-ttu-id="03939-103">Une transformation d’échelle multiplie une ou plusieurs des quatre composantes de couleur par un nombre.</span><span class="sxs-lookup"><span data-stu-id="03939-103">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="03939-104">Les entrées de matrice de couleurs qui représentent la mise à l’échelle sont présentées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="03939-104">The color matrix entries that represent scaling are given in the following table.</span></span>  
  
|<span data-ttu-id="03939-105">Composant à l’échelle</span><span class="sxs-lookup"><span data-stu-id="03939-105">Component to be scaled</span></span>|<span data-ttu-id="03939-106">Entrée de la matrice</span><span class="sxs-lookup"><span data-stu-id="03939-106">Matrix entry</span></span>|  
|----------------------------|------------------|  
|<span data-ttu-id="03939-107">Rouge</span><span class="sxs-lookup"><span data-stu-id="03939-107">Red</span></span>|<span data-ttu-id="03939-108">[0][0]</span><span class="sxs-lookup"><span data-stu-id="03939-108">[0][0]</span></span>|  
|<span data-ttu-id="03939-109">Vert</span><span class="sxs-lookup"><span data-stu-id="03939-109">Green</span></span>|<span data-ttu-id="03939-110">[1][1]</span><span class="sxs-lookup"><span data-stu-id="03939-110">[1][1]</span></span>|  
|<span data-ttu-id="03939-111">Bleu</span><span class="sxs-lookup"><span data-stu-id="03939-111">Blue</span></span>|<span data-ttu-id="03939-112">[2][2]</span><span class="sxs-lookup"><span data-stu-id="03939-112">[2][2]</span></span>|  
|<span data-ttu-id="03939-113">Alpha</span><span class="sxs-lookup"><span data-stu-id="03939-113">Alpha</span></span>|<span data-ttu-id="03939-114">[3][3]</span><span class="sxs-lookup"><span data-stu-id="03939-114">[3][3]</span></span>|  
  
## <a name="scaling-one-color"></a><span data-ttu-id="03939-115">Mise à l’échelle d’une couleur</span><span class="sxs-lookup"><span data-stu-id="03939-115">Scaling One Color</span></span>  
 <span data-ttu-id="03939-116">L’exemple suivant construit une <xref:System.Drawing.Image> objet à partir du fichier ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="03939-116">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="03939-117">Ensuite, le code ajuste la composante bleue de chaque pixel dans l’image selon un facteur de 2.</span><span class="sxs-lookup"><span data-stu-id="03939-117">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="03939-118">L’image d’origine est dessinée en même temps que l’image transformée.</span><span class="sxs-lookup"><span data-stu-id="03939-118">The original image is drawn alongside the transformed image.</span></span>  
  
 [!code-csharp[System.Drawing.RecoloringImages#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.RecoloringImages#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#41)]  
  
 <span data-ttu-id="03939-119">L’illustration suivante montre l’image d’origine sur la gauche et l’image à l’échelle sur la droite.</span><span class="sxs-lookup"><span data-stu-id="03939-119">The following illustration shows the original image on the left and the scaled image on the right.</span></span>  
  
 <span data-ttu-id="03939-120">![Mettre à l’échelle de couleurs](../../../../docs/framework/winforms/advanced/media/colortrans3.png "colortrans3")</span><span class="sxs-lookup"><span data-stu-id="03939-120">![Scale Colors](../../../../docs/framework/winforms/advanced/media/colortrans3.png "colortrans3")</span></span>  
  
 <span data-ttu-id="03939-121">Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après la mise à l’échelle bleu.</span><span class="sxs-lookup"><span data-stu-id="03939-121">The following table lists the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="03939-122">Notez que la composante bleue de la quatrième barre de couleurs est passée de 0,8 à 0,6.</span><span class="sxs-lookup"><span data-stu-id="03939-122">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="03939-123">C’est parce que [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] conserve uniquement la partie fractionnaire du résultat.</span><span class="sxs-lookup"><span data-stu-id="03939-123">That is because [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] retains only the fractional part of the result.</span></span> <span data-ttu-id="03939-124">Par exemple, (2)(0.8) = 1,6 et la partie fractionnaire de 1,6 est 0,6.</span><span class="sxs-lookup"><span data-stu-id="03939-124">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="03939-125">En conservant uniquement la partie fractionnaire garantit que le résultat est toujours dans l’intervalle [0, 1].</span><span class="sxs-lookup"><span data-stu-id="03939-125">Retaining only the fractional part ensures that the result is always in the interval [0, 1].</span></span>  
  
|<span data-ttu-id="03939-126">D'origine</span><span class="sxs-lookup"><span data-stu-id="03939-126">Original</span></span>|<span data-ttu-id="03939-127">Mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="03939-127">Scaled</span></span>|  
|--------------|------------|  
|<span data-ttu-id="03939-128">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-128">(0.4, 0.4, 0.4, 1)</span></span>|<span data-ttu-id="03939-129">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-129">(0.4, 0.4, 0.8, 1)</span></span>|  
|<span data-ttu-id="03939-130">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-130">(0.4, 0.2, 0.2, 1)</span></span>|<span data-ttu-id="03939-131">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-131">(0.4, 0.2, 0.4, 1)</span></span>|  
|<span data-ttu-id="03939-132">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-132">(0.2, 0.4, 0.2, 1)</span></span>|<span data-ttu-id="03939-133">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-133">(0.2, 0.4, 0.4, 1)</span></span>|  
|<span data-ttu-id="03939-134">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-134">(0.4, 0.4, 0.8, 1)</span></span>|<span data-ttu-id="03939-135">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-135">(0.4, 0.4, 0.6, 1)</span></span>|  
  
## <a name="scaling-multiple-colors"></a><span data-ttu-id="03939-136">Mise à l’échelle de plusieurs couleurs</span><span class="sxs-lookup"><span data-stu-id="03939-136">Scaling Multiple Colors</span></span>  
 <span data-ttu-id="03939-137">L’exemple suivant construit une <xref:System.Drawing.Image> objet à partir du fichier ColorBars2.bmp.</span><span class="sxs-lookup"><span data-stu-id="03939-137">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="03939-138">Ensuite, le code ajuste les composants rouges, verts et bleus de chaque pixel de l’image.</span><span class="sxs-lookup"><span data-stu-id="03939-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="03939-139">Les composants rouges sont réduites de 25 pour cent, les composants verts à l’échelle vers le bas 35 % et les composants bleus sont réduites de 50 pour cent.</span><span class="sxs-lookup"><span data-stu-id="03939-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>  
  
 [!code-csharp[System.Drawing.RecoloringImages#42](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#42)]
 [!code-vb[System.Drawing.RecoloringImages#42](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#42)]  
  
 <span data-ttu-id="03939-140">L’illustration suivante montre l’image d’origine sur la gauche et l’image à l’échelle sur la droite.</span><span class="sxs-lookup"><span data-stu-id="03939-140">The following illustration shows the original image on the left and the scaled image on the right.</span></span>  
  
 <span data-ttu-id="03939-141">![Mettre à l’échelle de couleurs](../../../../docs/framework/winforms/advanced/media/colortrans4.png "colortrans4")</span><span class="sxs-lookup"><span data-stu-id="03939-141">![Scale Colors](../../../../docs/framework/winforms/advanced/media/colortrans4.png "colortrans4")</span></span>  
  
 <span data-ttu-id="03939-142">Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après le redimensionnement rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="03939-142">The following table lists the color vectors for the four bars before and after the red, green and blue scaling.</span></span>  
  
|<span data-ttu-id="03939-143">D'origine</span><span class="sxs-lookup"><span data-stu-id="03939-143">Original</span></span>|<span data-ttu-id="03939-144">Mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="03939-144">Scaled</span></span>|  
|--------------|------------|  
|<span data-ttu-id="03939-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-145">(0.6, 0.6, 0.6, 1)</span></span>|<span data-ttu-id="03939-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-146">(0.45, 0.39, 0.3, 1)</span></span>|  
|<span data-ttu-id="03939-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-147">(0, 1, 1, 1)</span></span>|<span data-ttu-id="03939-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-148">(0, 0.65, 0.5, 1)</span></span>|  
|<span data-ttu-id="03939-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-149">(1, 1, 0, 1)</span></span>|<span data-ttu-id="03939-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-150">(0.75, 0.65, 0, 1)</span></span>|  
|<span data-ttu-id="03939-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-151">(1, 0, 1, 1)</span></span>|<span data-ttu-id="03939-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="03939-152">(0.75, 0, 0.5, 1)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="03939-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03939-153">See Also</span></span>  
 <xref:System.Drawing.Imaging.ColorMatrix>  
 <xref:System.Drawing.Imaging.ImageAttributes>  
 [<span data-ttu-id="03939-154">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="03939-154">Graphics and Drawing in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)  
 [<span data-ttu-id="03939-155">Recoloriage des images</span><span class="sxs-lookup"><span data-stu-id="03939-155">Recoloring Images</span></span>](../../../../docs/framework/winforms/advanced/recoloring-images.md)
