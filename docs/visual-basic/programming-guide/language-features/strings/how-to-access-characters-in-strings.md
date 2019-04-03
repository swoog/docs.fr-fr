---
title: 'Procédure : Accès des caractères dans les chaînes en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], accessing characters
- characters [Visual Basic], accessing in strings
ms.assetid: 02c5206c-ffab-494d-b648-3b2ea358dc34
ms.openlocfilehash: 840a769b0bb322ef7b878a312437c5ec200ab074
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834489"
---
# <a name="how-to-access-characters-in-strings-in-visual-basic"></a><span data-ttu-id="7d7d8-102">Procédure : Accès des caractères dans les chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7d7d8-102">How to: Access Characters in Strings in Visual Basic</span></span>
<span data-ttu-id="7d7d8-103">Cet exemple montre comment utiliser le <xref:System.String.Chars%2A> propriété à laquelle accéder le caractère situé à l’emplacement spécifié dans une chaîne.</span><span class="sxs-lookup"><span data-stu-id="7d7d8-103">This example demonstrates how to use the <xref:System.String.Chars%2A> property to access the character at the specified location in a string.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7d7d8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="7d7d8-104">Example</span></span>  
 <span data-ttu-id="7d7d8-105">Il est parfois utile de disposer de données sur les caractères de votre chaîne et les positions de ces caractères dans votre chaîne.</span><span class="sxs-lookup"><span data-stu-id="7d7d8-105">Sometimes it is useful to have data about the characters in your string and the positions of those characters within your string.</span></span> <span data-ttu-id="7d7d8-106">Vous pouvez considérer une chaîne comme un tableau de caractères (`Char` instances) ; vous pouvez récupérer un caractère particulier en faisant référence à l’index de ce caractère via la <xref:System.String.Chars%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="7d7d8-106">You can think of a string as an array of characters (`Char` instances); you can retrieve a particular character by referencing the index of that character through the <xref:System.String.Chars%2A> property.</span></span>  
  
 [!code-vb[VbVbalrStrings#49](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#49)]  
  
 <span data-ttu-id="7d7d8-107">Le `index` paramètre de la <xref:System.String.Chars%2A> propriété est de base zéro.</span><span class="sxs-lookup"><span data-stu-id="7d7d8-107">The `index` parameter of the <xref:System.String.Chars%2A> property is zero-based.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="7d7d8-108">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="7d7d8-108">Robust Programming</span></span>  
 <span data-ttu-id="7d7d8-109">Le <xref:System.String.Chars%2A> propriété retourne le caractère situé à la position spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7d7d8-109">The <xref:System.String.Chars%2A> property returns the character at the specified position.</span></span> <span data-ttu-id="7d7d8-110">Toutefois, certains caractères Unicode peuvent être représentés par plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="7d7d8-110">However, some Unicode characters can be represented by more than one character.</span></span> <span data-ttu-id="7d7d8-111">Pour plus d’informations sur l’utilisation des caractères Unicode, consultez [Comment : Convertir une chaîne en un tableau de caractères](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md).</span><span class="sxs-lookup"><span data-stu-id="7d7d8-111">For more information on how to work with Unicode characters, see [How to: Convert a String to an Array of Characters](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md).</span></span>  
  
 <span data-ttu-id="7d7d8-112">Le <xref:System.String.Chars%2A> propriété lève une <xref:System.IndexOutOfRangeException> exception si le `index` paramètre est supérieur ou égal à la longueur de la chaîne, ou si elle est inférieure à zéro</span><span class="sxs-lookup"><span data-stu-id="7d7d8-112">The <xref:System.String.Chars%2A> property throws an <xref:System.IndexOutOfRangeException> exception if the `index` parameter is greater than or equal to the length of the string, or if it is less than zero</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d7d8-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d7d8-113">See also</span></span>

- <xref:System.String.Chars%2A>
- [<span data-ttu-id="7d7d8-114">Guide pratique pour Convertir une chaîne en un tableau de caractères</span><span class="sxs-lookup"><span data-stu-id="7d7d8-114">How to: Convert a String to an Array of Characters</span></span>](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-a-string-to-an-array-of-characters.md)
- [<span data-ttu-id="7d7d8-115">Conversion entre chaînes et d’autres types de données en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7d7d8-115">Converting Between Strings and Other Data Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/converting-between-strings-and-other-data-types.md)
- [<span data-ttu-id="7d7d8-116">Chaînes</span><span class="sxs-lookup"><span data-stu-id="7d7d8-116">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
