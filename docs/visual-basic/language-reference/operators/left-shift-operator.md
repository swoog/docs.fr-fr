---
title: <<, Opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.<<
helpviewer_keywords:
- bit shift operators [Visual Basic]
- << operator [Visual Basic]
- operator <<, Visual Basic left shift operator
ms.assetid: fdb93d25-81ba-417f-b808-41207bfb8440
ms.openlocfilehash: 75c16c27dc919ba365cbe3c28c61a1e46496b0ae
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768288"
---
# <a name="-operator-visual-basic"></a><span data-ttu-id="8a0f3-102">\<\< Opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8a0f3-102">\<\< Operator (Visual Basic)</span></span>
<span data-ttu-id="8a0f3-103">Effectue un décalage arithmétique vers la gauche sur un modèle binaire.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-103">Performs an arithmetic left shift on a bit pattern.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a0f3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a0f3-104">Syntax</span></span>  
  
```  
result = pattern << amount  
```  
  
## <a name="parts"></a><span data-ttu-id="8a0f3-105">Composants</span><span class="sxs-lookup"><span data-stu-id="8a0f3-105">Parts</span></span>  
 `result`  
 <span data-ttu-id="8a0f3-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-106">Required.</span></span> <span data-ttu-id="8a0f3-107">Valeur numérique entière.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-107">Integral numeric value.</span></span> <span data-ttu-id="8a0f3-108">Le résultat du décalage du modèle de bit.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-108">The result of shifting the bit pattern.</span></span> <span data-ttu-id="8a0f3-109">Le type de données est identique à celui de `pattern`.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-109">The data type is the same as that of `pattern`.</span></span>  
  
 `pattern`  
 <span data-ttu-id="8a0f3-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-110">Required.</span></span> <span data-ttu-id="8a0f3-111">Expression numérique entière.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-111">Integral numeric expression.</span></span> <span data-ttu-id="8a0f3-112">Le modèle de bits à décaler.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-112">The bit pattern to be shifted.</span></span> <span data-ttu-id="8a0f3-113">Le type de données doit être un type intégral (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, ou `ULong`).</span><span class="sxs-lookup"><span data-stu-id="8a0f3-113">The data type must be an integral type (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, or `ULong`).</span></span>  
  
 `amount`  
 <span data-ttu-id="8a0f3-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-114">Required.</span></span> <span data-ttu-id="8a0f3-115">Expression numérique.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-115">Numeric expression.</span></span> <span data-ttu-id="8a0f3-116">Le nombre de bits pour décaler le modèle binaire.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-116">The number of bits to shift the bit pattern.</span></span> <span data-ttu-id="8a0f3-117">Le type de données doit être `Integer` ou s’étendre au `Integer`.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-117">The data type must be `Integer` or widen to `Integer`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8a0f3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8a0f3-118">Remarks</span></span>  
 <span data-ttu-id="8a0f3-119">Les décalages arithmétiques ne sont pas circulaires, ce qui signifie que les bits décalés à une extrémité du résultat ne sont pas réintroduits à l’autre extrémité.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-119">Arithmetic shifts are not circular, which means the bits shifted off one end of the result are not reintroduced at the other end.</span></span> <span data-ttu-id="8a0f3-120">Dans un décalage arithmétique vers la gauche, les bits décalés au-delà de la plage du type de données de résultat sont ignorés, et les positions binaires libérées à droite sont définies à zéro.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-120">In an arithmetic left shift, the bits shifted beyond the range of the result data type are discarded, and the bit positions vacated on the right are set to zero.</span></span>  
  
 <span data-ttu-id="8a0f3-121">Pour éviter un décalage en plus de bits que le résultat peut contenir, Visual Basic masque la valeur de `amount` avec un masque de taille qui correspond au type de données de `pattern`.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-121">To prevent a shift by more bits than the result can hold, Visual Basic masks the value of `amount` with a size mask that corresponds to the data type of `pattern`.</span></span> <span data-ttu-id="8a0f3-122">L’opération AND binaire de ces valeurs est utilisé pour le décalage.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-122">The binary AND of these values is used for the shift amount.</span></span> <span data-ttu-id="8a0f3-123">Les masques de taille sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a0f3-123">The size masks are as follows:</span></span>  
  
