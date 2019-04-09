---
title: 'Procédure : lister les décodeurs installés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image decoders [Windows Forms], listing
ms.assetid: 11417191-8c95-40ca-8024-779e61706fb6
ms.openlocfilehash: c92b8010def2f77f859ee0bd9cdb1ed51dd15f27
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079409"
---
# <a name="how-to-list-installed-decoders"></a><span data-ttu-id="fdfb0-102">Procédure : lister les décodeurs installés</span><span class="sxs-lookup"><span data-stu-id="fdfb0-102">How to: List Installed Decoders</span></span>
<span data-ttu-id="fdfb0-103">Voulez-vous répertorier les décodeurs d’images disponibles sur un ordinateur, pour déterminer si votre application peut lire un format de fichier d’image particulier.</span><span class="sxs-lookup"><span data-stu-id="fdfb0-103">You may want to list the image decoders available on a computer, to determine whether your application can read a particular image file format.</span></span> <span data-ttu-id="fdfb0-104">Le <xref:System.Drawing.Imaging.ImageCodecInfo> classe fournit le <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> des méthodes statiques afin que vous pouvez déterminer quelle image décodeurs disponibles.</span><span class="sxs-lookup"><span data-stu-id="fdfb0-104">The <xref:System.Drawing.Imaging.ImageCodecInfo> class provides the <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> static methods so that you can determine which image decoders are available.</span></span> <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> <span data-ttu-id="fdfb0-105">Retourne un tableau de <xref:System.Drawing.Imaging.ImageCodecInfo> objets.</span><span class="sxs-lookup"><span data-stu-id="fdfb0-105">returns an array of <xref:System.Drawing.Imaging.ImageCodecInfo> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fdfb0-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="fdfb0-106">Example</span></span>  
 <span data-ttu-id="fdfb0-107">L’exemple de code suivant génère la liste des décodeurs installés et leurs valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="fdfb0-107">The following code example outputs the list of installed decoders and their property values.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#2](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#2)]
 [!code-vb[UsingImageEncodersDecoders#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#2)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="fdfb0-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="fdfb0-108">Compiling the Code</span></span>  
 <span data-ttu-id="fdfb0-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="fdfb0-109">This example requires:</span></span>  
  
-   <span data-ttu-id="fdfb0-110">une application Windows Forms ;</span><span class="sxs-lookup"><span data-stu-id="fdfb0-110">A Windows Forms application.</span></span>  
  
-   <span data-ttu-id="fdfb0-111">Un <xref:System.Windows.Forms.PaintEventArgs>, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="fdfb0-111">A <xref:System.Windows.Forms.PaintEventArgs>, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fdfb0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdfb0-112">See also</span></span>

- [<span data-ttu-id="fdfb0-113">Procédure : lister les encodeurs installés</span><span class="sxs-lookup"><span data-stu-id="fdfb0-113">How to: List Installed Encoders</span></span>](how-to-list-installed-encoders.md)
- [<span data-ttu-id="fdfb0-114">Utilisation d'encodeurs et de décodeurs d'images dans GDI+ managé</span><span class="sxs-lookup"><span data-stu-id="fdfb0-114">Using Image Encoders and Decoders in Managed GDI+</span></span>](using-image-encoders-and-decoders-in-managed-gdi.md)
