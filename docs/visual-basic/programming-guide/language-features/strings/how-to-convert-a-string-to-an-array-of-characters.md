---
title: 'Comment : convertir une chaîne en tableau de caractères en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- character arrays [Visual Basic], converting strings
- arrays [Visual Basic], converting strings to
- examples [Visual Basic], string conversion
- strings [Visual Basic], converting to arrays
- string conversion [Visual Basic], arrays
ms.assetid: 1b54b686-ab29-413b-adce-6bd5422376eb
ms.openlocfilehash: c109143601e304b1ec15a60c71d65fe6bd15aae8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33648617"
---
# <a name="how-to-convert-a-string-to-an-array-of-characters-in-visual-basic"></a><span data-ttu-id="87392-102">Comment : convertir une chaîne en tableau de caractères en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="87392-102">How to: Convert a String to an Array of Characters in Visual Basic</span></span>
<span data-ttu-id="87392-103">Il est parfois utile de disposer de données sur les caractères de votre chaîne ainsi que les positions de ces caractères dans la chaîne, telles que lorsque vous analysez une chaîne.</span><span class="sxs-lookup"><span data-stu-id="87392-103">Sometimes it is useful to have data about the characters in your string and the positions of those characters within your string, such as when you are parsing a string.</span></span> <span data-ttu-id="87392-104">Cet exemple montre comment vous pouvez obtenir un tableau de caractères dans une chaîne en appelant la chaîne <xref:System.String.ToCharArray%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="87392-104">This example shows how you can get an array of the characters in a string by calling the string's <xref:System.String.ToCharArray%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="87392-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="87392-105">Example</span></span>  
 <span data-ttu-id="87392-106">Cet exemple montre comment fractionner une chaîne en un `Char` tableau et comment fractionner une chaîne en un `String` tableau de caractères Unicode texte.</span><span class="sxs-lookup"><span data-stu-id="87392-106">This example demonstrates how to split a string into a `Char` array, and how to split a string into a `String` array of its Unicode text characters.</span></span> <span data-ttu-id="87392-107">La raison de cette distinction est que les caractères de texte Unicode peuvent être composés de deux ou plusieurs `Char` caractères (par exemple une paire de substitution ou une combinaison séquence de caractères).</span><span class="sxs-lookup"><span data-stu-id="87392-107">The reason for this distinction is that Unicode text characters can be composed of two or more `Char` characters (such as a surrogate pair or a combining character sequence).</span></span> <span data-ttu-id="87392-108">Pour plus d’informations, consultez <xref:System.Globalization.TextElementEnumerator> et « La norme Unicode » sur http://www.unicode.org.</span><span class="sxs-lookup"><span data-stu-id="87392-108">For more information, see <xref:System.Globalization.TextElementEnumerator> and "The Unicode Standard" at http://www.unicode.org.</span></span>  
  
 [!code-vb[VbVbalrStrings#75](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-a-string-to-an-array-of-characters_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="87392-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="87392-109">Example</span></span>  
 <span data-ttu-id="87392-110">Il est plus difficile de fractionner une chaîne en ses caractères de texte Unicode, mais cette opération est nécessaire si vous avez besoin d’informations sur la représentation visuelle d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="87392-110">It is more difficult to split a string into its Unicode text characters, but this is necessary if you need information about the visual representation of a string.</span></span> <span data-ttu-id="87392-111">Cet exemple utilise la <xref:System.Globalization.StringInfo.SubstringByTextElements%2A> méthode pour obtenir des informations sur les caractères de texte Unicode qui composent une chaîne.</span><span class="sxs-lookup"><span data-stu-id="87392-111">This example uses the <xref:System.Globalization.StringInfo.SubstringByTextElements%2A> method to get information about the Unicode text characters that make up a string.</span></span>  
  
 [!code-vb[VbVbalrStrings#76](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-convert-a-string-to-an-array-of-characters_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="87392-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87392-112">See Also</span></span>  
 <xref:System.String.Chars%2A>  
 <xref:System.Globalization.StringInfo?displayProperty=nameWithType>  
 [<span data-ttu-id="87392-113">Guide pratique : accéder aux caractères dans les chaînes</span><span class="sxs-lookup"><span data-stu-id="87392-113">How to: Access Characters in Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/how-to-access-characters-in-strings.md)  
 [<span data-ttu-id="87392-114">Conversion entre chaînes et d’autres types de données en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="87392-114">Converting Between Strings and Other Data Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)  
 [<span data-ttu-id="87392-115">Chaînes</span><span class="sxs-lookup"><span data-stu-id="87392-115">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
