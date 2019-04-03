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
# <a name="how-to-convert-a-string-to-an-array-of-characters-in-visual-basic"></a><span data-ttu-id="b2754-102">Procédure : Convertir une chaîne en un tableau de caractères en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b2754-102">How to: Convert a String to an Array of Characters in Visual Basic</span></span>
<span data-ttu-id="b2754-103">Il est parfois utile de disposer de données sur les caractères de votre chaîne et les positions de ces caractères dans votre chaîne, comme lorsque vous analysez une chaîne.</span><span class="sxs-lookup"><span data-stu-id="b2754-103">Sometimes it is useful to have data about the characters in your string and the positions of those characters within your string, such as when you are parsing a string.</span></span> <span data-ttu-id="b2754-104">Cet exemple montre comment vous pouvez obtenir un tableau de caractères dans une chaîne en appelant la chaîne <xref:System.String.ToCharArray%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="b2754-104">This example shows how you can get an array of the characters in a string by calling the string's <xref:System.String.ToCharArray%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b2754-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="b2754-105">Example</span></span>  
 <span data-ttu-id="b2754-106">Cet exemple montre comment fractionner une chaîne en un `Char` tableau et comment fractionner une chaîne en un `String` tableau de ses caractères de texte Unicode.</span><span class="sxs-lookup"><span data-stu-id="b2754-106">This example demonstrates how to split a string into a `Char` array, and how to split a string into a `String` array of its Unicode text characters.</span></span> <span data-ttu-id="b2754-107">La raison de cette distinction est que les caractères de texte Unicode peuvent être composés de deux ou plusieurs `Char` caractères (par exemple une paire de substitution ou une combinaison séquence de caractères).</span><span class="sxs-lookup"><span data-stu-id="b2754-107">The reason for this distinction is that Unicode text characters can be composed of two or more `Char` characters (such as a surrogate pair or a combining character sequence).</span></span> <span data-ttu-id="b2754-108">Pour plus d’informations, consultez <xref:System.Globalization.TextElementEnumerator> et [la norme Unicode](https://www.unicode.org/standard/standard.html).</span><span class="sxs-lookup"><span data-stu-id="b2754-108">For more information, see <xref:System.Globalization.TextElementEnumerator> and [The Unicode Standard](https://www.unicode.org/standard/standard.html).</span></span>  
  
 [!code-vb[VbVbalrStrings#75](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class4.vb#75)]  
  
## <a name="example"></a><span data-ttu-id="b2754-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="b2754-109">Example</span></span>  
 <span data-ttu-id="b2754-110">Il est plus difficile de fractionner une chaîne en ses caractères de texte Unicode, mais cela est nécessaire si vous avez besoin d’informations sur la représentation visuelle d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="b2754-110">It is more difficult to split a string into its Unicode text characters, but this is necessary if you need information about the visual representation of a string.</span></span> <span data-ttu-id="b2754-111">Cet exemple utilise le <xref:System.Globalization.StringInfo.SubstringByTextElements%2A> méthode pour obtenir des informations sur les caractères de texte Unicode qui composent une chaîne.</span><span class="sxs-lookup"><span data-stu-id="b2754-111">This example uses the <xref:System.Globalization.StringInfo.SubstringByTextElements%2A> method to get information about the Unicode text characters that make up a string.</span></span>  
  
 [!code-vb[VbVbalrStrings#76](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class4.vb#76)]  
  
## <a name="see-also"></a><span data-ttu-id="b2754-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2754-112">See also</span></span>

- <xref:System.String.Chars%2A>
- <xref:System.Globalization.StringInfo?displayProperty=nameWithType>
- [<span data-ttu-id="b2754-113">Guide pratique pour Accès des caractères dans les chaînes</span><span class="sxs-lookup"><span data-stu-id="b2754-113">How to: Access Characters in Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/how-to-access-characters-in-strings.md)
- [<span data-ttu-id="b2754-114">Conversion entre chaînes et d’autres types de données en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b2754-114">Converting Between Strings and Other Data Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)
- [<span data-ttu-id="b2754-115">Chaînes</span><span class="sxs-lookup"><span data-stu-id="b2754-115">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
