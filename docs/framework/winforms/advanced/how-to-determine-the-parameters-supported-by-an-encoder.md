---
title: 'Procédure : déterminer les paramètres pris en charge par un encodeur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- encoder parameters [Windows Forms], determining supported
ms.assetid: f47ae459-e3ce-4d41-a140-2f6c6aea3f44
ms.openlocfilehash: 2626eee239d9876125340dd133c5a9b3e45c3d7e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62004326"
---
# <a name="how-to-determine-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="64227-102">Procédure : déterminer les paramètres pris en charge par un encodeur</span><span class="sxs-lookup"><span data-stu-id="64227-102">How to: Determine the Parameters Supported by an Encoder</span></span>
<span data-ttu-id="64227-103">Vous pouvez ajuster les paramètres d’image, comme le niveau de qualité et la compression, mais vous devez savoir quels paramètres sont pris en charge par un encodeur d’image donné.</span><span class="sxs-lookup"><span data-stu-id="64227-103">You can adjust image parameters, such as quality and compression level, but you must know which parameters are supported by a given image encoder.</span></span> <span data-ttu-id="64227-104">Le <xref:System.Drawing.Image> classe fournit le <xref:System.Drawing.Image.GetEncoderParameterList%2A> méthode afin que vous puissiez déterminer quels paramètres d’image sont pris en charge pour un encodeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="64227-104">The <xref:System.Drawing.Image> class provides the <xref:System.Drawing.Image.GetEncoderParameterList%2A> method so that you can determine which image parameters are supported for a particular encoder.</span></span> <span data-ttu-id="64227-105">Vous spécifiez l’encodeur avec un GUID.</span><span class="sxs-lookup"><span data-stu-id="64227-105">You specify the encoder with a GUID.</span></span> <span data-ttu-id="64227-106">Le <xref:System.Drawing.Image.GetEncoderParameterList%2A> méthode retourne un tableau de <xref:System.Drawing.Imaging.EncoderParameter> objets.</span><span class="sxs-lookup"><span data-stu-id="64227-106">The <xref:System.Drawing.Image.GetEncoderParameterList%2A> method returns an array of <xref:System.Drawing.Imaging.EncoderParameter> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="64227-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="64227-107">Example</span></span>  
 <span data-ttu-id="64227-108">L’exemple de code suivant génère les paramètres pris en charge pour l’encodeur JPEG.</span><span class="sxs-lookup"><span data-stu-id="64227-108">The following example code outputs the supported parameters for the JPEG encoder.</span></span> <span data-ttu-id="64227-109">Utilisez la liste des catégories de paramètre et les GUID associés dans le <xref:System.Drawing.Imaging.Encoder> vue d’ensemble de la classe pour déterminer la catégorie de chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="64227-109">Use the list of parameter categories and associated GUIDs in the <xref:System.Drawing.Imaging.Encoder> class overview to determine the category for each parameter.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#3](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#3)]
 [!code-vb[UsingImageEncodersDecoders#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#3)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="64227-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="64227-110">Compiling the Code</span></span>  
 <span data-ttu-id="64227-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="64227-111">This example requires:</span></span>  
  
- <span data-ttu-id="64227-112">une application Windows Forms ;</span><span class="sxs-lookup"><span data-stu-id="64227-112">A Windows Forms application.</span></span>  
  
- <span data-ttu-id="64227-113">Un <xref:System.Windows.Forms.PaintEventArgs>, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="64227-113">A <xref:System.Windows.Forms.PaintEventArgs>, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64227-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64227-114">See also</span></span>

- [<span data-ttu-id="64227-115">Guide pratique pour Répertorier les encodeurs installés</span><span class="sxs-lookup"><span data-stu-id="64227-115">How to: List Installed Encoders</span></span>](how-to-list-installed-encoders.md)
- [<span data-ttu-id="64227-116">Types de bitmaps</span><span class="sxs-lookup"><span data-stu-id="64227-116">Types of Bitmaps</span></span>](types-of-bitmaps.md)
- [<span data-ttu-id="64227-117">Utilisation d’encodeurs et de décodeurs d’images dans GDI+ managé</span><span class="sxs-lookup"><span data-stu-id="64227-117">Using Image Encoders and Decoders in Managed GDI+</span></span>](using-image-encoders-and-decoders-in-managed-gdi.md)
