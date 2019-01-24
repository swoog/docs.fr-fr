---
title: 'Procédure : Convertir un tableau d’octets en une chaîne en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- string conversion [Visual Basic], arrays
- byte arrays [Visual Basic], converting to strings
- examples [Visual Basic], strings
- arrays [Visual Basic], converting to strings
ms.assetid: d0dc8317-9ab3-4324-99f7-3f5788c0e72a
ms.openlocfilehash: 577cce6322bf80bf2abdb963f07938b1a8b5d174
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718349"
---
# <a name="how-to-convert-an-array-of-bytes-into-a-string-in-visual-basic"></a>Procédure : Convertir un tableau d’octets en une chaîne en Visual Basic
Cette rubrique montre comment convertir les octets à partir d’un tableau d’octets en une chaîne.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise le <xref:System.Text.Encoding.GetString%2A> méthode de la <xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType> classe pour convertir tous les octets à partir d’un tableau d’octets en une chaîne de codage.  
  
 [!code-vb[VbVbalrStrings#72](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-an-array-of-bytes-into-a-string_1.vb)]  
  
 Vous pouvez choisir parmi plusieurs options d’encodage pour convertir un tableau d’octets en une chaîne :  
  
-   <xref:System.Text.Encoding.ASCII%2A?displayProperty=nameWithType>: Obtient un encodage pour le jeu de caractères ASCII (7 bits).  
  
-   <xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-16 à l’aide de l’ordre de primauté des octets.  
  
-   <xref:System.Text.Encoding.Default%2A?displayProperty=nameWithType>: Obtient un encodage pour la page de codes ANSI actuelle du système.  
  
-   <xref:System.Text.Encoding.Unicode%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-16 à l’aide de l’ordre de primauté des octets.  
  
-   <xref:System.Text.Encoding.UTF32%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-32 à l’aide de l’ordre de primauté des octets.  
  
-   <xref:System.Text.Encoding.UTF7%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-7.  
  
-   <xref:System.Text.Encoding.UTF8%2A?displayProperty=nameWithType>: Obtient un encodage pour le format UTF-8.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Text.Encoding?displayProperty=nameWithType>
- <xref:System.Text.Encoding.GetString%2A>
- [Guide pratique pour Convertir des chaînes en un tableau d’octets en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-strings-into-an-array-of-bytes.md)
