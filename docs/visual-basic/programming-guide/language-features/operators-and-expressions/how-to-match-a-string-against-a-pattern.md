---
title: 'Procédure : Faire correspondre une chaîne à un modèle (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- comparison operators [Visual Basic], comparing strings
- pattern matching
- strings [Visual Basic], comparing
- string comparison [Visual Basic], operators
- Visual Basic code, operators
- pattern matching [Visual Basic], string comparison
- string comparison [Visual Basic]
- Like operator [Visual Basic], pattern matching
- pattern matching, empty strings
- operators [Visual Basic], comparison
ms.assetid: 19a83804-b5af-4739-928b-ac93e64e457f
ms.openlocfilehash: c14aa35ce15549ad9eccabe2330a7c43b6795140
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59316269"
---
# <a name="how-to-match-a-string-against-a-pattern-visual-basic"></a><span data-ttu-id="38c0c-102">Procédure : Faire correspondre une chaîne à un modèle (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="38c0c-102">How to: Match a String against a Pattern (Visual Basic)</span></span>
<span data-ttu-id="38c0c-103">Si vous souhaitez savoir si une expression de la [Type de données String](../../../../visual-basic/language-reference/data-types/string-data-type.md) satisfait à un modèle, vous pouvez ensuite utiliser le [opérateur Like](../../../../visual-basic/language-reference/operators/like-operator.md).</span><span class="sxs-lookup"><span data-stu-id="38c0c-103">If you want to find out if an expression of the [String Data Type](../../../../visual-basic/language-reference/data-types/string-data-type.md) satisfies a pattern, then you can use the [Like Operator](../../../../visual-basic/language-reference/operators/like-operator.md).</span></span>  
  
 <span data-ttu-id="38c0c-104">`Like` accepte deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="38c0c-104">`Like` takes two operands.</span></span> <span data-ttu-id="38c0c-105">L’opérande gauche est une expression de chaîne, et l’opérande de droite est une chaîne contenant le modèle à utiliser pour la correspondance.</span><span class="sxs-lookup"><span data-stu-id="38c0c-105">The left operand is a string expression, and the right operand is a string containing the pattern to be used for matching.</span></span> <span data-ttu-id="38c0c-106">`Like` Retourne un `Boolean` valeur indiquant si l’expression de chaîne est conforme au modèle.</span><span class="sxs-lookup"><span data-stu-id="38c0c-106">`Like` returns a `Boolean` value indicating whether the string expression satisfies the pattern.</span></span>  
  
 <span data-ttu-id="38c0c-107">Vous pouvez faire correspondre chaque caractère de l’expression de chaîne avec un caractère spécifique, un caractère générique, une liste de caractères ou une plage de caractères.</span><span class="sxs-lookup"><span data-stu-id="38c0c-107">You can match each character in the string expression against a specific character, a wildcard character, a character list, or a character range.</span></span> <span data-ttu-id="38c0c-108">Les positions des spécifications dans la chaîne de modèle correspondent vers les positions des caractères à mettre en correspondance dans l’expression de chaîne.</span><span class="sxs-lookup"><span data-stu-id="38c0c-108">The positions of the specifications in the pattern string correspond to the positions of the characters to be matched in the string expression.</span></span>  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-specific-character"></a><span data-ttu-id="38c0c-109">Pour mettre en correspondance un caractère de l’expression de chaîne avec un caractère spécifique</span><span class="sxs-lookup"><span data-stu-id="38c0c-109">To match a character in the string expression against a specific character</span></span>  
  
