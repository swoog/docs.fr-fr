---
title: 'Procédure : dessiner une image bitmap existante à l’écran'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [Windows Forms], displaying in Windows Forms
- bitmaps [Windows Forms], loading in Windows Forms applications
- images [Windows Forms], displaying on Windows Forms
ms.assetid: 5bc558d7-b326-4050-a834-b8600da0de95
ms.openlocfilehash: 90511adf9caffe7952e270d6fe32dd85162a29d7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59089164"
---
# <a name="how-to-draw-an-existing-bitmap-to-the-screen"></a><span data-ttu-id="5d702-102">Procédure : dessiner une image bitmap existante à l’écran</span><span class="sxs-lookup"><span data-stu-id="5d702-102">How to: Draw an Existing Bitmap to the Screen</span></span>
<span data-ttu-id="5d702-103">Vous pouvez facilement dessiner une image existante sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="5d702-103">You can easily draw an existing image on the screen.</span></span> <span data-ttu-id="5d702-104">Vous devez d’abord créer un <xref:System.Drawing.Bitmap> objet à l’aide du constructeur de bitmap qui prend un nom de fichier <xref:System.Drawing.Bitmap.%23ctor%28System.String%29>.</span><span class="sxs-lookup"><span data-stu-id="5d702-104">First you need to create a <xref:System.Drawing.Bitmap> object by using the bitmap constructor that takes a file name, <xref:System.Drawing.Bitmap.%23ctor%28System.String%29>.</span></span> <span data-ttu-id="5d702-105">Ce constructeur accepte des images avec différents formats de fichiers, notamment BMP, GIF, JPEG, PNG et TIFF.</span><span class="sxs-lookup"><span data-stu-id="5d702-105">This constructor accepts images with several different file formats, including BMP, GIF, JPEG, PNG, and TIFF.</span></span> <span data-ttu-id="5d702-106">Après avoir créé le <xref:System.Drawing.Bitmap> d’objet, qui passez <xref:System.Drawing.Bitmap> de l’objet à la <xref:System.Drawing.Graphics.DrawImage%2A> méthode d’un <xref:System.Drawing.Graphics> objet.</span><span class="sxs-lookup"><span data-stu-id="5d702-106">After you have created the <xref:System.Drawing.Bitmap> object, pass that <xref:System.Drawing.Bitmap> object to the <xref:System.Drawing.Graphics.DrawImage%2A> method of a <xref:System.Drawing.Graphics> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5d702-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="5d702-107">Example</span></span>  
 <span data-ttu-id="5d702-108">Cet exemple crée un <xref:System.Drawing.Bitmap> objet à partir d’un fichier JPEG, puis dessine l’image bitmap avec son coin supérieur gauche à (60, 10).</span><span class="sxs-lookup"><span data-stu-id="5d702-108">This example creates a <xref:System.Drawing.Bitmap> object from a JPEG file and then draws the bitmap with its upper-left corner at (60, 10).</span></span>  
  
 <span data-ttu-id="5d702-109">L’illustration suivante montre l’image bitmap dessinée à l’emplacement spécifié :</span><span class="sxs-lookup"><span data-stu-id="5d702-109">The following illustration shows the bitmap drawn at the specified location:</span></span>  
  
 ![Capture d’écran montrant une image à une position spécifiée.](./media/how-to-draw-an-existing-bitmap-to-the-screen/bitmap-specified-position.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.WorkingWithImages#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5d702-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="5d702-111">Compiling the Code</span></span>  
 <span data-ttu-id="5d702-112">L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="5d702-112">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d702-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d702-113">See also</span></span>

- [<span data-ttu-id="5d702-114">Graphiques et dessins dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5d702-114">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="5d702-115">Utilisation des images, bitmaps, icônes et métafichiers</span><span class="sxs-lookup"><span data-stu-id="5d702-115">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
