---
title: 'Comment : accéder aux caractères dans les chaînes en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], accessing characters
- characters [Visual Basic], accessing in strings
ms.assetid: 02c5206c-ffab-494d-b648-3b2ea358dc34
ms.openlocfilehash: 48507cade639660e6ce36697975d09fb29206c20
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33649150"
---
# <a name="how-to-access-characters-in-strings-in-visual-basic"></a><span data-ttu-id="f2be4-102">Comment : accéder aux caractères dans les chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f2be4-102">How to: Access Characters in Strings in Visual Basic</span></span>
<span data-ttu-id="f2be4-103">Cet exemple montre comment utiliser le <xref:System.String.Chars%2A> propriété pour accéder au caractère à l’emplacement spécifié dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="f2be4-103">This example demonstrates how to use the <xref:System.String.Chars%2A> property to access the character at the specified location in a string.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f2be4-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2be4-104">Example</span></span>  
 <span data-ttu-id="f2be4-105">Il est parfois utile de disposer de données sur les caractères de votre chaîne ainsi que les positions de ces caractères dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f2be4-105">Sometimes it is useful to have data about the characters in your string and the positions of those characters within your string.</span></span> <span data-ttu-id="f2be4-106">Vous pouvez considérer une chaîne sous forme de tableau de caractères (`Char` instances) ; vous pouvez récupérer un caractère particulier en faisant référence à l’index de ce caractère via la <xref:System.String.Chars%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f2be4-106">You can think of a string as an array of characters (`Char` instances); you can retrieve a particular character by referencing the index of that character through the <xref:System.String.Chars%2A> property.</span></span>  
  
 [!code-vb[VbVbalrStrings#49](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-access-characters-in-strings_1.vb)]  
  
 <span data-ttu-id="f2be4-107">Le `index` paramètre de la <xref:System.String.Chars%2A> propriété est de base zéro.</span><span class="sxs-lookup"><span data-stu-id="f2be4-107">The `index` parameter of the <xref:System.String.Chars%2A> property is zero-based.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="f2be4-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="f2be4-108">Robust Programming</span></span>  
 <span data-ttu-id="f2be4-109">Le <xref:System.String.Chars%2A> propriété retourne le caractère situé à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f2be4-109">The <xref:System.String.Chars%2A> property returns the character at the specified position.</span></span> <span data-ttu-id="f2be4-110">Toutefois, certains caractères Unicode peuvent être représentés par plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="f2be4-110">However, some Unicode characters can be represented by more than one character.</span></span> <span data-ttu-id="f2be4-111">Pour plus d’informations sur l’utilisation des caractères Unicode, consultez [Comment : convertir une chaîne en un tableau de caractères](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md).</span><span class="sxs-lookup"><span data-stu-id="f2be4-111">For more information on how to work with Unicode characters, see [How to: Convert a String to an Array of Characters](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md).</span></span>  
  
 <span data-ttu-id="f2be4-112">Le <xref:System.String.Chars%2A> propriété lève une <xref:System.IndexOutOfRangeException> exception si le `index` paramètre est supérieur ou égal à la longueur de la chaîne, ou si elle est inférieure à zéro</span><span class="sxs-lookup"><span data-stu-id="f2be4-112">The <xref:System.String.Chars%2A> property throws an <xref:System.IndexOutOfRangeException> exception if the `index` parameter is greater than or equal to the length of the string, or if it is less than zero</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2be4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2be4-113">See Also</span></span>  
 <xref:System.String.Chars%2A>  
 [<span data-ttu-id="f2be4-114">Guide pratique : convertir une chaîne en tableau de caractères</span><span class="sxs-lookup"><span data-stu-id="f2be4-114">How to: Convert a String to an Array of Characters</span></span>](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md)  
 [<span data-ttu-id="f2be4-115">Conversion entre chaînes et d’autres types de données en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f2be4-115">Converting Between Strings and Other Data Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)  
 [<span data-ttu-id="f2be4-116">Chaînes</span><span class="sxs-lookup"><span data-stu-id="f2be4-116">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
