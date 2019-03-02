---
title: 'Procédure : Convertir des chaînes hexadécimales en nombres (Visual Basic)'
ms.date: 01/31/2018
helpviewer_keywords:
- numbers [Visual Basic], hexadecimals
- hexadecimals [Visual Basic], decimals
- examples [Visual Basic], string conversion
- decimals [Visual Basic], hexadecimals
- string conversion [Visual Basic], hexadecimal to numbers
ms.assetid: 76675807-eadb-4c08-bd50-e6c6ff4b8ced
ms.openlocfilehash: c8ef615b6874642fa9ad1b22fe9d7f7745d4ffde
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57200999"
---
# <a name="how-to-convert-hexadecimal-strings-to-numbers-visual-basic"></a>Procédure : Convertir des chaînes hexadécimales en nombres (Visual Basic)
Cet exemple convertit une chaîne hexadécimale en un entier à l’aide de la <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType> (méthode).  
  
## <a name="to-convert-a-hexadecimal-string-to-a-number"></a>Pour convertir une chaîne hexadécimale en un nombre  
  
-   Utilisez le <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode pour convertir le nombre exprimé en base-16 en un entier.  
  
     Le premier argument de la <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode est la chaîne à convertir. Le deuxième argument décrit la base que le nombre est exprimé ; hexadécimal est de base 16.  
  
     [!code-vb[VbVbalrStrings#62](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#62)]  

- Notez que la chaîne hexadécimale présente les restrictions suivantes :

   - Il ne peut pas inclure le `&h` préfixe.
   - Il ne peut pas inclure le `_` séparateur numérique.

   Si le préfixe ou un séparateur numérique est présente, l’appel à la <xref:System.Convert.ToInt32(System.String,System.Int32)> méthode lève un <xref:System.FormatException>.

## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Conversion.Hex%2A>
- <xref:System.Convert.ToInt32%2A?displayProperty=nameWithType>
