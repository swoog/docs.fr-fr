---
title: 'Procédure : faire pivoter des couleurs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], rotating
- examples [Windows Forms], rotating colors
ms.assetid: e2e4c300-159c-4f4a-9b56-103b0f7cbc05
ms.openlocfilehash: 241d2824fc2d87a0505eb6e790c865bfa7d8ef90
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59175537"
---
# <a name="how-to-rotate-colors"></a><span data-ttu-id="0791a-102">Procédure : faire pivoter des couleurs</span><span class="sxs-lookup"><span data-stu-id="0791a-102">How to: Rotate Colors</span></span>
<span data-ttu-id="0791a-103">Rotation dans un espace de couleurs à quatre dimensions est difficile à visualiser.</span><span class="sxs-lookup"><span data-stu-id="0791a-103">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="0791a-104">Nous pouvons facilitent la visualisation, choisissez de conserver un seul des composants de couleur fixe.</span><span class="sxs-lookup"><span data-stu-id="0791a-104">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="0791a-105">Supposons que nous mettre d’accord conserver le composant alpha fixé à 1 (totalement opaque).</span><span class="sxs-lookup"><span data-stu-id="0791a-105">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="0791a-106">Vous pouvez ensuite visualiser un espace de couleurs à trois dimensions avec des axes rouges, vert et bleus, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="0791a-106">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>  
  
 ![Illustration des rotation avec les axes de rouges, vert et bleus.](./media/how-to-rotate-colors/rotation-red-green-blue-axes.gif)  
  
 <span data-ttu-id="0791a-108">Une couleur peut être considérée comme un point dans l’espace 3D.</span><span class="sxs-lookup"><span data-stu-id="0791a-108">A color can be thought of as a point in 3-D space.</span></span> <span data-ttu-id="0791a-109">Par exemple, le point (1, 0, 0) dans l’espace représente la couleur rouge, et le point (0, 1, 0) dans l’espace représente la couleur verte.</span><span class="sxs-lookup"><span data-stu-id="0791a-109">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>  
  
 <span data-ttu-id="0791a-110">L’illustration suivante montre ce que cela signifie pour faire pivoter la couleur (1, 0, 0) via un angle de 60 degrés dans le plan rouge-vert.</span><span class="sxs-lookup"><span data-stu-id="0791a-110">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="0791a-111">Rotation d’un plan parallèle au plan rouge-vert peut être considérée comme une rotation sur l’axe bleu.</span><span class="sxs-lookup"><span data-stu-id="0791a-111">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>  
  
 ![Illustration qui montre une rotation sur l’axe bleu.](./media/how-to-rotate-colors/rotation-about-blue-axis.gif)  
  
 <span data-ttu-id="0791a-113">L’illustration suivante montre comment initialiser une matrice de couleurs pour effectuer des rotations sur chacun des trois axes de coordonnées (rouge, vert, bleu) :</span><span class="sxs-lookup"><span data-stu-id="0791a-113">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue):</span></span>  
  
 ![Initialiser une matrice de couleurs pour effectuer des rotations sur trois axes.](./media/how-to-rotate-colors/rotation-about-three-axes.gif)  
  
## <a name="example"></a><span data-ttu-id="0791a-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="0791a-115">Example</span></span>  
 <span data-ttu-id="0791a-116">L’exemple suivant prend une image qui est une couleur (1, 0, 0.6) et applique une rotation de 60 degrés autour de l’axe bleu.</span><span class="sxs-lookup"><span data-stu-id="0791a-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="0791a-117">L’angle de rotation est balayé pour passer d’un plan parallèle au plan rouge-vert.</span><span class="sxs-lookup"><span data-stu-id="0791a-117">The angle of the rotation is swept out in a plane that is parallel to the red-green plane.</span></span>  
  
 <span data-ttu-id="0791a-118">L’illustration suivante montre l’image d’origine sur la gauche et l’image pivoté de couleur sur la droite :</span><span class="sxs-lookup"><span data-stu-id="0791a-118">The following illustration shows the original image on the left and the color-rotated image on the right:</span></span>  
  
 ![Illustration qui montre l’image d’origine et image pivoté de couleur.](./media/how-to-rotate-colors/original-color-rotated-images.png)  
  
 <span data-ttu-id="0791a-120">L’illustration suivante montre une visualisation de la rotation de couleurs effectuée dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="0791a-120">The following illustration shows a visualization of the color rotation performed in the following code:</span></span>
  
 ![Illustration qui montre la visualisation de la rotation de couleur.](./media/how-to-rotate-colors/visualization-color-rotation.gif)  
  
 [!code-csharp[System.Drawing.RotateColors#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RotateColors/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.RotateColors#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RotateColors/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0791a-122">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0791a-122">Compiling the Code</span></span>  
 <span data-ttu-id="0791a-123">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0791a-123">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs>`e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="0791a-124">Remplacez `RotationInput.bmp` avec un nom de fichier d’image et le chemin d’accès valide sur votre système.</span><span class="sxs-lookup"><span data-stu-id="0791a-124">Replace `RotationInput.bmp` with an image file name and path valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0791a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0791a-125">See also</span></span>

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [<span data-ttu-id="0791a-126">Graphiques et dessins dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0791a-126">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="0791a-127">Recoloriage des images</span><span class="sxs-lookup"><span data-stu-id="0791a-127">Recoloring Images</span></span>](recoloring-images.md)
