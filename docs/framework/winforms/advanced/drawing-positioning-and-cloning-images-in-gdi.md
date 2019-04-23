---
title: Dessin, positionnement et clonage d'images dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- raster images [Windows Forms]
- images [Windows Forms], positioning
- drawing [Windows Forms], images
- drawing [Windows Forms], raster images
- images [Windows Forms], cloning
- images [Windows Forms], drawing
- GDI+, drawing images
- GDI+, cloning images
- GDI+, positioning images
ms.assetid: 09f0c07a-19c0-43b4-90a2-862a10545ce8
ms.openlocfilehash: b5f98e7bdef9ff8ed0a4cd0e040cb92a31f30503
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59188446"
---
# <a name="drawing-positioning-and-cloning-images-in-gdi"></a><span data-ttu-id="67d55-102">Dessin, positionnement et clonage d'images dans GDI+</span><span class="sxs-lookup"><span data-stu-id="67d55-102">Drawing, Positioning, and Cloning Images in GDI+</span></span>
<span data-ttu-id="67d55-103">Vous pouvez utiliser la <xref:System.Drawing.Bitmap> classe pour charger et afficher des images raster et vous pouvez utiliser la <xref:System.Drawing.Imaging.Metafile> classe pour charger et afficher des images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="67d55-103">You can use the <xref:System.Drawing.Bitmap> class to load and display raster images, and you can use the <xref:System.Drawing.Imaging.Metafile> class to load and display vector images.</span></span> <span data-ttu-id="67d55-104">Le <xref:System.Drawing.Bitmap> et <xref:System.Drawing.Imaging.Metafile> classes héritent de la <xref:System.Drawing.Image> classe.</span><span class="sxs-lookup"><span data-stu-id="67d55-104">The <xref:System.Drawing.Bitmap> and <xref:System.Drawing.Imaging.Metafile> classes inherit from the <xref:System.Drawing.Image> class.</span></span> <span data-ttu-id="67d55-105">Pour afficher une image vectorielle, vous avez besoin d’une instance de la <xref:System.Drawing.Graphics> classe et un <xref:System.Drawing.Imaging.Metafile>.</span><span class="sxs-lookup"><span data-stu-id="67d55-105">To display a vector image, you need an instance of the <xref:System.Drawing.Graphics> class and a <xref:System.Drawing.Imaging.Metafile>.</span></span> <span data-ttu-id="67d55-106">Pour afficher une image raster, vous avez besoin d’une instance de la <xref:System.Drawing.Graphics> classe et un <xref:System.Drawing.Bitmap>.</span><span class="sxs-lookup"><span data-stu-id="67d55-106">To display a raster image, you need an instance of the <xref:System.Drawing.Graphics> class and a <xref:System.Drawing.Bitmap>.</span></span> <span data-ttu-id="67d55-107">L’instance de la <xref:System.Drawing.Graphics> classe fournit le <xref:System.Drawing.Graphics.DrawImage%2A> (méthode), qui reçoit le <xref:System.Drawing.Imaging.Metafile> ou <xref:System.Drawing.Bitmap> en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="67d55-107">The instance of the <xref:System.Drawing.Graphics> class provides the <xref:System.Drawing.Graphics.DrawImage%2A> method, which receives the <xref:System.Drawing.Imaging.Metafile> or <xref:System.Drawing.Bitmap> as an argument.</span></span>  
  
