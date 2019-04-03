---
title: 'Procédure : Convertir une chaîne en un tableau de caractères en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- character arrays [Visual Basic], converting strings
- arrays [Visual Basic], converting strings to
- examples [Visual Basic], string conversion
- strings [Visual Basic], converting to arrays
- string conversion [Visual Basic], arrays
ms.assetid: 1b54b686-ab29-413b-adce-6bd5422376eb
ms.openlocfilehash: 921d7ad62545d3a29870aee6c6b354fdadeb0500
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58823309"
---
# <a name="how-to-convert-a-string-to-an-array-of-characters-in-visual-basic"></a>Procédure : Convertir une chaîne en un tableau de caractères en Visual Basic
Il est parfois utile de disposer de données sur les caractères de votre chaîne et les positions de ces caractères dans votre chaîne, comme lorsque vous analysez une chaîne. Cet exemple montre comment vous pouvez obtenir un tableau de caractères dans une chaîne en appelant la chaîne <xref:System.String.ToCharArray%2A> (méthode).  
  
## <a name="example"></a>Exemple  
 Cet exemple montre comment fractionner une chaîne en un `Char` tableau et comment fractionner une chaîne en un `String` tableau de ses caractères de texte Unicode. La raison de cette distinction est que les caractères de texte Unicode peuvent être composés de deux ou plusieurs `Char` caractères (par exemple une paire de substitution ou une combinaison séquence de caractères). Pour plus d’informations, consultez <xref:System.Globalization.TextElementEnumerator> et [la norme Unicode](https://www.unicode.org/standard/standard.html).  
  
 [!code-vb[VbVbalrStrings#75](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class4.vb#75)]  
  
## <a name="example"></a>Exemple  
 Il est plus difficile de fractionner une chaîne en ses caractères de texte Unicode, mais cela est nécessaire si vous avez besoin d’informations sur la représentation visuelle d’une chaîne. Cet exemple utilise le <xref:System.Globalization.StringInfo.SubstringByTextElements%2A> méthode pour obtenir des informations sur les caractères de texte Unicode qui composent une chaîne.  
  
 [!code-vb[VbVbalrStrings#76](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class4.vb#76)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.String.Chars%2A>
- <xref:System.Globalization.StringInfo?displayProperty=nameWithType>
- [Guide pratique pour Accès des caractères dans les chaînes](../../../../visual-basic/programming-guide/language-features/strings/how-to-access-characters-in-strings.md)
- [Conversion entre chaînes et d’autres types de données en Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)
- [Chaînes](../../../../visual-basic/programming-guide/language-features/strings/index.md)
