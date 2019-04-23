---
title: 'Procédure : remplir une forme avec une texture d’image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], using with brushes
- bitmaps [Windows Forms], using texture
- shapes [Windows Forms], filling with images
ms.assetid: 508da5a6-2433-4d2b-9680-eaeae4e96e3b
ms.openlocfilehash: 099bc9f5359f19439f308f28a6766d470956daea
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59177318"
---
# <a name="how-to-fill-a-shape-with-an-image-texture"></a><span data-ttu-id="835e3-102">Procédure : remplir une forme avec une texture d’image</span><span class="sxs-lookup"><span data-stu-id="835e3-102">How to: Fill a Shape with an Image Texture</span></span>
<span data-ttu-id="835e3-103">Vous pouvez remplir une forme fermée avec une texture à l’aide de la <xref:System.Drawing.Image> classe et la <xref:System.Drawing.TextureBrush> classe.</span><span class="sxs-lookup"><span data-stu-id="835e3-103">You can fill a closed shape with a texture by using the <xref:System.Drawing.Image> class and the <xref:System.Drawing.TextureBrush> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="835e3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="835e3-104">Example</span></span>  
 <span data-ttu-id="835e3-105">L’exemple suivant remplit une ellipse avec une image.</span><span class="sxs-lookup"><span data-stu-id="835e3-105">The following example fills an ellipse with an image.</span></span> <span data-ttu-id="835e3-106">Le code construit une <xref:System.Drawing.Image> de l’objet et passe ensuite l’adresse de ce <xref:System.Drawing.Image> objet en tant qu’argument à un <xref:System.Drawing.TextureBrush.%23ctor%2A> constructeur.</span><span class="sxs-lookup"><span data-stu-id="835e3-106">The code constructs an <xref:System.Drawing.Image> object, and then passes the address of that <xref:System.Drawing.Image> object as an argument to a <xref:System.Drawing.TextureBrush.%23ctor%2A> constructor.</span></span> <span data-ttu-id="835e3-107">La troisième instruction met à l’échelle de l’image et la quatrième remplit l’ellipse avec les copies répétées de l’image à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="835e3-107">The third statement scales the image, and the fourth statement fills the ellipse with repeated copies of the scaled image.</span></span>  
  
 <span data-ttu-id="835e3-108">Dans le code suivant, le <xref:System.Drawing.TextureBrush.Transform%2A> propriété contient la transformation qui est appliquée à l’image avant qu’elle est dessinée.</span><span class="sxs-lookup"><span data-stu-id="835e3-108">In the following code, the <xref:System.Drawing.TextureBrush.Transform%2A> property contains the transformation that is applied to the image before it is drawn.</span></span> <span data-ttu-id="835e3-109">Supposons que l’image d’origine a une largeur de 640 pixels et une hauteur de 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="835e3-109">Assume that the original image has a width of 640 pixels and a height of 480 pixels.</span></span> <span data-ttu-id="835e3-110">La transformation réduit l’image à 75 × 75 en définissant les valeurs de mise à l’échelle horizontales et verticales.</span><span class="sxs-lookup"><span data-stu-id="835e3-110">The transform shrinks the image to 75×75 by setting the horizontal and vertical scaling values.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="835e3-111">Dans l’exemple suivant, la taille de l’image est 75 × 75 et la taille de l’ellipse est 150 × 250.</span><span class="sxs-lookup"><span data-stu-id="835e3-111">In the following example, the image size is 75×75, and the ellipse size is 150×250.</span></span> <span data-ttu-id="835e3-112">Étant donné que l’image est plus petite que l’ellipse qu’elle remplit, l’ellipse est affichée en mosaïque avec l’image.</span><span class="sxs-lookup"><span data-stu-id="835e3-112">Because the image is smaller than the ellipse it is filling, the ellipse is tiled with the image.</span></span> <span data-ttu-id="835e3-113">Signifie que l’image est répétée horizontalement et verticalement jusqu'à ce que la limite de la forme de mosaïque est atteinte.</span><span class="sxs-lookup"><span data-stu-id="835e3-113">Tiling means that the image is repeated horizontally and vertically until the boundary of the shape is reached.</span></span> <span data-ttu-id="835e3-114">Pour plus d’informations sur la mosaïque, consultez [Comment : Remplir une forme avec une Image](how-to-tile-a-shape-with-an-image.md).</span><span class="sxs-lookup"><span data-stu-id="835e3-114">For more information about tiling, see [How to: Tile a Shape with an Image](how-to-tile-a-shape-with-an-image.md).</span></span>  
  
 [!code-csharp[System.Drawing.UsingABrush#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.UsingABrush#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="835e3-115">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="835e3-115">Compiling the Code</span></span>  
 <span data-ttu-id="835e3-116">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="835e3-116">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="835e3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="835e3-117">See also</span></span>

- [<span data-ttu-id="835e3-118">Utilisation d'un pinceau pour remplir des formes</span><span class="sxs-lookup"><span data-stu-id="835e3-118">Using a Brush to Fill Shapes</span></span>](using-a-brush-to-fill-shapes.md)