|<span data-ttu-id="8a0f3-124">Type de données `pattern`</span><span class="sxs-lookup"><span data-stu-id="8a0f3-124">Data type of `pattern`</span></span>|<span data-ttu-id="8a0f3-125">Masque de taille (décimal)</span><span class="sxs-lookup"><span data-stu-id="8a0f3-125">Size mask (decimal)</span></span>|<span data-ttu-id="8a0f3-126">Masque de taille (hexadécimal)</span><span class="sxs-lookup"><span data-stu-id="8a0f3-126">Size mask (hexadecimal)</span></span>|  
|----------------------------|---------------------------|-------------------------------|  
|<span data-ttu-id="8a0f3-127">`SByte`, `Byte`</span><span class="sxs-lookup"><span data-stu-id="8a0f3-127">`SByte`, `Byte`</span></span>|<span data-ttu-id="8a0f3-128">7</span><span class="sxs-lookup"><span data-stu-id="8a0f3-128">7</span></span>|<span data-ttu-id="8a0f3-129">&H00000007</span><span class="sxs-lookup"><span data-stu-id="8a0f3-129">&H00000007</span></span>|  
|<span data-ttu-id="8a0f3-130">`Short`, `UShort`</span><span class="sxs-lookup"><span data-stu-id="8a0f3-130">`Short`, `UShort`</span></span>|<span data-ttu-id="8a0f3-131">15</span><span class="sxs-lookup"><span data-stu-id="8a0f3-131">15</span></span>|<span data-ttu-id="8a0f3-132">&H0000000F</span><span class="sxs-lookup"><span data-stu-id="8a0f3-132">&H0000000F</span></span>|  
|<span data-ttu-id="8a0f3-133">`Integer`, `UInteger`</span><span class="sxs-lookup"><span data-stu-id="8a0f3-133">`Integer`, `UInteger`</span></span>|<span data-ttu-id="8a0f3-134">31</span><span class="sxs-lookup"><span data-stu-id="8a0f3-134">31</span></span>|<span data-ttu-id="8a0f3-135">&H0000001F</span><span class="sxs-lookup"><span data-stu-id="8a0f3-135">&H0000001F</span></span>|  
|<span data-ttu-id="8a0f3-136">`Long`, `ULong`</span><span class="sxs-lookup"><span data-stu-id="8a0f3-136">`Long`, `ULong`</span></span>|<span data-ttu-id="8a0f3-137">63</span><span class="sxs-lookup"><span data-stu-id="8a0f3-137">63</span></span>|<span data-ttu-id="8a0f3-138">&H0000003F</span><span class="sxs-lookup"><span data-stu-id="8a0f3-138">&H0000003F</span></span>|  
  
 <span data-ttu-id="8a0f3-139">Si `amount` est égal à zéro, la valeur de `result` est identique à la valeur de `pattern`.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-139">If `amount` is zero, the value of `result` is identical to the value of `pattern`.</span></span> <span data-ttu-id="8a0f3-140">Si `amount` est négatif, il est considéré comme une valeur non signée et masquée avec le masque de taille appropriée.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-140">If `amount` is negative, it is taken as an unsigned value and masked with the appropriate size mask.</span></span>  
  
 <span data-ttu-id="8a0f3-141">Les décalages arithmétiques ne génèrent jamais des exceptions de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-141">Arithmetic shifts never generate overflow exceptions.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8a0f3-142">Le `<<` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-142">The `<<` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure.</span></span> <span data-ttu-id="8a0f3-143">Si votre code utilise cet opérateur sur une telle classe ou structure, assurez-vous que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-143">If your code uses this operator on such a class or structure, be sure that you understand its redefined behavior.</span></span> <span data-ttu-id="8a0f3-144">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="8a0f3-144">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8a0f3-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="8a0f3-145">Example</span></span>  
 <span data-ttu-id="8a0f3-146">L’exemple suivant utilise le `<<` opérateur pour effectuer une opération arithmétique gauche décale sur des valeurs intégrales.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-146">The following example uses the `<<` operator to perform arithmetic left shifts on integral values.</span></span> <span data-ttu-id="8a0f3-147">Le résultat a toujours les données de mêmes type que celui de l’expression décalée.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-147">The result always has the same data type as that of the expression being shifted.</span></span>  
  
 [!code-vb[VbVbalrOperators#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#12)]  
  
 <span data-ttu-id="8a0f3-148">Les résultats de l’exemple précédent sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8a0f3-148">The results of the previous example are as follows:</span></span>  
  
- <span data-ttu-id="8a0f3-149">`result1` is 192 (0000 0000 1100 0000).</span><span class="sxs-lookup"><span data-stu-id="8a0f3-149">`result1` is 192 (0000 0000 1100 0000).</span></span>  
  
- <span data-ttu-id="8a0f3-150">`result2` is 3072 (0000 1100 0000 0000).</span><span class="sxs-lookup"><span data-stu-id="8a0f3-150">`result2` is 3072 (0000 1100 0000 0000).</span></span>  
  
- <span data-ttu-id="8a0f3-151">`result3` is -32768 (1000 0000 0000 0000).</span><span class="sxs-lookup"><span data-stu-id="8a0f3-151">`result3` is -32768 (1000 0000 0000 0000).</span></span>  
  
- <span data-ttu-id="8a0f3-152">`result4` is 384 (0000 0001 1000 0000).</span><span class="sxs-lookup"><span data-stu-id="8a0f3-152">`result4` is 384 (0000 0001 1000 0000).</span></span>  
  
- <span data-ttu-id="8a0f3-153">`result5` est égal à 0 (décalé de 15 places vers la gauche).</span><span class="sxs-lookup"><span data-stu-id="8a0f3-153">`result5` is 0 (shifted 15 places to the left).</span></span>  
  
 <span data-ttu-id="8a0f3-154">Le nombre de positions de décalage pour `result4` est calculé comme 17 AND 15, ce qui est égal à 1.</span><span class="sxs-lookup"><span data-stu-id="8a0f3-154">The shift amount for `result4` is calculated as 17 AND 15, which equals 1.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a0f3-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a0f3-155">See also</span></span>

- [<span data-ttu-id="8a0f3-156">Opérateurs de décalage de bits</span><span class="sxs-lookup"><span data-stu-id="8a0f3-156">Bit Shift Operators</span></span>](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [<span data-ttu-id="8a0f3-157">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="8a0f3-157">Assignment Operators</span></span>](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [<span data-ttu-id="8a0f3-158"><<= (opérateur)</span><span class="sxs-lookup"><span data-stu-id="8a0f3-158"><<= Operator</span></span>](../../../visual-basic/language-reference/operators/left-shift-assignment-operator.md)
- [<span data-ttu-id="8a0f3-159">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8a0f3-159">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="8a0f3-160">Opérateurs répertoriés par fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="8a0f3-160">Operators Listed by Functionality</span></span>](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [<span data-ttu-id="8a0f3-161">Opérateurs arithmétiques en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8a0f3-161">Arithmetic Operators in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)
