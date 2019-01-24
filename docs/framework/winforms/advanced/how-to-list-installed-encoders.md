---
title: 'Procédure : Répertorier les encodeurs installés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image encoders [Windows Forms], listing
ms.assetid: 49e8e4e9-7a67-42d9-86bf-08821cdc282e
ms.openlocfilehash: c5019a349b4f3c881190241042cecc6c4c571950
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54605654"
---
# <a name="how-to-list-installed-encoders"></a><span data-ttu-id="91e26-102">Procédure : Répertorier les encodeurs installés</span><span class="sxs-lookup"><span data-stu-id="91e26-102">How to: List Installed Encoders</span></span>
<span data-ttu-id="91e26-103">Voulez-vous répertorier les encodeurs d’images disponibles sur un ordinateur, pour déterminer si votre application peut enregistrer dans un format de fichier d’image particulier.</span><span class="sxs-lookup"><span data-stu-id="91e26-103">You may want to list the image encoders available on a computer, to determine whether your application can save to a particular image file format.</span></span> <span data-ttu-id="91e26-104">Le <xref:System.Drawing.Imaging.ImageCodecInfo> classe fournit le <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> des méthodes statiques afin que vous puissiez déterminer quelle image les encodeurs sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="91e26-104">The <xref:System.Drawing.Imaging.ImageCodecInfo> class provides the <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> static methods so that you can determine which image encoders are available.</span></span> <span data-ttu-id="91e26-105"><xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> Retourne un tableau de <xref:System.Drawing.Imaging.ImageCodecInfo> objets.</span><span class="sxs-lookup"><span data-stu-id="91e26-105"><xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> returns an array of <xref:System.Drawing.Imaging.ImageCodecInfo> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="91e26-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="91e26-106">Example</span></span>  
 <span data-ttu-id="91e26-107">L’exemple de code suivant génère la liste des encodeurs installés et leurs valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="91e26-107">The following code example outputs the list of installed encoders and their property values.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#1)]
 [!code-vb[UsingImageEncodersDecoders#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="91e26-108">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="91e26-108">Compiling the Code</span></span>  
 <span data-ttu-id="91e26-109">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="91e26-109">This example requires:</span></span>  
  
-   <span data-ttu-id="91e26-110">une application Windows Forms ;</span><span class="sxs-lookup"><span data-stu-id="91e26-110">A Windows Forms application.</span></span>  
  
-   <span data-ttu-id="91e26-111">Un <xref:System.Windows.Forms.PaintEventArgs>, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="91e26-111">A <xref:System.Windows.Forms.PaintEventArgs>, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91e26-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91e26-112">See also</span></span>
- [<span data-ttu-id="91e26-113">Guide pratique pour Répertorier les décodeurs installés</span><span class="sxs-lookup"><span data-stu-id="91e26-113">How to: List Installed Decoders</span></span>](../../../../docs/framework/winforms/advanced/how-to-list-installed-decoders.md)
- [<span data-ttu-id="91e26-114">Utilisation d’encodeurs et de décodeurs d’images dans GDI+ managé</span><span class="sxs-lookup"><span data-stu-id="91e26-114">Using Image Encoders and Decoders in Managed GDI+</span></span>](../../../../docs/framework/winforms/advanced/using-image-encoders-and-decoders-in-managed-gdi.md)
