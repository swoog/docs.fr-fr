---
title: Utilisation des images, bitmaps, icônes et métafichiers
ms.date: 03/30/2017
helpviewer_keywords:
- metafiles [Windows Forms], working with
- examples [Windows Forms], bitmaps
- examples [Windows Forms], images
- bitmaps [Windows Forms], working with
- images [Windows Forms], working with
- examples [Windows Forms], metafiles
ms.assetid: a626d701-bd99-4fd8-b92f-7b8f794e042b
ms.openlocfilehash: 6d2f0a2f4acebaac59f2d8180f2de4ccb88b2965
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33526832"
---
# <a name="working-with-images-bitmaps-icons-and-metafiles"></a><span data-ttu-id="cd3f0-102">Utilisation des images, bitmaps, icônes et métafichiers</span><span class="sxs-lookup"><span data-stu-id="cd3f0-102">Working with Images, Bitmaps, Icons, and Metafiles</span></span>
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]<span data-ttu-id="cd3f0-103"> fournit la classe `Bitmap` pour utiliser des images raster et la classe `Metafile` pour utiliser des images vectorielles.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-103"> provides the `Bitmap` class for working with raster images and the `Metafile` class for working with vector images.</span></span> <span data-ttu-id="cd3f0-104">Les classes `Bitmap` et `Metafile` héritent toutes deux de la classe `Image`.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-104">The `Bitmap` and the `Metafile` classes both inherit from the `Image` class.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="cd3f0-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="cd3f0-105">In This Section</span></span>  
 [<span data-ttu-id="cd3f0-106">Guide pratique pour dessiner une bitmap existante à l'écran</span><span class="sxs-lookup"><span data-stu-id="cd3f0-106">How to: Draw an Existing Bitmap to the Screen</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-an-existing-bitmap-to-the-screen.md)  
 <span data-ttu-id="cd3f0-107">Décrit comment charger et dessiner des bitmaps.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-107">Describes how to load and draw bitmaps.</span></span>  
  
 [<span data-ttu-id="cd3f0-108">Guide pratique pour charger et afficher des métafichiers</span><span class="sxs-lookup"><span data-stu-id="cd3f0-108">How to: Load and Display Metafiles</span></span>](../../../../docs/framework/winforms/advanced/how-to-load-and-display-metafiles.md)  
 <span data-ttu-id="cd3f0-109">Montre comment charger et dessiner des métafichiers.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-109">Shows how to load and draw metafiles.</span></span>  
  
 [<span data-ttu-id="cd3f0-110">Rognage et mise à l'échelle d'images dans GDI+</span><span class="sxs-lookup"><span data-stu-id="cd3f0-110">Cropping and Scaling Images in GDI+</span></span>](../../../../docs/framework/winforms/advanced/cropping-and-scaling-images-in-gdi.md)  
 <span data-ttu-id="cd3f0-111">Explique comment rogner et mettre à l'échelle des images raster et vectorielles.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-111">Explains how to crop and scale vector and raster images.</span></span>  
  
 [<span data-ttu-id="cd3f0-112">Guide pratique pour faire pivoter, refléter et incliner des images</span><span class="sxs-lookup"><span data-stu-id="cd3f0-112">How to: Rotate, Reflect, and Skew Images</span></span>](../../../../docs/framework/winforms/advanced/how-to-rotate-reflect-and-skew-images.md)  
 <span data-ttu-id="cd3f0-113">Décrit comment dessiner des images pivotées, reflétées et inclinées.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-113">Describes how to draw rotated, reflected and skewed images.</span></span>  
  
 [<span data-ttu-id="cd3f0-114">Guide pratique pour utiliser le mode d'interpolation pour contrôler la qualité d'image pendant la mise à l'échelle</span><span class="sxs-lookup"><span data-stu-id="cd3f0-114">How to: Use Interpolation Mode to Control Image Quality During Scaling</span></span>](../../../../docs/framework/winforms/advanced/how-to-use-interpolation-mode-to-control-image-quality-during-scaling.md)  
 <span data-ttu-id="cd3f0-115">Montre comment utiliser l'énumération <xref:System.Drawing.Drawing2D.InterpolationMode> pour modifier la qualité d'image.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-115">Shows how to use the <xref:System.Drawing.Drawing2D.InterpolationMode> enumeration to change image quality.</span></span>  
  
 [<span data-ttu-id="cd3f0-116">Guide pratique pour créer des images miniatures</span><span class="sxs-lookup"><span data-stu-id="cd3f0-116">How to: Create Thumbnail Images</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-thumbnail-images.md)  
 <span data-ttu-id="cd3f0-117">Décrit comment créer des images miniatures.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-117">Describes how to create thumbnail images.</span></span>  
  
 [<span data-ttu-id="cd3f0-118">Guide pratique pour améliorer les performances en évitant la mise à l’échelle automatique</span><span class="sxs-lookup"><span data-stu-id="cd3f0-118">How to: Improve Performance by Avoiding Automatic Scaling</span></span>](../../../../docs/framework/winforms/advanced/how-to-improve-performance-by-avoiding-automatic-scaling.md)  
 <span data-ttu-id="cd3f0-119">Explique comment dessiner une image sans mise à l'échelle automatique.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-119">Explains how to draw an image without automatic scaling.</span></span>  
  
 [<span data-ttu-id="cd3f0-120">Guide pratique pour lire des métadonnées d'image</span><span class="sxs-lookup"><span data-stu-id="cd3f0-120">How to: Read Image Metadata</span></span>](../../../../docs/framework/winforms/advanced/how-to-read-image-metadata.md)  
 <span data-ttu-id="cd3f0-121">Décrit comment lire des métadonnées à partir d'une image.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-121">Describes how to read metadata from an image.</span></span>  
  
 [<span data-ttu-id="cd3f0-122">Guide pratique pour créer une bitmap au moment de l'exécution</span><span class="sxs-lookup"><span data-stu-id="cd3f0-122">How to: Create a Bitmap at Run Time</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-a-bitmap-at-run-time.md)  
 <span data-ttu-id="cd3f0-123">Montre comment dessiner une bitmap au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-123">Shows how to draw a bitmap at runtime.</span></span>  
  
 [<span data-ttu-id="cd3f0-124">Guide pratique pour extraire l'icône associée à un fichier dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cd3f0-124">How to: Extract the Icon Associated with a File in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/how-to-extract-the-icon-associated-with-a-file-in-windows-forms.md)  
 <span data-ttu-id="cd3f0-125">Décrit comment extraire une icône qui est une ressource incorporée d'un fichier.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-125">Describes how to extract an icon that is an embedded resource of a file.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="cd3f0-126">Référence</span><span class="sxs-lookup"><span data-stu-id="cd3f0-126">Reference</span></span>  
 <xref:System.Drawing.Image>  
 <span data-ttu-id="cd3f0-127">Décrit cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-127">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Drawing.Imaging.Metafile>  
 <span data-ttu-id="cd3f0-128">Décrit cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-128">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Drawing.Bitmap>  
 <span data-ttu-id="cd3f0-129">Décrit cette classe et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-129">Describes this class and has links to all of its members.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="cd3f0-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd3f0-130">Related Sections</span></span>  
 [<span data-ttu-id="cd3f0-131">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="cd3f0-131">Images, Bitmaps, and Metafiles</span></span>](../../../../docs/framework/winforms/advanced/images-bitmaps-and-metafiles.md)  
 <span data-ttu-id="cd3f0-132">Contient des liens vers des rubriques qui traitent des différents types de bitmaps et de leur manipulation dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="cd3f0-132">Contains links to topics that discuss different types of bitmaps and manipulating them in your applications.</span></span>
