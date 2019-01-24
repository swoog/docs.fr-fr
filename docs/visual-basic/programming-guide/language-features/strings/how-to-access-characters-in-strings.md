---
title: 'Procédure : Accès des caractères dans les chaînes en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], accessing characters
- characters [Visual Basic], accessing in strings
ms.assetid: 02c5206c-ffab-494d-b648-3b2ea358dc34
ms.openlocfilehash: 9833b562fc0b4115448ebefb8631f0d73eb15f6f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54618920"
---
# <a name="how-to-access-characters-in-strings-in-visual-basic"></a>Procédure : Accès des caractères dans les chaînes en Visual Basic
Cet exemple montre comment utiliser le <xref:System.String.Chars%2A> propriété à laquelle accéder le caractère situé à l’emplacement spécifié dans une chaîne.  
  
## <a name="example"></a>Exemple  
 Il est parfois utile de disposer de données sur les caractères de votre chaîne et les positions de ces caractères dans votre chaîne. Vous pouvez considérer une chaîne comme un tableau de caractères (`Char` instances) ; vous pouvez récupérer un caractère particulier en faisant référence à l’index de ce caractère via la <xref:System.String.Chars%2A> propriété.  
  
 [!code-vb[VbVbalrStrings#49](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-access-characters-in-strings_1.vb)]  
  
 Le `index` paramètre de la <xref:System.String.Chars%2A> propriété est de base zéro.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Le <xref:System.String.Chars%2A> propriété retourne le caractère situé à la position spécifiée. Toutefois, certains caractères Unicode peuvent être représentés par plusieurs caractères. Pour plus d’informations sur l’utilisation des caractères Unicode, consultez [Comment : Convertir une chaîne en un tableau de caractères](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md).  
  
 Le <xref:System.String.Chars%2A> propriété lève une <xref:System.IndexOutOfRangeException> exception si le `index` paramètre est supérieur ou égal à la longueur de la chaîne, ou si elle est inférieure à zéro  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.String.Chars%2A>
- [Guide pratique pour Convertir une chaîne en un tableau de caractères](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md)
- [Conversion entre chaînes et d’autres types de données en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)
- [Chaînes](../../../../visual-basic/programming-guide/language-features/strings/index.md)
