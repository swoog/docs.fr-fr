---
title: 'Comment : encoder et décoder une image JPEG'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- encoding image formats [WPF]
- decoding JPEG images [WPF]
- encoding JPEG images [WPF]
- decoding image formats [WPF]
- JPEG decoding [WPF]
- JPEG encoding [WPF]
ms.assetid: b8cfde37-9f68-4911-a05e-51d8d7bdec7b
ms.openlocfilehash: 916eab63938100daf91e6c1a5af31648a99108d0
ms.sourcegitcommit: f9e38d31288fe5962e6be5b0cc286da633482873
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/27/2018
ms.locfileid: "37027965"
---
# <a name="how-to-encode-and-decode-a-jpeg-image"></a><span data-ttu-id="701c0-102">Comment : encoder et décoder une image JPEG</span><span class="sxs-lookup"><span data-stu-id="701c0-102">How to: Encode and decode a JPEG image</span></span>

<span data-ttu-id="701c0-103">Les exemples suivants montrent comment décoder et encoder une image JPEG à l’aide spécifique au <xref:System.Windows.Media.Imaging.JpegBitmapDecoder> et <xref:System.Windows.Media.Imaging.JpegBitmapEncoder> objets.</span><span class="sxs-lookup"><span data-stu-id="701c0-103">The following examples show how to decode and encode a JPEG image using the specific <xref:System.Windows.Media.Imaging.JpegBitmapDecoder> and <xref:System.Windows.Media.Imaging.JpegBitmapEncoder> objects.</span></span>  
  
## <a name="example---decode-a-jpeg-image"></a><span data-ttu-id="701c0-104">Exemple - décoder une image JPEG</span><span class="sxs-lookup"><span data-stu-id="701c0-104">Example - Decode a JPEG image</span></span>

<span data-ttu-id="701c0-105">Cet exemple montre comment décoder une image JPEG en utilisant un <xref:System.Windows.Media.Imaging.JpegBitmapDecoder> d’un <xref:System.IO.FileStream>.</span><span class="sxs-lookup"><span data-stu-id="701c0-105">This example demonstrates how to decode a JPEG image using a <xref:System.Windows.Media.Imaging.JpegBitmapDecoder> from a <xref:System.IO.FileStream>.</span></span>  
  
[!code-cpp[JpegBitmapDecoderEncoder#1](~/samples/snippets/cpp/VS_Snippets_Wpf/JpegBitmapDecoderEncoder/CPP/jpegencoderdecoder.cpp#1)]
[!code-csharp[JpegBitmapDecoderEncoder#1](~/samples/snippets/csharp/VS_Snippets_Wpf/JpegBitmapDecoderEncoder/CSharp/JpegEncoderDecoder.cs#1)]
[!code-vb[JpegBitmapDecoderEncoder#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/JpegBitmapDecoderEncoder/VB/JpegEncoderDecoder.vb#1)]  
  
## <a name="example---encode-a-jpeg-image"></a><span data-ttu-id="701c0-106">Exemple - encoder une image JPEG</span><span class="sxs-lookup"><span data-stu-id="701c0-106">Example - Encode a JPEG image</span></span>

<span data-ttu-id="701c0-107">Cet exemple montre comment encoder un <xref:System.Windows.Media.Imaging.BitmapSource> au format de l’image à l’aide un <xref:System.Windows.Media.Imaging.JpegBitmapEncoder>.</span><span class="sxs-lookup"><span data-stu-id="701c0-107">This example demonstrates how to encode a <xref:System.Windows.Media.Imaging.BitmapSource> into a JPEG image using a <xref:System.Windows.Media.Imaging.JpegBitmapEncoder>.</span></span>  
  
[!code-cpp[JpegBitmapDecoderEncoder#4](~/samples/snippets/cpp/VS_Snippets_Wpf/JpegBitmapDecoderEncoder/CPP/jpegencoderdecoder.cpp#4)]
[!code-csharp[JpegBitmapDecoderEncoder#4](~/samples/snippets/csharp/VS_Snippets_Wpf/JpegBitmapDecoderEncoder/CSharp/JpegEncoderDecoder.cs#4)]
[!code-vb[JpegBitmapDecoderEncoder#4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/JpegBitmapDecoderEncoder/VB/JpegEncoderDecoder.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="701c0-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="701c0-108">See also</span></span>

[<span data-ttu-id="701c0-109">Vue d’ensemble de la création d’images</span><span class="sxs-lookup"><span data-stu-id="701c0-109">Imaging Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)