---
title: 'Procédure : lister les encodeurs installés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image encoders [Windows Forms], listing
ms.assetid: 49e8e4e9-7a67-42d9-86bf-08821cdc282e
ms.openlocfilehash: ce297cb6d183bc63c8b276e30100aa4e864cd90d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61722950"
---
# <a name="how-to-list-installed-encoders"></a><span data-ttu-id="46e28-102">Procédure : lister les encodeurs installés</span><span class="sxs-lookup"><span data-stu-id="46e28-102">How to: List Installed Encoders</span></span>
<span data-ttu-id="46e28-103">Voulez-vous répertorier les encodeurs d’images disponibles sur un ordinateur, pour déterminer si votre application peut enregistrer dans un format de fichier d’image particulier.</span><span class="sxs-lookup"><span data-stu-id="46e28-103">You may want to list the image encoders available on a computer, to determine whether your application can save to a particular image file format.</span></span> <span data-ttu-id="46e28-104">Le <xref:System.Drawing.Imaging.ImageCodecInfo> classe fournit le <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> des méthodes statiques afin que vous puissiez déterminer quelle image les encodeurs sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="46e28-104">The <xref:System.Drawing.Imaging.ImageCodecInfo> class provides the <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> static methods so that you can determine which image encoders are available.</span></span> <span data-ttu-id="46e28-105"><xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> Retourne un tableau de <xref:System.Drawing.Imaging.ImageCodecInfo> objets.</span><span class="sxs-lookup"><span data-stu-id="46e28-105"><xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> returns an array of <xref:System.Drawing.Imaging.ImageCodecInfo> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="46e28-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="46e28-106">Example</span></span>  
 <span data-ttu-id="46e28-107">L’exemple de code suivant génère la liste des encodeurs installés et leurs valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="46e28-107">The following code example outputs the list of installed encoders and their property values.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#1](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#1)]
 [!code-vb[UsingImageEncodersDecoders#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="46e28-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="46e28-108">Compiling the Code</span></span>  
 <span data-ttu-id="46e28-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="46e28-109">This example requires:</span></span>  
  
-   <span data-ttu-id="46e28-110">une application Windows Forms ;</span><span class="sxs-lookup"><span data-stu-id="46e28-110">A Windows Forms application.</span></span>  
  
-   <span data-ttu-id="46e28-111">Un <xref:System.Windows.Forms.PaintEventArgs>, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="46e28-111">A <xref:System.Windows.Forms.PaintEventArgs>, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46e28-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46e28-112">See also</span></span>

- [<span data-ttu-id="46e28-113">Guide pratique pour Répertorier les décodeurs installés</span><span class="sxs-lookup"><span data-stu-id="46e28-113">How to: List Installed Decoders</span></span>](how-to-list-installed-decoders.md)
- [<span data-ttu-id="46e28-114">Utilisation d’encodeurs et de décodeurs d’images dans GDI+ managé</span><span class="sxs-lookup"><span data-stu-id="46e28-114">Using Image Encoders and Decoders in Managed GDI+</span></span>](using-image-encoders-and-decoders-in-managed-gdi.md)
