---
title: Rognage et mise à l'échelle d'images dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI+, scaling images
- GDI+, cropping images
- images [Windows Forms], cropping
- compressing data [Windows Forms], images
- images [Windows Forms], expansion
- images [Windows Forms], scaling
- rectangles [Windows Forms], source
- rectangles [Windows Forms], destination
- images [Windows Forms], compression
ms.assetid: ad5daf26-005f-45bc-a2af-e0e97777a21a
ms.openlocfilehash: c3cdb06e99770808461f9266fb5f07df9074149b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59183727"
---
# <a name="cropping-and-scaling-images-in-gdi"></a><span data-ttu-id="9321a-102">Rognage et mise à l'échelle d'images dans GDI+</span><span class="sxs-lookup"><span data-stu-id="9321a-102">Cropping and Scaling Images in GDI+</span></span>
<span data-ttu-id="9321a-103">Vous pouvez utiliser la <xref:System.Drawing.Graphics.DrawImage%2A> méthode de la <xref:System.Drawing.Graphics> classe pour dessiner et positionner des images vectorielles et des images raster.</span><span class="sxs-lookup"><span data-stu-id="9321a-103">You can use the <xref:System.Drawing.Graphics.DrawImage%2A> method of the <xref:System.Drawing.Graphics> class to draw and position vector images and raster images.</span></span> <span data-ttu-id="9321a-104"><xref:System.Drawing.Graphics.DrawImage%2A> est une méthode surchargée, donc il existe plusieurs façons, vous pouvez lui fournir arguments.</span><span class="sxs-lookup"><span data-stu-id="9321a-104"><xref:System.Drawing.Graphics.DrawImage%2A> is an overloaded method, so there are several ways you can supply it with arguments.</span></span>  
  
## <a name="drawimage-variations"></a><span data-ttu-id="9321a-105">Variations de DrawImage</span><span class="sxs-lookup"><span data-stu-id="9321a-105">DrawImage Variations</span></span>  
 <span data-ttu-id="9321a-106">Une variante de la <xref:System.Drawing.Graphics.DrawImage%2A> méthode reçoit un <xref:System.Drawing.Bitmap> et un <xref:System.Drawing.Rectangle>.</span><span class="sxs-lookup"><span data-stu-id="9321a-106">One variation of the <xref:System.Drawing.Graphics.DrawImage%2A> method receives a <xref:System.Drawing.Bitmap> and a <xref:System.Drawing.Rectangle>.</span></span> <span data-ttu-id="9321a-107">Le rectangle spécifie la destination de l’opération de dessin ; Autrement dit, il spécifie le rectangle dans lequel dessiner l’image.</span><span class="sxs-lookup"><span data-stu-id="9321a-107">The rectangle specifies the destination for the drawing operation; that is, it specifies the rectangle in which to draw the image.</span></span> <span data-ttu-id="9321a-108">Si la taille du rectangle de destination est différente de la taille de l’image d’origine, l’image est étirée pour remplir le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="9321a-108">If the size of the destination rectangle is different from the size of the original image, the image is scaled to fit the destination rectangle.</span></span> <span data-ttu-id="9321a-109">L’exemple de code suivant montre comment dessiner des trois fois la même image : aucune mise à l’échelle, avec une expansion et avec une compression :</span><span class="sxs-lookup"><span data-stu-id="9321a-109">The following code example shows how to draw the same image three times: once with no scaling, once with an expansion, and once with a compression:</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#31)]  
  
 <span data-ttu-id="9321a-110">L’illustration suivante montre les trois images.</span><span class="sxs-lookup"><span data-stu-id="9321a-110">The following illustration shows the three pictures.</span></span>  
  
 <span data-ttu-id="9321a-111">![Scaling](./media/aboutgdip03-art06.gif "AboutGdip03_Art06")</span><span class="sxs-lookup"><span data-stu-id="9321a-111">![Scaling](./media/aboutgdip03-art06.gif "AboutGdip03_Art06")</span></span>  
  
 <span data-ttu-id="9321a-112">Des variantes de la <xref:System.Drawing.Graphics.DrawImage%2A> méthode ont un paramètre de rectangle source comme un rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="9321a-112">Some variations of the <xref:System.Drawing.Graphics.DrawImage%2A> method have a source-rectangle parameter as well as a destination-rectangle parameter.</span></span> <span data-ttu-id="9321a-113">Le paramètre du rectangle source Spécifie la partie de l’image d’origine à dessiner.</span><span class="sxs-lookup"><span data-stu-id="9321a-113">The source-rectangle parameter specifies the portion of the original image to draw.</span></span> <span data-ttu-id="9321a-114">Le rectangle de destination Spécifie le rectangle dans lequel dessiner la partie de l’image.</span><span class="sxs-lookup"><span data-stu-id="9321a-114">The destination rectangle specifies the rectangle in which to draw that portion of the image.</span></span> <span data-ttu-id="9321a-115">Si la taille du rectangle de destination est différente de la taille du rectangle source, l’image est étiré pour remplir le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="9321a-115">If the size of the destination rectangle is different from the size of the source rectangle, the picture is scaled to fit the destination rectangle.</span></span>  
  
 <span data-ttu-id="9321a-116">L’exemple de code suivant montre comment construire un <xref:System.Drawing.Bitmap> à partir du fichier Runner.jpg.</span><span class="sxs-lookup"><span data-stu-id="9321a-116">The following code example shows how to construct a <xref:System.Drawing.Bitmap> from the file Runner.jpg.</span></span> <span data-ttu-id="9321a-117">L’image entière est dessinée avec aucune mise à l’échelle (0, 0).</span><span class="sxs-lookup"><span data-stu-id="9321a-117">The entire image is drawn with no scaling at (0, 0).</span></span> <span data-ttu-id="9321a-118">Puis une petite partie de l’image est dessinée à deux reprises : une fois avec une compression et une fois avec une expansion.</span><span class="sxs-lookup"><span data-stu-id="9321a-118">Then a small portion of the image is drawn twice: once with a compression and once with an expansion.</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#32)]  
  
 <span data-ttu-id="9321a-119">L’illustration suivante montre l’image non ajustée et les parties de l’image réduite et agrandie.</span><span class="sxs-lookup"><span data-stu-id="9321a-119">The following illustration shows the unscaled image, and the compressed and expanded image portions.</span></span>  
  
 <span data-ttu-id="9321a-120">![Rognage et mise à l’échelle](./media/aboutgdip03-art07.gif "AboutGdip03_Art07")</span><span class="sxs-lookup"><span data-stu-id="9321a-120">![Cropping and Scaling](./media/aboutgdip03-art07.gif "AboutGdip03_Art07")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9321a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9321a-121">See also</span></span>

- [<span data-ttu-id="9321a-122">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="9321a-122">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="9321a-123">Utilisation des images, bitmaps, icônes et métafichiers</span><span class="sxs-lookup"><span data-stu-id="9321a-123">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
