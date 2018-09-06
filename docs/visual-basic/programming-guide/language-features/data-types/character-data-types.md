---
title: Types de données caractères (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- data types [Visual Basic], character
- String data type [Visual Basic], character data types
- character data types [Visual Basic]
- Char data type [Visual Basic], character data types
- data types [Visual Basic], choosing
ms.assetid: 902479ef-1679-47fc-9911-0c1c5008226c
ms.openlocfilehash: 3b031c6e3dc04637128f95ca8e922d3298981287
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863201"
---
# <a name="character-data-types-visual-basic"></a><span data-ttu-id="b239c-102">Types de données caractères (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b239c-102">Character Data Types (Visual Basic)</span></span>
<span data-ttu-id="b239c-103">Visual Basic fournit *les types de données character* à gérer avec des caractères imprimables et affichables.</span><span class="sxs-lookup"><span data-stu-id="b239c-103">Visual Basic provides *character data types* to deal with printable and displayable characters.</span></span> <span data-ttu-id="b239c-104">Reconnaissent les caractères Unicode, `Char` contient un caractère tandis que `String` contient un nombre indéfini de caractères.</span><span class="sxs-lookup"><span data-stu-id="b239c-104">While they both deal with Unicode characters, `Char` holds a single character whereas `String` contains an indefinite number of characters.</span></span>  
  
 <span data-ttu-id="b239c-105">Pour une table qui affiche une comparaison côte à côte des types de données Visual Basic, consultez [Types de données](../../../../visual-basic/language-reference/data-types/index.md).</span><span class="sxs-lookup"><span data-stu-id="b239c-105">For a table that displays a side-by-side comparison of the Visual Basic data types, see [Data Types](../../../../visual-basic/language-reference/data-types/index.md).</span></span>  
  
## <a name="char-type"></a><span data-ttu-id="b239c-106">Char, Type</span><span class="sxs-lookup"><span data-stu-id="b239c-106">Char Type</span></span>  
 <span data-ttu-id="b239c-107">Le `Char` type de données est un caractère de Unicode sur deux octets (16 bits) unique.</span><span class="sxs-lookup"><span data-stu-id="b239c-107">The `Char` data type is a single two-byte (16-bit) Unicode character.</span></span> <span data-ttu-id="b239c-108">Si une variable stocke toujours exactement un caractère, déclarez-le en tant que `Char`.</span><span class="sxs-lookup"><span data-stu-id="b239c-108">If a variable always stores exactly one character, declare it as `Char`.</span></span> <span data-ttu-id="b239c-109">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b239c-109">For example:</span></span>  
  
 [!code-vb[VbVbalrCharTypes#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrchartypes/vb/module1.vb#1)]
  
 <span data-ttu-id="b239c-110">Chaque valeur possible dans un `Char` ou `String` variable est un *point de code*, ou code de caractère, dans le jeu de caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="b239c-110">Each possible value in a `Char` or `String` variable is a *code point*, or character code, in the Unicode character set.</span></span> <span data-ttu-id="b239c-111">Les caractères Unicode incluent le jeu de caractères ASCII base, différents autres lettres de l’alphabet, les accents, les symboles monétaires, fractions, les signes diacritiques et symboles mathématiques et techniques.</span><span class="sxs-lookup"><span data-stu-id="b239c-111">Unicode characters include the basic ASCII character set, various other alphabet letters, accents, currency symbols, fractions, diacritics, and mathematical and technical symbols.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b239c-112">Les points de code D800 à DFFF (55 296 à 55 551 décimal) pour les réserves de ressources de jeu de caractères Unicode *paires de substitution*, qui requiert des deux valeurs 16 bits pour représenter un seul point de code.</span><span class="sxs-lookup"><span data-stu-id="b239c-112">The Unicode character set reserves the code points D800 through DFFF (55296 through 55551 decimal) for *surrogate pairs*, which require two 16-bit values to represent a single code point.</span></span> <span data-ttu-id="b239c-113">Un `Char` variable ne peut pas contenir une paire de substitution et un `String` utilise deux positions pour contenir une paire.</span><span class="sxs-lookup"><span data-stu-id="b239c-113">A `Char` variable cannot hold a surrogate pair, and a `String` uses two positions to hold such a pair.</span></span>  
  
 <span data-ttu-id="b239c-114">Pour plus d’informations, consultez [Type de données Char](../../../../visual-basic/language-reference/data-types/char-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="b239c-114">For more information, see [Char Data Type](../../../../visual-basic/language-reference/data-types/char-data-type.md).</span></span>  
  
## <a name="string-type"></a><span data-ttu-id="b239c-115">Type de chaîne</span><span class="sxs-lookup"><span data-stu-id="b239c-115">String Type</span></span>  
 <span data-ttu-id="b239c-116">Le `String` type de données est une séquence de zéro ou plusieurs caractères Unicode à deux octets (16 bits).</span><span class="sxs-lookup"><span data-stu-id="b239c-116">The `String` data type is a sequence of zero or more two-byte (16-bit) Unicode characters.</span></span> <span data-ttu-id="b239c-117">Si une variable peut contenir un nombre indéfini de caractères, déclarez-le en tant que `String`.</span><span class="sxs-lookup"><span data-stu-id="b239c-117">If a variable can contain an indefinite number of characters, declare it as `String`.</span></span> <span data-ttu-id="b239c-118">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b239c-118">For example:</span></span>  
  
 [!code-vb[VbVbalrCharTypes#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrchartypes/vb/module1.vb#2)]
  
 <span data-ttu-id="b239c-119">Pour plus d’informations, consultez [Type de données String](../../../../visual-basic/language-reference/data-types/string-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="b239c-119">For more information, see [String Data Type](../../../../visual-basic/language-reference/data-types/string-data-type.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b239c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b239c-120">See Also</span></span>  
 [<span data-ttu-id="b239c-121">Types de données élémentaires</span><span class="sxs-lookup"><span data-stu-id="b239c-121">Elementary Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)  
 [<span data-ttu-id="b239c-122">Types de données composites</span><span class="sxs-lookup"><span data-stu-id="b239c-122">Composite Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)  
 [<span data-ttu-id="b239c-123">Types génériques en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b239c-123">Generic Types in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)  
 [<span data-ttu-id="b239c-124">Types valeur et types référence</span><span class="sxs-lookup"><span data-stu-id="b239c-124">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)  
 [<span data-ttu-id="b239c-125">Conversions de type en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b239c-125">Type Conversions in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)  
 [<span data-ttu-id="b239c-126">Dépannage des types de données</span><span class="sxs-lookup"><span data-stu-id="b239c-126">Troubleshooting Data Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 [<span data-ttu-id="b239c-127">Caractères de type</span><span class="sxs-lookup"><span data-stu-id="b239c-127">Type Characters</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)
