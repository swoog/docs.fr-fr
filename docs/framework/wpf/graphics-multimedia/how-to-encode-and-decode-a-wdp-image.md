---
title: 'Procédure : Encoder et décoder une image WDP'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- WDP encoding [WPF]
- WDP decoding [WPF]
- encoding image formats [WPF]
- decoding WDP images [WPF]
- decoding image formats [WPF]
- encoding WDP images [WPF]
ms.assetid: 911777d1-516b-49db-a87b-b54e31b18532
ms.openlocfilehash: b143106092235b42044d264189c135d2cd65426c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59153359"
---
# <a name="how-to-encode-and-decode-a-wdp-image"></a><span data-ttu-id="b9ff1-102">Procédure : Encoder et décoder une image WDP</span><span class="sxs-lookup"><span data-stu-id="b9ff1-102">How to: Encode and Decode a WDP Image</span></span>
<span data-ttu-id="b9ff1-103">Les exemples suivants montrent comment décoder et encoder une [!INCLUDE[TLA#tla_wdp](../../../../includes/tlasharptla-wdp-md.md)] de l’image à l’aide spécifique au <xref:System.Windows.Media.Imaging.WmpBitmapDecoder> et <xref:System.Windows.Media.Imaging.WmpBitmapEncoder> objets.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-103">The following examples show how to decode and encode a [!INCLUDE[TLA#tla_wdp](../../../../includes/tlasharptla-wdp-md.md)] image using the specific <xref:System.Windows.Media.Imaging.WmpBitmapDecoder> and <xref:System.Windows.Media.Imaging.WmpBitmapEncoder> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b9ff1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b9ff1-104">Example</span></span>  
 <span data-ttu-id="b9ff1-105">Cet exemple montre comment décoder une [!INCLUDE[TLA2#tla_wdp](../../../../includes/tla2sharptla-wdp-md.md)] à l’aide de l’image un <xref:System.Windows.Media.Imaging.WmpBitmapDecoder> à partir d’un <xref:System.Uri>.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-105">This example demonstrates how to decode a [!INCLUDE[TLA2#tla_wdp](../../../../includes/tla2sharptla-wdp-md.md)] image using a <xref:System.Windows.Media.Imaging.WmpBitmapDecoder> from a <xref:System.Uri>.</span></span>  
  
 [!code-cpp[WdpBitmapDecoderEncoder#1](~/samples/snippets/cpp/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/CPP/WDPEncoderDecoder.cpp#1)]
 [!code-csharp[WdpBitmapDecoderEncoder#1](~/samples/snippets/csharp/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/CSharp/WDPEncoderDecoder.cs#1)]
 [!code-vb[WdpBitmapDecoderEncoder#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/VB/WDPEncoderDecoder.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="b9ff1-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="b9ff1-106">Example</span></span>  
 <span data-ttu-id="b9ff1-107">Cet exemple montre comment encoder un <xref:System.Windows.Media.Imaging.BitmapSource> dans un [!INCLUDE[TLA2#tla_wdp](../../../../includes/tla2sharptla-wdp-md.md)] à l’aide de l’image un <xref:System.Windows.Media.Imaging.WmpBitmapEncoder>.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-107">This example demonstrates how to encode a <xref:System.Windows.Media.Imaging.BitmapSource> into a [!INCLUDE[TLA2#tla_wdp](../../../../includes/tla2sharptla-wdp-md.md)] image using a <xref:System.Windows.Media.Imaging.WmpBitmapEncoder>.</span></span>  
  
 [!code-cpp[WdpBitmapDecoderEncoder#4](~/samples/snippets/cpp/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/CPP/WDPEncoderDecoder.cpp#4)]
 [!code-csharp[WdpBitmapDecoderEncoder#4](~/samples/snippets/csharp/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/CSharp/WDPEncoderDecoder.cs#4)]
 [!code-vb[WdpBitmapDecoderEncoder#4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WdpBitmapDecoderEncoder/VB/WDPEncoderDecoder.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="b9ff1-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9ff1-108">See also</span></span>

- [<span data-ttu-id="b9ff1-109">Vue d'ensemble de la création d'images</span><span class="sxs-lookup"><span data-stu-id="b9ff1-109">Imaging Overview</span></span>](imaging-overview.md)
