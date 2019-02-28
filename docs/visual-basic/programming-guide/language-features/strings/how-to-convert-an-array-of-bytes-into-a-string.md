---
title: 'Procédure : Convertir un tableau d’octets en une chaîne en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- string conversion [Visual Basic], arrays
- byte arrays [Visual Basic], converting to strings
- examples [Visual Basic], strings
- arrays [Visual Basic], converting to strings
ms.assetid: d0dc8317-9ab3-4324-99f7-3f5788c0e72a
ms.openlocfilehash: cd091d743b04ef9d9709bde2b5a1205f3d7ae292
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56979506"
---
# <a name="how-to-convert-an-array-of-bytes-into-a-string-in-visual-basic"></a><span data-ttu-id="cab98-102">Procédure : Convertir un tableau d’octets en une chaîne en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cab98-102">How to: Convert an Array of Bytes into a String in Visual Basic</span></span>
<span data-ttu-id="cab98-103">Cette rubrique montre comment convertir les octets à partir d’un tableau d’octets en une chaîne.</span><span class="sxs-lookup"><span data-stu-id="cab98-103">This topic shows how to convert the bytes from a byte array into a string.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cab98-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="cab98-104">Example</span></span>  
 <span data-ttu-id="cab98-105">Cet exemple utilise le <xref:System.Text.Encoding.GetString%2A> méthode de la <xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType> classe pour convertir tous les octets à partir d’un tableau d’octets en une chaîne de codage.</span><span class="sxs-lookup"><span data-stu-id="cab98-105">This example uses the <xref:System.Text.Encoding.GetString%2A> method of the <xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType> encoding class to convert all the bytes from a byte array into a string.</span></span>  
  
 [!code-vb[VbVbalrStrings#72](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#72)]  
  
 <span data-ttu-id="cab98-106">Vous pouvez choisir parmi plusieurs options d’encodage pour convertir un tableau d’octets en une chaîne :</span><span class="sxs-lookup"><span data-stu-id="cab98-106">You can choose from several encoding options to convert a byte array into a string:</span></span>  
  
-   <span data-ttu-id="cab98-107"><xref:System.Text.Encoding.ASCII%2A?displayProperty=nameWithType>: Obtient un encodage pour le jeu de caractères ASCII (7 bits).</span><span class="sxs-lookup"><span data-stu-id="cab98-107"><xref:System.Text.Encoding.ASCII%2A?displayProperty=nameWithType>: Gets an encoding for the ASCII (7-bit) character set.</span></span>  
  
-   <span data-ttu-id="cab98-108"><xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-16 à l’aide de l’ordre de primauté des octets.</span><span class="sxs-lookup"><span data-stu-id="cab98-108"><xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-16 format using the big-endian byte order.</span></span>  
  
-   <span data-ttu-id="cab98-109"><xref:System.Text.Encoding.Default%2A?displayProperty=nameWithType>: Obtient un encodage pour la page de codes ANSI actuelle du système.</span><span class="sxs-lookup"><span data-stu-id="cab98-109"><xref:System.Text.Encoding.Default%2A?displayProperty=nameWithType>: Gets an encoding for the system's current ANSI code page.</span></span>  
  
-   <span data-ttu-id="cab98-110"><xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-16 à l’aide de l’ordre de primauté des octets.</span><span class="sxs-lookup"><span data-stu-id="cab98-110"><xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-16 format using the little-endian byte order.</span></span>  
  
-   <span data-ttu-id="cab98-111"><xref:System.Text.Encoding.UTF32%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-32 à l’aide de l’ordre de primauté des octets.</span><span class="sxs-lookup"><span data-stu-id="cab98-111"><xref:System.Text.Encoding.UTF32%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-32 format using the little-endian byte order.</span></span>  
  
-   <span data-ttu-id="cab98-112"><xref:System.Text.Encoding.UTF7%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-7.</span><span class="sxs-lookup"><span data-stu-id="cab98-112"><xref:System.Text.Encoding.UTF7%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-7 format.</span></span>  
  
-   <span data-ttu-id="cab98-113"><xref:System.Text.Encoding.UTF8%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-8.</span><span class="sxs-lookup"><span data-stu-id="cab98-113"><xref:System.Text.Encoding.UTF8%2A?displayProperty=nameWithType>: Gets an encoding for the UTF-8 format.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cab98-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cab98-114">See also</span></span>
- <xref:System.Text.Encoding?displayProperty=nameWithType>
- <xref:System.Text.Encoding.GetString%2A>
- [<span data-ttu-id="cab98-115">Guide pratique pour Convertir des chaînes en un tableau d’octets en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cab98-115">How to: Convert Strings into an Array of Bytes in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-strings-into-an-array-of-bytes.md)
