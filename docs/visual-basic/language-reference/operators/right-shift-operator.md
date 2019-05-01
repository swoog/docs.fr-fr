---
title: '>> Opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.>>
helpviewer_keywords:
- operator>>
- '>> operator [Visual Basic]'
- bit shift operators [Visual Basic]
- operator >>
- right shift operators [Visual Basic]
ms.assetid: 054dc6a6-47d9-47ef-82da-cfa2b59fbf8f
ms.openlocfilehash: 8803dc2e25edde756958a243d429dd30c5c78bcf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62053286"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="3ac1d-102">>>, Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3ac1d-102">>> Operator (Visual Basic)</span></span>
<span data-ttu-id="3ac1d-103">Effectue un décalage arithmétique vers la droite sur un modèle binaire.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-103">Performs an arithmetic right shift on a bit pattern.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3ac1d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ac1d-104">Syntax</span></span>  
  
```  
result = pattern >> amount  
```  
  
## <a name="parts"></a><span data-ttu-id="3ac1d-105">Composants</span><span class="sxs-lookup"><span data-stu-id="3ac1d-105">Parts</span></span>  
 `result`  
 <span data-ttu-id="3ac1d-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-106">Required.</span></span> <span data-ttu-id="3ac1d-107">Valeur numérique entière.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-107">Integral numeric value.</span></span> <span data-ttu-id="3ac1d-108">Le résultat du décalage du modèle de bit.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-108">The result of shifting the bit pattern.</span></span> <span data-ttu-id="3ac1d-109">Le type de données est identique à celui de `pattern`.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-109">The data type is the same as that of `pattern`.</span></span>  
  
 `pattern`  
 <span data-ttu-id="3ac1d-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-110">Required.</span></span> <span data-ttu-id="3ac1d-111">Expression numérique entière.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-111">Integral numeric expression.</span></span> <span data-ttu-id="3ac1d-112">Le modèle de bits à décaler.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-112">The bit pattern to be shifted.</span></span> <span data-ttu-id="3ac1d-113">Le type de données doit être un type intégral (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, ou `ULong`).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-113">The data type must be an integral type (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, or `ULong`).</span></span>  
  
 `amount`  
 <span data-ttu-id="3ac1d-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-114">Required.</span></span> <span data-ttu-id="3ac1d-115">Expression numérique.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-115">Numeric expression.</span></span> <span data-ttu-id="3ac1d-116">Le nombre de bits pour décaler le modèle binaire.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-116">The number of bits to shift the bit pattern.</span></span> <span data-ttu-id="3ac1d-117">Le type de données doit être `Integer` ou s’étendre au `Integer`.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-117">The data type must be `Integer` or widen to `Integer`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3ac1d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3ac1d-118">Remarks</span></span>  
 <span data-ttu-id="3ac1d-119">Les décalages arithmétiques ne sont pas circulaires, ce qui signifie que les bits décalés à une extrémité du résultat ne sont pas réintroduits à l’autre extrémité.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-119">Arithmetic shifts are not circular, which means the bits shifted off one end of the result are not reintroduced at the other end.</span></span> <span data-ttu-id="3ac1d-120">Dans un décalage arithmétique à droite, les bits décalés au-delà de la position de bit plus à droite sont supprimés, et le bit de plus à gauche (connexion) est propagé vers les positions de bit libérées à gauche.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-120">In an arithmetic right shift, the bits shifted beyond the rightmost bit position are discarded, and the leftmost (sign) bit is propagated into the bit positions vacated at the left.</span></span> <span data-ttu-id="3ac1d-121">Cela signifie que si `pattern` a une valeur négative, les positions libérées sont définies sur un ; sinon, elles sont définies à zéro.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-121">This means that if `pattern` has a negative value, the vacated positions are set to one; otherwise they are set to zero.</span></span>  
  
 <span data-ttu-id="3ac1d-122">Notez que les types de données `Byte`, `UShort`, `UInteger`, et `ULong` sont non signé, il n’existe aucune propagation du bit de signe.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-122">Note that the data types `Byte`, `UShort`, `UInteger`, and `ULong` are unsigned, so there is no sign bit to propagate.</span></span> <span data-ttu-id="3ac1d-123">Si `pattern` est de type non signé, les positions libérées ont toujours la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-123">If `pattern` is of any unsigned type, the vacated positions are always set to zero.</span></span>  
  
 <span data-ttu-id="3ac1d-124">Pour éviter un décalage des bits plus que peut contenir le résultat, Visual Basic masque la valeur de `amount` avec un masque de taille correspondant au type de données de `pattern`.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-124">To prevent shifting by more bits than the result can hold, Visual Basic masks the value of `amount` with a size mask corresponding to the data type of `pattern`.</span></span> <span data-ttu-id="3ac1d-125">L’opération AND binaire de ces valeurs est utilisé pour le décalage.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-125">The binary AND of these values is used for the shift amount.</span></span> <span data-ttu-id="3ac1d-126">Les masques de taille sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ac1d-126">The size masks are as follows:</span></span>  
  
