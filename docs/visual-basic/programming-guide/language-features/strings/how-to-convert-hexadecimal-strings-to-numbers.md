---
title: 'Comment : convertir des chaînes hexadécimales en nombres (Visual Basic)'
ms.date: 01/31/2018
helpviewer_keywords:
- numbers [Visual Basic], hexadecimals
- hexadecimals [Visual Basic], decimals
- examples [Visual Basic], string conversion
- decimals [Visual Basic], hexadecimals
- string conversion [Visual Basic], hexadecimal to numbers
ms.assetid: 76675807-eadb-4c08-bd50-e6c6ff4b8ced
ms.openlocfilehash: 65184bbb742ad549a8398d55dc7bdeed05a9d973
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50048552"
---
# <a name="how-to-convert-hexadecimal-strings-to-numbers-visual-basic"></a><span data-ttu-id="eb78c-102">Comment : convertir des chaînes hexadécimales en nombres (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="eb78c-102">How to: Convert Hexadecimal Strings to Numbers (Visual Basic)</span></span>
<span data-ttu-id="eb78c-103">Cet exemple convertit une chaîne hexadécimale en un entier à l’aide de la <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="eb78c-103">This example converts a hexadecimal string to an integer using the <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType> method.</span></span>  
  
## <a name="to-convert-a-hexadecimal-string-to-a-number"></a><span data-ttu-id="eb78c-104">Pour convertir une chaîne hexadécimale en un nombre</span><span class="sxs-lookup"><span data-stu-id="eb78c-104">To convert a hexadecimal string to a number</span></span>  
  
-   <span data-ttu-id="eb78c-105">Utilisez le <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode pour convertir le nombre exprimé en base-16 en un entier.</span><span class="sxs-lookup"><span data-stu-id="eb78c-105">Use the <xref:System.Convert.ToInt32(System.String,System.Int32)> method to convert the number expressed in base-16 to an integer.</span></span>  
  
     <span data-ttu-id="eb78c-106">Le premier argument de la <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode est la chaîne à convertir.</span><span class="sxs-lookup"><span data-stu-id="eb78c-106">The first argument of the <xref:System.Convert.ToInt32(System.String,System.Int32)> method is the string to convert.</span></span> <span data-ttu-id="eb78c-107">Le deuxième argument décrit la base que le nombre est exprimé ; hexadécimal est de base 16.</span><span class="sxs-lookup"><span data-stu-id="eb78c-107">The second argument describes what base the number is expressed in; hexadecimal is base 16.</span></span>  
  
     [!code-vb[HexConversion](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-hexadecimal-strings-to-numbers_1.vb)]  

- <span data-ttu-id="eb78c-108">Notez que la chaîne hexadécimale présente les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="eb78c-108">Note that the hexadecimal string has the following restrictions:</span></span>

   - <span data-ttu-id="eb78c-109">Il ne peut pas inclure le `&h` préfixe.</span><span class="sxs-lookup"><span data-stu-id="eb78c-109">It cannot include the `&h` prefix.</span></span>
   - <span data-ttu-id="eb78c-110">Il ne peut pas inclure le `_` séparateur numérique.</span><span class="sxs-lookup"><span data-stu-id="eb78c-110">It cannot include the `_` digit separator.</span></span>

   <span data-ttu-id="eb78c-111">Si le préfixe ou un séparateur numérique est présente, l’appel à la <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode lève un <xref:System.FormatException>.</span><span class="sxs-lookup"><span data-stu-id="eb78c-111">If the prefix or a digit separator is present, the call to the <xref:System.Convert.ToInt32(System.String,System.Int32)> method throws a <xref:System.FormatException>.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb78c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb78c-112">See Also</span></span>  
 <xref:Microsoft.VisualBasic.Conversion.Hex%2A>  
 <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType>
