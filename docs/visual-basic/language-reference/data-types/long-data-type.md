---
title: Long, type de données (Visual Basic)
ms.date: 01/31/2018
f1_keywords:
- vb.Long
helpviewer_keywords:
- identifier type characters [Visual Basic], &
- numbers [Visual Basic], whole
- whole numbers
- integral data types [Visual Basic]
- '& identifier type character'
- integer numbers
- literal type characters [Visual Basic], L
- numbers [Visual Basic], integer
- integers [Visual Basic], data types
- L literal type character [Visual Basic]
- integers [Visual Basic], types
- Long keyword [Visual Basic]
- data types [Visual Basic], integral
- data types [Visual Basic], assigning
- Long data type
ms.assetid: b4770c34-1804-4f8c-b512-c10b0893e516
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0b3970aad08f2be98d175b4175ef06711bcaf609
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43452821"
---
# <a name="long-data-type-visual-basic"></a><span data-ttu-id="e04c7-102">Type de données long (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e04c7-102">Long data type (Visual Basic)</span></span>

<span data-ttu-id="e04c7-103">Contient des entiers (8 octets) de 64 bits dont la valeur de -9,223,372,036,854,775,808 à 9,223,372,036,854,775,807 signés (9.2... E + 18).</span><span class="sxs-lookup"><span data-stu-id="e04c7-103">Holds signed 64-bit (8-byte) integers ranging in value from -9,223,372,036,854,775,808 through 9,223,372,036,854,775,807 (9.2...E+18).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e04c7-104">Notes</span><span class="sxs-lookup"><span data-stu-id="e04c7-104">Remarks</span></span>

 <span data-ttu-id="e04c7-105">Utilisez le `Long` type de données contenant des nombres entiers qui sont trop volumineuses pour tenir le `Integer` type de données.</span><span class="sxs-lookup"><span data-stu-id="e04c7-105">Use the `Long` data type to contain integer numbers that are too large to fit in the `Integer` data type.</span></span>  
  
 <span data-ttu-id="e04c7-106">La valeur par défaut de `Long` est 0.</span><span class="sxs-lookup"><span data-stu-id="e04c7-106">The default value of `Long` is 0.</span></span>

## <a name="literal-assignments"></a><span data-ttu-id="e04c7-107">Affectations de littéraux</span><span class="sxs-lookup"><span data-stu-id="e04c7-107">Literal assignments</span></span> 

