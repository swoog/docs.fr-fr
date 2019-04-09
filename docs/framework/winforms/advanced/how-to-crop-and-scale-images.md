---
title: 'Procédure : rogner et mettre à l’échelle des images'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], cropping
- images [Windows Forms], scaling
ms.assetid: 053e3360-bca0-4b25-9afa-0e77a6f17b03
ms.openlocfilehash: 4257431881565f9160f45795111d374cc680dedd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59189883"
---
# <a name="how-to-crop-and-scale-images"></a><span data-ttu-id="a8415-102">Procédure : rogner et mettre à l’échelle des images</span><span class="sxs-lookup"><span data-stu-id="a8415-102">How to: Crop and Scale Images</span></span>
<span data-ttu-id="a8415-103">Le <xref:System.Drawing.Graphics> classe fournit plusieurs <xref:System.Drawing.Graphics.DrawImage%2A> méthodes, dont certaines ont des paramètres de rectangle source et destination que vous pouvez utiliser pour rogner et mettre à l’échelle des images.</span><span class="sxs-lookup"><span data-stu-id="a8415-103">The <xref:System.Drawing.Graphics> class provides several <xref:System.Drawing.Graphics.DrawImage%2A> methods, some of which have source and destination rectangle parameters that you can use to crop and scale images.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a8415-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8415-104">Example</span></span>  
 <span data-ttu-id="a8415-105">L’exemple suivant construit un <xref:System.Drawing.Image> objet à partir du fichier de disque Apple.gif.</span><span class="sxs-lookup"><span data-stu-id="a8415-105">The following example constructs an <xref:System.Drawing.Image> object from the disk file Apple.gif.</span></span> <span data-ttu-id="a8415-106">Le code dessine l’image entière dans sa taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="a8415-106">The code draws the entire apple image in its original size.</span></span> <span data-ttu-id="a8415-107">Le code appelle ensuite la <xref:System.Drawing.Graphics.DrawImage%2A> méthode d’un <xref:System.Drawing.Graphics> objet sur lequel dessiner une partie de l’image dans un rectangle de destination est supérieur à l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="a8415-107">The code then calls the <xref:System.Drawing.Graphics.DrawImage%2A> method of a <xref:System.Drawing.Graphics> object to draw a portion of the apple image in a destination rectangle that is larger than the original apple image.</span></span>  
  
 <span data-ttu-id="a8415-108">Le <xref:System.Drawing.Graphics.DrawImage%2A> méthode détermine la partie de la pomme à dessiner en examinant le rectangle source, qui est spécifié par le troisième, quatrième, cinquième et sixième arguments.</span><span class="sxs-lookup"><span data-stu-id="a8415-108">The <xref:System.Drawing.Graphics.DrawImage%2A> method determines which portion of the apple to draw by looking at the source rectangle, which is specified by the third, fourth, fifth, and sixth arguments.</span></span> <span data-ttu-id="a8415-109">Dans ce cas, la pomme est rognée à 75 % de sa largeur et 75 pour cent de sa hauteur.</span><span class="sxs-lookup"><span data-stu-id="a8415-109">In this case, the apple is cropped to 75 percent of its width and 75 percent of its height.</span></span>  
  
 <span data-ttu-id="a8415-110">Le <xref:System.Drawing.Graphics.DrawImage%2A> méthode détermine où dessiner la pomme rognée et la taille pour rendre la pomme rognée en examinant le rectangle de destination, qui est spécifié par le deuxième argument.</span><span class="sxs-lookup"><span data-stu-id="a8415-110">The <xref:System.Drawing.Graphics.DrawImage%2A> method determines where to draw the cropped apple and how big to make the cropped apple by looking at the destination rectangle, which is specified by the second argument.</span></span> <span data-ttu-id="a8415-111">Dans ce cas, le rectangle de destination est 30 pour cent plus large et 30 pour cent plus haut que l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="a8415-111">In this case, the destination rectangle is 30 percent wider and 30 percent taller than the original image.</span></span>  
  
 <span data-ttu-id="a8415-112">L’illustration suivante montre la pomme d’origine et la mise à l’échelle, rognage d’apple.</span><span class="sxs-lookup"><span data-stu-id="a8415-112">The following illustration shows the original apple and the scaled, cropped apple.</span></span>  
  
 ![Capture d’écran d’une image d’origine et de la même image rognée.](./media/how-to-crop-and-scale-images/original-image-cropped-image.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.WorkingWithImages#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a8415-114">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="a8415-114">Compiling the Code</span></span>  
 <span data-ttu-id="a8415-115">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="a8415-115">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="a8415-116">Veillez à remplacer `Apple.gif` avec un nom de fichier d’image et le chemin d’accès valides sur votre système.</span><span class="sxs-lookup"><span data-stu-id="a8415-116">Make sure to replace `Apple.gif` with an image file name and path that are valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8415-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8415-117">See also</span></span>

- [<span data-ttu-id="a8415-118">Images, bitmaps et métafichiers</span><span class="sxs-lookup"><span data-stu-id="a8415-118">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="a8415-119">Utilisation des images, bitmaps, icônes et métafichiers</span><span class="sxs-lookup"><span data-stu-id="a8415-119">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
