---
title: 'Procédure : Convertir des chaînes en un tableau d’octets en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- string conversion [Visual Basic], arrays
- arrays [Visual Basic], converting strings to
- byte arrays
- examples [Visual Basic], string conversion
- arrays [Visual Basic], byte arrays
ms.assetid: f477d35c-a3fc-4a30-b1d4-cd0d353aae1d
ms.openlocfilehash: a96664f308a711d440f063627665283c5b7fc264
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56967501"
---
# <a name="how-to-convert-strings-into-an-array-of-bytes-in-visual-basic"></a>Procédure : Convertir des chaînes en un tableau d’octets en Visual Basic
Cette rubrique montre comment convertir une chaîne en un tableau d’octets.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Text.Encoding.GetBytes%2A> méthode de la <xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType> classe pour convertir une chaîne en un tableau d’octets d’encodage.  
  
 [!code-vb[VbVbalrStrings#74](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#74)]  
  
 Vous pouvez choisir parmi plusieurs options d’encodage pour convertir une chaîne en tableau d’octets :  
  
-   <xref:System.Text.Encoding.ASCII%2A?displayProperty=nameWithType>: Obtient un encodage pour le jeu de caractères ASCII (7 bits).  
  
-   <xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-16 à l’aide de l’ordre de primauté des octets.  
  
-   <xref:System.Text.Encoding.Default%2A?displayProperty=nameWithType>: Obtient un encodage pour la page de codes ANSI actuelle du système.  
  
-   <xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-16 à l’aide de l’ordre de primauté des octets.  
  
-   <xref:System.Text.Encoding.UTF32%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-32 à l’aide de l’ordre de primauté des octets.  
  
-   <xref:System.Text.Encoding.UTF7%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-7.  
  
-   <xref:System.Text.Encoding.UTF8%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-8.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Text.Encoding?displayProperty=nameWithType>
- <xref:System.Text.Encoding.GetBytes%2A>
- [Guide pratique pour Convertir un tableau d’octets en une chaîne en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-an-array-of-bytes-into-a-string.md)