<span data-ttu-id="e04c7-108">Vous pouvez déclarer et initialiser une `Long` variable en lui assignant un littéral décimal, un littéral hexadécimal, un littéral octal, ou (à partir de Visual Basic 2017) un littéral binaire.</span><span class="sxs-lookup"><span data-stu-id="e04c7-108">You can declare and initialize a `Long` variable by assigning it a decimal literal, a hexadecimal literal, an octal literal, or (starting with Visual Basic 2017) a binary literal.</span></span> <span data-ttu-id="e04c7-109">Si le littéral entier est en dehors de la plage de `Long` (autrement dit, s’il est inférieur à <xref:System.Int64.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.Int64.MaxValue?displayProperty=nameWithType>, une erreur de compilation se produit.</span><span class="sxs-lookup"><span data-stu-id="e04c7-109">If the integer literal is outside the range of `Long` (that is, if it is less than <xref:System.Int64.MinValue?displayProperty=nameWithType> or greater than <xref:System.Int64.MaxValue?displayProperty=nameWithType>, a compilation error occurs.</span></span>

<span data-ttu-id="e04c7-110">Dans l’exemple suivant, les entiers égaux à 4 294 967 296 représentés comme des littéraux décimaux, hexadécimaux et binaires sont assignés aux valeurs `Long`.</span><span class="sxs-lookup"><span data-stu-id="e04c7-110">In the following example, integers equal to 4,294,967,296 that are represented as decimal, hexadecimal, and binary literals are assigned to `Long` values.</span></span>
  
[!code-vb[long](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#Long)]  

> [!NOTE]
> <span data-ttu-id="e04c7-111">Vous utilisez le préfixe `&h` ou `&H` pour désigner un littéral hexadécimal, le préfixe `&b` ou `&B` pour désigner un littéral binaire et le préfixe `&o` ou `&O` pour désigner un littéral octal.</span><span class="sxs-lookup"><span data-stu-id="e04c7-111">You use the prefix `&h` or `&H` to denote a hexadecimal literal, the prefix `&b` or `&B` to denote a binary literal, and the prefix `&o` or `&O` to denote an octal literal.</span></span> <span data-ttu-id="e04c7-112">Les littéraux décimaux n’ont pas de préfixe.</span><span class="sxs-lookup"><span data-stu-id="e04c7-112">Decimal literals have no prefix.</span></span>

<span data-ttu-id="e04c7-113">À partir de Visual Basic 2017, vous pouvez également utiliser le caractère de soulignement, `_`, comme un séparateur numérique pour améliorer la lisibilité, comme dans l’exemple suivant montre.</span><span class="sxs-lookup"><span data-stu-id="e04c7-113">Starting with Visual Basic 2017, you can also use the underscore character, `_`, as a digit separator to enhance readability, as the following example shows.</span></span>

[!code-vb[long](../../../../samples/snippets/visualbasic/language-reference/data-types/numeric-literals.vb#LongS)]

<span data-ttu-id="e04c7-114">À partir de Visual Basic 15.5, vous pouvez également utiliser le caractère de soulignement (`_`) comme séparateur de début entre le préfixe et les chiffres hexadécimaux, binaires ou octaux.</span><span class="sxs-lookup"><span data-stu-id="e04c7-114">Starting with Visual Basic 15.5, you can also use the underscore character (`_`) as a leading separator between the prefix and the hexadecimal, binary, or octal digits.</span></span> <span data-ttu-id="e04c7-115">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e04c7-115">For example:</span></span>

```vb
Dim number As Long = &H_0FAC_0326_1489_D68C
```

[!INCLUDE [supporting-underscores](../../../../includes/vb-separator-langversion.md)]

<span data-ttu-id="e04c7-116">Littéraux numériques peuvent également inclure le `L` [caractère de type](../../programming-guide\language-features\data-types/type-characters.md) pour désigner le `Long` type de données, comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="e04c7-116">Numeric literals can also include the `L` [type character](../../programming-guide\language-features\data-types/type-characters.md) to denote the `Long` data type, as the following example shows.</span></span>

```vb
Dim number = &H_0FAC_0326_1489_D68CL
```

## <a name="programming-tips"></a><span data-ttu-id="e04c7-117">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="e04c7-117">Programming tips</span></span>

-   <span data-ttu-id="e04c7-118">**Considérations sur l’interopérabilité.**</span><span class="sxs-lookup"><span data-stu-id="e04c7-118">**Interop Considerations.**</span></span> <span data-ttu-id="e04c7-119">Si vous utilisez des composants non écrits pour le .NET Framework, par exemple des objets Automation ou COM, n’oubliez pas que `Long` a une largeur de données différente (32 bits) dans d’autres environnements.</span><span class="sxs-lookup"><span data-stu-id="e04c7-119">If you are interfacing with components not written for the .NET Framework, for example Automation or COM objects, remember that `Long` has a different data width (32 bits) in other environments.</span></span> <span data-ttu-id="e04c7-120">Si vous passez un argument de 32 bits à un tel composant, déclarez-le en tant que `Integer` au lieu de `Long` dans votre nouveau code Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e04c7-120">If you are passing a 32-bit argument to such a component, declare it as `Integer` instead of `Long` in your new Visual Basic code.</span></span>  
  
-   <span data-ttu-id="e04c7-121">**Étendues.**</span><span class="sxs-lookup"><span data-stu-id="e04c7-121">**Widening.**</span></span> <span data-ttu-id="e04c7-122">Le `Long` type de données s’étend à `Decimal`, `Single`, ou `Double`.</span><span class="sxs-lookup"><span data-stu-id="e04c7-122">The `Long` data type widens to `Decimal`, `Single`, or `Double`.</span></span> <span data-ttu-id="e04c7-123">Cela signifie que vous pouvez convertir `Long` en l'un de ces types sans rencontrer d'erreur <xref:System.OverflowException?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="e04c7-123">This means you can convert `Long` to any one of these types without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>  
  
-   <span data-ttu-id="e04c7-124">**Caractères de type.**</span><span class="sxs-lookup"><span data-stu-id="e04c7-124">**Type Characters.**</span></span> <span data-ttu-id="e04c7-125">L'ajout du caractère de type littéral `L` à un littéral force ce dernier en type de données `Long`.</span><span class="sxs-lookup"><span data-stu-id="e04c7-125">Appending the literal type character `L` to a literal forces it to the `Long` data type.</span></span> <span data-ttu-id="e04c7-126">L'ajout du caractère de type identificateur `&` à un identificateur force ce dernier en type `Long`.</span><span class="sxs-lookup"><span data-stu-id="e04c7-126">Appending the identifier type character `&` to any identifier forces it to `Long`.</span></span>  
  
-   <span data-ttu-id="e04c7-127">**Type de Framework.**</span><span class="sxs-lookup"><span data-stu-id="e04c7-127">**Framework Type.**</span></span> <span data-ttu-id="e04c7-128">Le type correspondant dans le .NET Framework est la structure <xref:System.Int64?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="e04c7-128">The corresponding type in the .NET Framework is the <xref:System.Int64?displayProperty=nameWithType> structure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e04c7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e04c7-129">See also</span></span>

<span data-ttu-id="e04c7-130"><xref:System.Int64>
[Types de données](../../../visual-basic/language-reference/data-types/index.md) </span><span class="sxs-lookup"><span data-stu-id="e04c7-130"><xref:System.Int64>
[Data Types](../../../visual-basic/language-reference/data-types/index.md) </span></span>  
<span data-ttu-id="e04c7-131">[Type de données Integer](../../../visual-basic/language-reference/data-types/integer-data-type.md) </span><span class="sxs-lookup"><span data-stu-id="e04c7-131">[Integer Data Type](../../../visual-basic/language-reference/data-types/integer-data-type.md) </span></span>  
<span data-ttu-id="e04c7-132">[Type de données de type short](../../../visual-basic/language-reference/data-types/short-data-type.md) </span><span class="sxs-lookup"><span data-stu-id="e04c7-132">[Short Data Type](../../../visual-basic/language-reference/data-types/short-data-type.md) </span></span>  
<span data-ttu-id="e04c7-133">[Fonctions de Conversion de type](../../../visual-basic/language-reference/functions/type-conversion-functions.md) </span><span class="sxs-lookup"><span data-stu-id="e04c7-133">[Type Conversion Functions](../../../visual-basic/language-reference/functions/type-conversion-functions.md) </span></span>  
<span data-ttu-id="e04c7-134">[Résumé de la conversion](../../../visual-basic/language-reference/keywords/conversion-summary.md) </span><span class="sxs-lookup"><span data-stu-id="e04c7-134">[Conversion Summary](../../../visual-basic/language-reference/keywords/conversion-summary.md) </span></span>  
[<span data-ttu-id="e04c7-135">Utilisation efficace des types de données</span><span class="sxs-lookup"><span data-stu-id="e04c7-135">Efficient Use of Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
