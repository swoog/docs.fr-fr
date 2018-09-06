---
title: Decimal, type de données (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Decimal
helpviewer_keywords:
- literal type characters [Visual Basic], D
- trailing zeros
- real numbers
- trailing 0 characters [Visual Basic]
- Decimal data type
- D literal type character [Visual Basic]
- decimals, Decimal data type
- 0 characters [Visual Basic], trailing
- data types [Visual Basic], assigning
- decimal keyword [Visual Basic]
- numbers [Visual Basic], real
- variable-precision numbers
- zeros, trailing
- '@ identifier type character'
- identifier type characters [Visual Basic], @
ms.assetid: 1d855b45-afe2-45b0-a623-96b6f63a43d5
ms.openlocfilehash: ffc1cd141ba624d2ce26e4b1c070431ff0ddd6fe
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44036192"
---
# <a name="decimal-data-type-visual-basic"></a><span data-ttu-id="cce03-102">Decimal, type de données (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cce03-102">Decimal Data Type (Visual Basic)</span></span>
<span data-ttu-id="cce03-103">Contient des valeurs (16 octets) de 128 bits représentant des nombres entier de 96 bits (12 octets) mis à l’échelle par une puissance de 10 variable signés.</span><span class="sxs-lookup"><span data-stu-id="cce03-103">Holds signed 128-bit (16-byte) values representing 96-bit (12-byte) integer numbers scaled by a variable power of 10.</span></span> <span data-ttu-id="cce03-104">Le facteur d’échelle spécifie le nombre de chiffres à droite de la virgule décimale ; Il est compris entre 0 et 28.</span><span class="sxs-lookup"><span data-stu-id="cce03-104">The scaling factor specifies the number of digits to the right of the decimal point; it ranges from 0 through 28.</span></span> <span data-ttu-id="cce03-105">Avec une échelle de 0 (pas de décimales), la plus grande valeur possible est +/-79,228,162,514,264,337,593,543,950,335 (+/-7 9228162514264337593543950335E + 28).</span><span class="sxs-lookup"><span data-stu-id="cce03-105">With a scale of 0 (no decimal places), the largest possible value is +/-79,228,162,514,264,337,593,543,950,335 (+/-7.9228162514264337593543950335E+28).</span></span> <span data-ttu-id="cce03-106">La plus grande valeur est +/-7,9228162514264337593543950335 avec 28 décimales, et la plus petite valeur différente de zéro est +/-0,0000000000000000000000000001 (+/-1E-28).</span><span class="sxs-lookup"><span data-stu-id="cce03-106">With 28 decimal places, the largest value is +/-7.9228162514264337593543950335, and the smallest nonzero value is +/-0.0000000000000000000000000001 (+/-1E-28).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cce03-107">Notes</span><span class="sxs-lookup"><span data-stu-id="cce03-107">Remarks</span></span>  
 <span data-ttu-id="cce03-108">Le `Decimal` type de données fournit le plus grand nombre de chiffres significatifs pour un nombre.</span><span class="sxs-lookup"><span data-stu-id="cce03-108">The `Decimal` data type provides the greatest number of significant digits for a number.</span></span> <span data-ttu-id="cce03-109">Il prend en charge jusqu'à 29 chiffres significatifs et peut représenter des valeurs dépassant 7,9228 x 10 ^ 28.</span><span class="sxs-lookup"><span data-stu-id="cce03-109">It supports up to 29 significant digits and can represent values in excess of 7.9228 x 10^28.</span></span> <span data-ttu-id="cce03-110">Il est particulièrement adapté aux calculs, tels que financiers, qui nécessitent un grand nombre de chiffres, mais ne peuvent pas tolérer les erreurs d’arrondi.</span><span class="sxs-lookup"><span data-stu-id="cce03-110">It is particularly suitable for calculations, such as financial, that require a large number of digits but cannot tolerate rounding errors.</span></span>  
  
 <span data-ttu-id="cce03-111">La valeur par défaut de `Decimal` est 0.</span><span class="sxs-lookup"><span data-stu-id="cce03-111">The default value of `Decimal` is 0.</span></span>  
  
## <a name="programming-tips"></a><span data-ttu-id="cce03-112">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="cce03-112">Programming Tips</span></span>  
  
-   <span data-ttu-id="cce03-113">**Précision.**</span><span class="sxs-lookup"><span data-stu-id="cce03-113">**Precision.**</span></span> <span data-ttu-id="cce03-114">`Decimal` n’est pas un type de données à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="cce03-114">`Decimal` is not a floating-point data type.</span></span> <span data-ttu-id="cce03-115">Le `Decimal` structure contient une valeur d’entier binaire, avec un bit de signe et un entier facteur qui spécifie quelle partie de la valeur est une fraction décimale d’échelle.</span><span class="sxs-lookup"><span data-stu-id="cce03-115">The `Decimal` structure holds a binary integer value, together with a sign bit and an integer scaling factor that specifies what portion of the value is a decimal fraction.</span></span> <span data-ttu-id="cce03-116">Pour cette raison, `Decimal` nombres ont une représentation plus précise dans la mémoire que les types à virgule flottante (`Single` et `Double`).</span><span class="sxs-lookup"><span data-stu-id="cce03-116">Because of this, `Decimal` numbers have a more precise representation in memory than floating-point types (`Single` and `Double`).</span></span>  
  
-   <span data-ttu-id="cce03-117">**Performances**</span><span class="sxs-lookup"><span data-stu-id="cce03-117">**Performance.**</span></span> <span data-ttu-id="cce03-118">Le `Decimal` type de données est le plus lent de tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="cce03-118">The `Decimal` data type is the slowest of all the numeric types.</span></span> <span data-ttu-id="cce03-119">Vous devez évaluer l’importance de précision par rapport aux performances avant de choisir un type de données.</span><span class="sxs-lookup"><span data-stu-id="cce03-119">You should weigh the importance of precision against performance before choosing a data type.</span></span>  
  
-   <span data-ttu-id="cce03-120">**Étendues.**</span><span class="sxs-lookup"><span data-stu-id="cce03-120">**Widening.**</span></span> <span data-ttu-id="cce03-121">Le `Decimal` type de données s’étend à `Single` ou `Double`.</span><span class="sxs-lookup"><span data-stu-id="cce03-121">The `Decimal` data type widens to `Single` or `Double`.</span></span> <span data-ttu-id="cce03-122">Cela signifie que vous pouvez convertir `Decimal` à un de ces types sans rencontrer un <xref:System.OverflowException?displayProperty=nameWithType> erreur.</span><span class="sxs-lookup"><span data-stu-id="cce03-122">This means you can convert `Decimal` to either of these types without encountering a <xref:System.OverflowException?displayProperty=nameWithType> error.</span></span>  
  
-   <span data-ttu-id="cce03-123">**Les zéros de fin.**</span><span class="sxs-lookup"><span data-stu-id="cce03-123">**Trailing Zeros.**</span></span> <span data-ttu-id="cce03-124">Visual Basic ne stocke pas de zéros de fin dans un `Decimal` littéral.</span><span class="sxs-lookup"><span data-stu-id="cce03-124">Visual Basic does not store trailing zeros in a `Decimal` literal.</span></span> <span data-ttu-id="cce03-125">Toutefois, un `Decimal` variable conserve les zéros de fin acquis par le calcul.</span><span class="sxs-lookup"><span data-stu-id="cce03-125">However, a `Decimal` variable preserves any trailing zeros acquired computationally.</span></span> <span data-ttu-id="cce03-126">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="cce03-126">The following example illustrates this.</span></span>  
  
    ```  
    Dim d1, d2, d3, d4 As Decimal  
    d1 = 2.375D  
    d2 = 1.625D  
    d3 = d1 + d2  
    d4 = 4.000D  
    MsgBox("d1 = " & CStr(d1) & ", d2 = " & CStr(d2) &  
          ", d3 = " & CStr(d3) & ", d4 = " & CStr(d4))  
    ```  
  
     <span data-ttu-id="cce03-127">La sortie de `MsgBox` dans l’exemple précédent est comme suit :</span><span class="sxs-lookup"><span data-stu-id="cce03-127">The output of `MsgBox` in the preceding example is as follows:</span></span>  
  
     <span data-ttu-id="cce03-128">D1 = 2.375, d2 = 1.625, d3 = 4.000, d4 = 4</span><span class="sxs-lookup"><span data-stu-id="cce03-128">d1 = 2.375, d2 = 1.625, d3 = 4.000, d4 = 4</span></span>  
  
-   <span data-ttu-id="cce03-129">**Caractères de type.**</span><span class="sxs-lookup"><span data-stu-id="cce03-129">**Type Characters.**</span></span> <span data-ttu-id="cce03-130">L'ajout du caractère de type littéral `D` à un littéral force ce dernier en type de données `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="cce03-130">Appending the literal type character `D` to a literal forces it to the `Decimal` data type.</span></span> <span data-ttu-id="cce03-131">L'ajout du caractère de type identificateur `@` à un identificateur force ce dernier en type `Decimal`.</span><span class="sxs-lookup"><span data-stu-id="cce03-131">Appending the identifier type character `@` to any identifier forces it to `Decimal`.</span></span>  
  
-   <span data-ttu-id="cce03-132">**Type de Framework.**</span><span class="sxs-lookup"><span data-stu-id="cce03-132">**Framework Type.**</span></span> <span data-ttu-id="cce03-133">Le type correspondant dans le .NET Framework est la structure <xref:System.Decimal?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="cce03-133">The corresponding type in the .NET Framework is the <xref:System.Decimal?displayProperty=nameWithType> structure.</span></span>  
  
## <a name="range"></a><span data-ttu-id="cce03-134">Plage</span><span class="sxs-lookup"><span data-stu-id="cce03-134">Range</span></span>  
 <span data-ttu-id="cce03-135">Vous devrez peut-être utiliser le `D` type caractère à assigner une grande valeur à une `Decimal` variable ou constante.</span><span class="sxs-lookup"><span data-stu-id="cce03-135">You might need to use the `D` type character to assign a large value to a `Decimal` variable or constant.</span></span> <span data-ttu-id="cce03-136">Cette exigence est étant donné que le compilateur interprète un littéral en tant que `Long` , sauf si un caractère de type littéral suit le littéral, comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="cce03-136">This requirement is because the compiler interprets a literal as `Long` unless a literal type character follows the literal, as the following example shows.</span></span>  
  
```  
Dim bigDec1 As Decimal = 9223372036854775807   ' No overflow.  
Dim bigDec2 As Decimal = 9223372036854775808   ' Overflow.  
Dim bigDec3 As Decimal = 9223372036854775808D  ' No overflow.  
```  
  
 <span data-ttu-id="cce03-137">La déclaration pour `bigDec1` ne produit pas un dépassement de capacité, car la valeur qui lui est attribuée se situe dans la plage pour `Long`.</span><span class="sxs-lookup"><span data-stu-id="cce03-137">The declaration for `bigDec1` doesn't produce an overflow because the value that's assigned to it falls within the range for `Long`.</span></span> <span data-ttu-id="cce03-138">Le `Long` valeur peut être assignée à la `Decimal` variable.</span><span class="sxs-lookup"><span data-stu-id="cce03-138">The `Long` value can be assigned to the `Decimal` variable.</span></span>  
  
 <span data-ttu-id="cce03-139">La déclaration pour `bigDec2` génère une erreur de dépassement de capacité, car la valeur qui lui est affectée est trop grande pour `Long`.</span><span class="sxs-lookup"><span data-stu-id="cce03-139">The declaration for `bigDec2` generates an overflow error because the value that's assigned to it is too large for `Long`.</span></span> <span data-ttu-id="cce03-140">Étant donné que le littéral numérique ne peut pas tout d’abord être interprété comme un `Long`, il ne peut pas être affecté à la `Decimal` variable.</span><span class="sxs-lookup"><span data-stu-id="cce03-140">Because the numeric literal can't first be interpreted as a `Long`, it can't be assigned to the `Decimal` variable.</span></span>  
  
 <span data-ttu-id="cce03-141">Pour `bigDec3`, le caractère de type littéral `D` résout le problème en forçant le compilateur à interpréter le littéral en tant qu’un `Decimal` au lieu de comme un `Long`.</span><span class="sxs-lookup"><span data-stu-id="cce03-141">For `bigDec3`, the literal type character `D` solves the problem by forcing the compiler to interpret the literal as a `Decimal` instead of as a `Long`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cce03-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cce03-142">See Also</span></span>  
 <xref:System.Decimal?displayProperty=nameWithType>  
 <xref:System.Decimal.%23ctor%2A?displayProperty=nameWithType>  
 <xref:System.Math.Round%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="cce03-143">Types de données</span><span class="sxs-lookup"><span data-stu-id="cce03-143">Data Types</span></span>](../../../visual-basic/language-reference/data-types/index.md)  
 [<span data-ttu-id="cce03-144">Single (type de données)</span><span class="sxs-lookup"><span data-stu-id="cce03-144">Single Data Type</span></span>](../../../visual-basic/language-reference/data-types/single-data-type.md)  
 [<span data-ttu-id="cce03-145">Double (type de données)</span><span class="sxs-lookup"><span data-stu-id="cce03-145">Double Data Type</span></span>](../../../visual-basic/language-reference/data-types/double-data-type.md)  
 [<span data-ttu-id="cce03-146">Fonctions de conversion de types</span><span class="sxs-lookup"><span data-stu-id="cce03-146">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)  
 [<span data-ttu-id="cce03-147">Liste des conversions</span><span class="sxs-lookup"><span data-stu-id="cce03-147">Conversion Summary</span></span>](../../../visual-basic/language-reference/keywords/conversion-summary.md)  
 [<span data-ttu-id="cce03-148">Utilisation efficace des types de données</span><span class="sxs-lookup"><span data-stu-id="cce03-148">Efficient Use of Data Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)
