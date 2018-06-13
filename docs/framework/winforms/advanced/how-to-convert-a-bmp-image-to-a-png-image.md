---
title: 'Comment : convertir une image BMP en image PNG'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- BMP images [Windows Forms], converting to PNG
- image formats [Windows Forms], converting between
ms.assetid: 9d4a692d-73ac-4ce3-9e05-9ec321e8fbd6
ms.openlocfilehash: fd890c4f17b9759d37d7625526366034c664a71a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33520784"
---
# <a name="how-to-convert-a-bmp-image-to-a-png-image"></a><span data-ttu-id="1a851-102">Comment : convertir une image BMP en image PNG</span><span class="sxs-lookup"><span data-stu-id="1a851-102">How to: Convert a BMP image to a PNG image</span></span>
<span data-ttu-id="1a851-103">Il peut arriver que vous souhaitiez effectuer une conversion d'un format de fichier image vers un autre.</span><span class="sxs-lookup"><span data-stu-id="1a851-103">Oftentimes, you will want to convert from one image file format to another.</span></span> <span data-ttu-id="1a851-104">Vous pouvez facilement effectuer cette conversion en appelant la méthode <xref:System.Drawing.Image.Save%2A> de la classe <xref:System.Drawing.Image> et en spécifiant le <xref:System.Drawing.Imaging.ImageFormat> pour le format de fichier image souhaité.</span><span class="sxs-lookup"><span data-stu-id="1a851-104">You can do this conversion easily by calling the <xref:System.Drawing.Image.Save%2A> method of the <xref:System.Drawing.Image> class and specifying the <xref:System.Drawing.Imaging.ImageFormat> for the desired image file format.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1a851-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="1a851-105">Example</span></span>  
 <span data-ttu-id="1a851-106">L'exemple suivant charge une image BMP à partir d'un type et enregistre l'image au format PNG.</span><span class="sxs-lookup"><span data-stu-id="1a851-106">The following example loads a BMP image from a type, and saves the image in the PNG format.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#4](../../../../samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#4)]
 [!code-vb[UsingImageEncodersDecoders#4](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#4)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="1a851-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="1a851-107">Compiling the Code</span></span>  
 <span data-ttu-id="1a851-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="1a851-108">This example requires:</span></span>  
  
-   <span data-ttu-id="1a851-109">une application Windows Forms ;</span><span class="sxs-lookup"><span data-stu-id="1a851-109">A Windows Forms application.</span></span>  
  
-   <span data-ttu-id="1a851-110">une référence à l'espace de noms `System.Drawing.Imaging`.</span><span class="sxs-lookup"><span data-stu-id="1a851-110">A reference to the `System.Drawing.Imaging` namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a851-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a851-111">See Also</span></span>  
 [<span data-ttu-id="1a851-112">Guide pratique pour répertorier les encodeurs installés</span><span class="sxs-lookup"><span data-stu-id="1a851-112">How to: List Installed Encoders</span></span>](../../../../docs/framework/winforms/advanced/how-to-list-installed-encoders.md)  
 [<span data-ttu-id="1a851-113">Utilisation d’encodeurs et de décodeurs d’images dans GDI+ managé</span><span class="sxs-lookup"><span data-stu-id="1a851-113">Using Image Encoders and Decoders in Managed GDI+</span></span>](../../../../docs/framework/winforms/advanced/using-image-encoders-and-decoders-in-managed-gdi.md)  
 [<span data-ttu-id="1a851-114">Types de bitmaps</span><span class="sxs-lookup"><span data-stu-id="1a851-114">Types of Bitmaps</span></span>](../../../../docs/framework/winforms/advanced/types-of-bitmaps.md)
