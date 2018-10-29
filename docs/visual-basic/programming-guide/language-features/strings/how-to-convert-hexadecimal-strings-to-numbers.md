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
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50197546"
---
# <a name="how-to-convert-hexadecimal-strings-to-numbers-visual-basic"></a>Comment : convertir des chaînes hexadécimales en nombres (Visual Basic)
Cet exemple convertit une chaîne hexadécimale en un entier à l’aide de la <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType> (méthode).  
  
## <a name="to-convert-a-hexadecimal-string-to-a-number"></a>Pour convertir une chaîne hexadécimale en un nombre  
  
-   Utilisez le <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode pour convertir le nombre exprimé en base-16 en un entier.  
  
     Le premier argument de la <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode est la chaîne à convertir. Le deuxième argument décrit la base que le nombre est exprimé ; hexadécimal est de base 16.  
  
     [!code-vb[HexConversion](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-hexadecimal-strings-to-numbers_1.vb)]  

- Notez que la chaîne hexadécimale présente les restrictions suivantes :

   - Il ne peut pas inclure le `&h` préfixe.
   - Il ne peut pas inclure le `_` séparateur numérique.

   Si le préfixe ou un séparateur numérique est présente, l’appel à la <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode lève un <xref:System.FormatException>.

## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.Conversion.Hex%2A>  
 <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType>