|<span data-ttu-id="3ac1d-127">Type de données `pattern`</span><span class="sxs-lookup"><span data-stu-id="3ac1d-127">Data type of `pattern`</span></span>|<span data-ttu-id="3ac1d-128">Masque de taille (décimal)</span><span class="sxs-lookup"><span data-stu-id="3ac1d-128">Size mask (decimal)</span></span>|<span data-ttu-id="3ac1d-129">Masque de taille (hexadécimal)</span><span class="sxs-lookup"><span data-stu-id="3ac1d-129">Size mask (hexadecimal)</span></span>|  
|----------------------------|---------------------------|-------------------------------|  
|<span data-ttu-id="3ac1d-130">`SByte`, `Byte`</span><span class="sxs-lookup"><span data-stu-id="3ac1d-130">`SByte`, `Byte`</span></span>|<span data-ttu-id="3ac1d-131">7</span><span class="sxs-lookup"><span data-stu-id="3ac1d-131">7</span></span>|<span data-ttu-id="3ac1d-132">&H00000007</span><span class="sxs-lookup"><span data-stu-id="3ac1d-132">&H00000007</span></span>|  
|<span data-ttu-id="3ac1d-133">`Short`, `UShort`</span><span class="sxs-lookup"><span data-stu-id="3ac1d-133">`Short`, `UShort`</span></span>|<span data-ttu-id="3ac1d-134">15</span><span class="sxs-lookup"><span data-stu-id="3ac1d-134">15</span></span>|<span data-ttu-id="3ac1d-135">&H0000000F</span><span class="sxs-lookup"><span data-stu-id="3ac1d-135">&H0000000F</span></span>|  
|<span data-ttu-id="3ac1d-136">`Integer`, `UInteger`</span><span class="sxs-lookup"><span data-stu-id="3ac1d-136">`Integer`, `UInteger`</span></span>|<span data-ttu-id="3ac1d-137">31</span><span class="sxs-lookup"><span data-stu-id="3ac1d-137">31</span></span>|<span data-ttu-id="3ac1d-138">&H0000001F</span><span class="sxs-lookup"><span data-stu-id="3ac1d-138">&H0000001F</span></span>|  
|<span data-ttu-id="3ac1d-139">`Long`, `ULong`</span><span class="sxs-lookup"><span data-stu-id="3ac1d-139">`Long`, `ULong`</span></span>|<span data-ttu-id="3ac1d-140">63</span><span class="sxs-lookup"><span data-stu-id="3ac1d-140">63</span></span>|<span data-ttu-id="3ac1d-141">&H0000003F</span><span class="sxs-lookup"><span data-stu-id="3ac1d-141">&H0000003F</span></span>|  
  
 <span data-ttu-id="3ac1d-142">Si `amount` est égal à zéro, la valeur de `result` est identique à la valeur de `pattern`.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-142">If `amount` is zero, the value of `result` is identical to the value of `pattern`.</span></span> <span data-ttu-id="3ac1d-143">Si `amount` est négatif, il est considéré comme une valeur non signée et masquée avec le masque de taille appropriée.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-143">If `amount` is negative, it is taken as an unsigned value and masked with the appropriate size mask.</span></span>  
  
 <span data-ttu-id="3ac1d-144">Les décalages arithmétiques ne génèrent jamais des exceptions de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-144">Arithmetic shifts never generate overflow exceptions.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="3ac1d-145">Surcharge</span><span class="sxs-lookup"><span data-stu-id="3ac1d-145">Overloading</span></span>  
 <span data-ttu-id="3ac1d-146">Le `>>` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-146">The `>>` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="3ac1d-147">Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-147">If your code uses this operator on such a class or structure, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="3ac1d-148">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-148">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="3ac1d-149">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ac1d-149">Example</span></span>  
 <span data-ttu-id="3ac1d-150">L’exemple suivant utilise le `>>` opérateur pour effectuer des décalages arithmétiques vers la droite sur des valeurs intégrales.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-150">The following example uses the `>>` operator to perform arithmetic right shifts on integral values.</span></span> <span data-ttu-id="3ac1d-151">Le résultat a toujours les données de mêmes type que celui de l’expression décalée.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-151">The result always has the same data type as that of the expression being shifted.</span></span>  
  
 [!code-vb[VbVbalrOperators#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#14)]  
  
 <span data-ttu-id="3ac1d-152">Les résultats de l’exemple précédent sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ac1d-152">The results of the preceding example are as follows:</span></span>  
  
- <span data-ttu-id="3ac1d-153">`result1` est 2560 (0000 1010 0000 0000).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-153">`result1` is 2560 (0000 1010 0000 0000).</span></span>  
  
- <span data-ttu-id="3ac1d-154">`result2` est de 160 (0000 0000 1010 0000).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-154">`result2` is 160 (0000 0000 1010 0000).</span></span>  
  
- <span data-ttu-id="3ac1d-155">`result3` est 2 (0000 0000 0000 0010).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-155">`result3` is 2 (0000 0000 0000 0010).</span></span>  
  
- <span data-ttu-id="3ac1d-156">`result4` est 640 (0000 0010 1000 0000).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-156">`result4` is 640 (0000 0010 1000 0000).</span></span>  
  
- <span data-ttu-id="3ac1d-157">`result5` est égal à 0 (décalé de 15 places à droite).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-157">`result5` is 0 (shifted 15 places to the right).</span></span>  
  
 <span data-ttu-id="3ac1d-158">Le nombre de positions de décalage pour `result4` est calculé comme 18 et 15, ce qui est égal à 2.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-158">The shift amount for `result4` is calculated as 18 AND 15, which equals 2.</span></span>  
  
 <span data-ttu-id="3ac1d-159">L’exemple suivant montre les décalages arithmétiques sur une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="3ac1d-159">The following example shows arithmetic shifts on a negative value.</span></span>  
  
 [!code-vb[VbVbalrOperators#55](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#55)]  
  
 <span data-ttu-id="3ac1d-160">Les résultats de l’exemple précédent sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3ac1d-160">The results of the preceding example are as follows:</span></span>  
  
- <span data-ttu-id="3ac1d-161">`negresult1` is -512 (1111 1110 0000 0000).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-161">`negresult1` is -512 (1111 1110 0000 0000).</span></span>  
  
- <span data-ttu-id="3ac1d-162">`negresult2` est -1 (le bit de signe est propagé).</span><span class="sxs-lookup"><span data-stu-id="3ac1d-162">`negresult2` is -1 (the sign bit is propagated).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ac1d-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ac1d-163">See also</span></span>

- [<span data-ttu-id="3ac1d-164">Opérateurs de décalage de bits</span><span class="sxs-lookup"><span data-stu-id="3ac1d-164">Bit Shift Operators</span></span>](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [<span data-ttu-id="3ac1d-165">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="3ac1d-165">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="3ac1d-166">>>= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="3ac1d-166">>>= Operator</span></span>](../../../visual-basic/language-reference/operators/right-shift-assignment-operator.md)
- [<span data-ttu-id="3ac1d-167">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3ac1d-167">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="3ac1d-168">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="3ac1d-168">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="3ac1d-169">Opérateurs arithmétiques en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3ac1d-169">Arithmetic Operators in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