## <a name="file-types-and-cloning"></a><span data-ttu-id="67d55-108">Types de fichiers et de clonage</span><span class="sxs-lookup"><span data-stu-id="67d55-108">File Types and Cloning</span></span>  
 <span data-ttu-id="67d55-109">L’exemple de code suivant montre comment construire un <xref:System.Drawing.Bitmap> à partir du fichier Climber.jpg et affiche la bitmap.</span><span class="sxs-lookup"><span data-stu-id="67d55-109">The following code example shows how to construct a <xref:System.Drawing.Bitmap> from the file Climber.jpg and displays the bitmap.</span></span> <span data-ttu-id="67d55-110">Point de destination pour le coin supérieur gauche de l’image, (10, 10), est spécifié dans les deuxième et troisième paramètres.</span><span class="sxs-lookup"><span data-stu-id="67d55-110">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters.</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#11)]  
  
 <span data-ttu-id="67d55-111">L’illustration suivante montre l’image.</span><span class="sxs-lookup"><span data-stu-id="67d55-111">The following illustration shows the image.</span></span>  
  
 <span data-ttu-id="67d55-112">![Exemple d’image](./media/aboutgdip03-art04.gif "AboutGdip03_Art04")</span><span class="sxs-lookup"><span data-stu-id="67d55-112">![Image Sample](./media/aboutgdip03-art04.gif "AboutGdip03_Art04")</span></span>  
  
 <span data-ttu-id="67d55-113">Vous pouvez construire <xref:System.Drawing.Bitmap> formats de fichier des objets à partir d’une variété de graphiques : BMP, GIF, JPEG, EXIF, PNG, TIFF et icône.</span><span class="sxs-lookup"><span data-stu-id="67d55-113">You can construct <xref:System.Drawing.Bitmap> objects from a variety of graphics file formats: BMP, GIF, JPEG, EXIF, PNG, TIFF, and ICON.</span></span>  
  
 <span data-ttu-id="67d55-114">L’exemple de code suivant montre comment construire <xref:System.Drawing.Bitmap> objets parmi un éventail de types de fichiers, puis affiche les bitmaps.</span><span class="sxs-lookup"><span data-stu-id="67d55-114">The following code example shows how to construct <xref:System.Drawing.Bitmap> objects from a variety of file types and then displays the bitmaps.</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#12)]  
  
 <span data-ttu-id="67d55-115">Le <xref:System.Drawing.Bitmap> classe fournit un <xref:System.Drawing.Bitmap.Clone%2A> méthode que vous pouvez utiliser pour effectuer une copie d’un existant <xref:System.Drawing.Bitmap>.</span><span class="sxs-lookup"><span data-stu-id="67d55-115">The <xref:System.Drawing.Bitmap> class provides a <xref:System.Drawing.Bitmap.Clone%2A> method that you can use to make a copy of an existing <xref:System.Drawing.Bitmap>.</span></span> <span data-ttu-id="67d55-116">Le <xref:System.Drawing.Bitmap.Clone%2A> méthode a un paramètre de rectangle source que vous pouvez utiliser pour spécifier la partie de l’image bitmap d’origine que vous souhaitez copier.</span><span class="sxs-lookup"><span data-stu-id="67d55-116">The <xref:System.Drawing.Bitmap.Clone%2A> method has a source rectangle parameter that you can use to specify the portion of the original bitmap that you want to copy.</span></span> <span data-ttu-id="67d55-117">L’exemple de code suivant montre comment créer un <xref:System.Drawing.Bitmap> en clonant la moitié supérieure du existant <xref:System.Drawing.Bitmap>.</span><span class="sxs-lookup"><span data-stu-id="67d55-117">The following code example shows how to create a <xref:System.Drawing.Bitmap> by cloning the top half of an existing <xref:System.Drawing.Bitmap>.</span></span> <span data-ttu-id="67d55-118">Ensuite, les deux images sont dessinées.</span><span class="sxs-lookup"><span data-stu-id="67d55-118">Then both images are drawn.</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#13](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#13](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#13)]  
  
 <span data-ttu-id="67d55-119">L’illustration suivante montre les deux images.</span><span class="sxs-lookup"><span data-stu-id="67d55-119">The following illustration shows the two images.</span></span>  
  
 <span data-ttu-id="67d55-120">![Cropping](./media/aboutgdip03-art05.gif "AboutGdip03_Art05")</span><span class="sxs-lookup"><span data-stu-id="67d55-120">![Cropping](./media/aboutgdip03-art05.gif "AboutGdip03_Art05")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67d55-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67d55-121">See also</span></span>

- [<span data-ttu-id="67d55-122">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="67d55-122">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="67d55-123">Guide pratique pour Créer des objets graphiques pour le dessin</span><span class="sxs-lookup"><span data-stu-id="67d55-123">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="67d55-124">Utilisation des images, bitmaps, icônes et métafichiers</span><span class="sxs-lookup"><span data-stu-id="67d55-124">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