-   <span data-ttu-id="38c0c-110">Placez le caractère spécifique directement dans la chaîne de modèle.</span><span class="sxs-lookup"><span data-stu-id="38c0c-110">Put the specific character directly in the pattern string.</span></span> <span data-ttu-id="38c0c-111">Certains caractères spéciaux doivent être entourés de crochets (`[ ]`).</span><span class="sxs-lookup"><span data-stu-id="38c0c-111">Certain special characters must be enclosed in brackets (`[ ]`).</span></span> <span data-ttu-id="38c0c-112">Pour plus d’informations, consultez [opérateur Like](../../../../visual-basic/language-reference/operators/like-operator.md).</span><span class="sxs-lookup"><span data-stu-id="38c0c-112">For more information, see [Like Operator](../../../../visual-basic/language-reference/operators/like-operator.md).</span></span>  
  
     <span data-ttu-id="38c0c-113">L’exemple suivant teste si `myString` se compose exactement du caractère `H`.</span><span class="sxs-lookup"><span data-stu-id="38c0c-113">The following example tests whether `myString` consists exactly of the single character `H`.</span></span>  
  
     [!code-vb[VbVbalrOperators#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#70)]  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-wildcard-character"></a><span data-ttu-id="38c0c-114">Pour mettre en correspondance un caractère de l’expression de chaîne avec un caractère générique</span><span class="sxs-lookup"><span data-stu-id="38c0c-114">To match a character in the string expression against a wildcard character</span></span>  
  
-   <span data-ttu-id="38c0c-115">Placez un point d’interrogation (`?`) dans la chaîne de modèle.</span><span class="sxs-lookup"><span data-stu-id="38c0c-115">Put a question mark (`?`) in the pattern string.</span></span> <span data-ttu-id="38c0c-116">N’importe quel caractère valide dans cette position rend une correspondance.</span><span class="sxs-lookup"><span data-stu-id="38c0c-116">Any valid character in this position makes a successful match.</span></span>  
  
     <span data-ttu-id="38c0c-117">L’exemple suivant teste si `myString` se compose du caractère `W` suivi exactement deux caractères de toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="38c0c-117">The following example tests whether `myString` consists of the single character `W` followed by exactly two characters of any values.</span></span>  
  
     [!code-vb[VbVbalrOperators#71](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#71)]  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-list-of-characters"></a><span data-ttu-id="38c0c-118">Pour mettre en correspondance un caractère dans l’expression de chaîne par rapport à une liste de caractères</span><span class="sxs-lookup"><span data-stu-id="38c0c-118">To match a character in the string expression against a list of characters</span></span>  
  
-   <span data-ttu-id="38c0c-119">Placez les crochets (`[ ]`) dans la chaîne de modèle et à l’intérieur de crochets, mettez la liste de caractères.</span><span class="sxs-lookup"><span data-stu-id="38c0c-119">Put brackets (`[ ]`) in the pattern string, and inside the brackets put the list of characters.</span></span> <span data-ttu-id="38c0c-120">Ne séparez pas les caractères par des virgules ou tout autre séparateur.</span><span class="sxs-lookup"><span data-stu-id="38c0c-120">Do not separate the characters with commas or any other separator.</span></span> <span data-ttu-id="38c0c-121">N’importe quel caractère unique dans la liste est en correspondance réussite.</span><span class="sxs-lookup"><span data-stu-id="38c0c-121">Any single character in the list makes a successful match.</span></span>  
  
     <span data-ttu-id="38c0c-122">L’exemple suivant teste si `myString` se compose de n’importe quel caractère valid, suivi par une seule des caractères `A`, `C`, ou `E`.</span><span class="sxs-lookup"><span data-stu-id="38c0c-122">The following example tests whether `myString` consists of any valid character followed by exactly one of the characters `A`, `C`, or `E`.</span></span>  
  
     [!code-vb[VbVbalrOperators#72](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#72)]  
  
     <span data-ttu-id="38c0c-123">Notez que cette correspondance respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="38c0c-123">Note that this match is case-sensitive.</span></span>  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-range-of-characters"></a><span data-ttu-id="38c0c-124">Pour mettre en correspondance un caractère de l’expression de chaîne avec une plage de caractères</span><span class="sxs-lookup"><span data-stu-id="38c0c-124">To match a character in the string expression against a range of characters</span></span>  
  
-   <span data-ttu-id="38c0c-125">Placez les crochets (`[ ]`) dans la chaîne de modèle et à l’intérieur de crochets, mettez les caractères les plus élevés dans la plage, séparés par un trait d’union (`–`).</span><span class="sxs-lookup"><span data-stu-id="38c0c-125">Put brackets (`[ ]`) in the pattern string, and inside the brackets put the lowest and highest characters in the range, separated by a hyphen (`–`).</span></span> <span data-ttu-id="38c0c-126">N’importe quel caractère unique dans la plage effectue une correspondance.</span><span class="sxs-lookup"><span data-stu-id="38c0c-126">Any single character within the range makes a successful match.</span></span>  
  
     <span data-ttu-id="38c0c-127">L’exemple suivant teste si `myString` se compose des caractères `num` suivie exactement un des caractères `i`, `j`, `k`, `l`, `m`, ou `n`.</span><span class="sxs-lookup"><span data-stu-id="38c0c-127">The following example tests whether `myString` consists of the characters `num` followed by exactly one of the characters `i`, `j`, `k`, `l`, `m`, or `n`.</span></span>  
  
     [!code-vb[VbVbalrOperators#73](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#73)]  
  
     <span data-ttu-id="38c0c-128">Notez que cette correspondance respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="38c0c-128">Note that this match is case-sensitive.</span></span>  
  
## <a name="matching-empty-strings"></a><span data-ttu-id="38c0c-129">Correspondance des chaînes vides</span><span class="sxs-lookup"><span data-stu-id="38c0c-129">Matching Empty Strings</span></span>  
 <span data-ttu-id="38c0c-130">`Like` traite la séquence `[]` comme une chaîne de longueur nulle (`""`).</span><span class="sxs-lookup"><span data-stu-id="38c0c-130">`Like` treats the sequence `[]` as a zero-length string (`""`).</span></span> <span data-ttu-id="38c0c-131">Vous pouvez utiliser `[]` pour tester si l’expression de chaîne entière est vide, mais vous ne pouvez pas l’utiliser pour tester si une position particulière dans l’expression de chaîne est vide.</span><span class="sxs-lookup"><span data-stu-id="38c0c-131">You can use `[]` to test whether the entire string expression is empty, but you cannot use it to test if a particular position in the string expression is empty.</span></span> <span data-ttu-id="38c0c-132">Si une position vide est une des options que vous devez tester, vous pouvez utiliser `Like` plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="38c0c-132">If an empty position is one of the options you need to test for, you can use `Like` more than once.</span></span>  
  
#### <a name="to-match-a-character-in-the-string-expression-against-a-list-of-characters-or-no-character"></a><span data-ttu-id="38c0c-133">Pour mettre en correspondance un caractère dans l’expression de chaîne par rapport à une liste de caractères ou aucun caractère</span><span class="sxs-lookup"><span data-stu-id="38c0c-133">To match a character in the string expression against a list of characters or no character</span></span>  
  
1. <span data-ttu-id="38c0c-134">Appelez le `Like` opérateur deux fois sur la même expression de chaîne et connectez les deux appels avec la [ou opérateur](../../../../visual-basic/language-reference/operators/or-operator.md) ou le [OrElse Operator](../../../../visual-basic/language-reference/operators/orelse-operator.md).</span><span class="sxs-lookup"><span data-stu-id="38c0c-134">Call the `Like` operator twice on the same string expression, and connect the two calls with either the [Or Operator](../../../../visual-basic/language-reference/operators/or-operator.md) or the [OrElse Operator](../../../../visual-basic/language-reference/operators/orelse-operator.md).</span></span>  
  
2. <span data-ttu-id="38c0c-135">Dans la chaîne de modèle pour la première `Like` clause, incluent la liste de caractères placés entourée crochets (`[ ]`).</span><span class="sxs-lookup"><span data-stu-id="38c0c-135">In the pattern string for the first `Like` clause, include the character list, enclosed in brackets (`[ ]`).</span></span>  
  
3. <span data-ttu-id="38c0c-136">Dans la chaîne de modèle pour le deuxième `Like` clause, ne placez pas n’importe quel caractère à la position en question.</span><span class="sxs-lookup"><span data-stu-id="38c0c-136">In the pattern string for the second `Like` clause, do not put any character at the position in question.</span></span>  
  
     <span data-ttu-id="38c0c-137">L’exemple suivant teste le numéro de téléphone à sept chiffres `phoneNum` pour exactement trois chiffres, suivis d’un espace, un trait d’union (`–`), une période (`.`), ou aucun caractère, ne suivi par exactement quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="38c0c-137">The following example tests the seven-digit telephone number `phoneNum` for exactly three numeric digits, followed by a space, a hyphen (`–`), a period (`.`), or no character at all, followed by exactly four numeric digits.</span></span>  
  
     [!code-vb[VbVbalrOperators#74](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#74)]  
  
## <a name="see-also"></a><span data-ttu-id="38c0c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38c0c-138">See also</span></span>

- [<span data-ttu-id="38c0c-139">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="38c0c-139">Comparison Operators</span></span>](../../../../visual-basic/language-reference/operators/comparison-operators.md)
- [<span data-ttu-id="38c0c-140">Opérateurs et expressions</span><span class="sxs-lookup"><span data-stu-id="38c0c-140">Operators and Expressions</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
- [<span data-ttu-id="38c0c-141">Like (opérateur)</span><span class="sxs-lookup"><span data-stu-id="38c0c-141">Like Operator</span></span>](../../../../visual-basic/language-reference/operators/like-operator.md)
- [<span data-ttu-id="38c0c-142">String (type de données)</span><span class="sxs-lookup"><span data-stu-id="38c0c-142">String Data Type</span></span>](../../../../visual-basic/language-reference/data-types/string-data-type.md)
