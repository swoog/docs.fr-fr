---
title: Fonction CType (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.CType
helpviewer_keywords:
- expression conversion results
- explicit data type conversions [Visual Basic]
- CType function
- conversions [Visual Basic], expression
ms.assetid: dd4b29e7-6fa1-428c-877e-69955420bb72
ms.openlocfilehash: 77bff81efbd61a68c054519710bd671d90af1e7c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54694774"
---
# <a name="ctype-function-visual-basic"></a><span data-ttu-id="81b11-102">Fonction CType (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="81b11-102">CType Function (Visual Basic)</span></span>
<span data-ttu-id="81b11-103">Retourne le résultat de la conversion explicite d’une expression en un type de données spécifié, objet, structure, classe ou interface.</span><span class="sxs-lookup"><span data-stu-id="81b11-103">Returns the result of explicitly converting an expression to a specified data type, object, structure, class, or interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81b11-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81b11-104">Syntax</span></span>  
  
```  
CType(expression, typename)  
```  
  
## <a name="parts"></a><span data-ttu-id="81b11-105">Composants</span><span class="sxs-lookup"><span data-stu-id="81b11-105">Parts</span></span>  
 `expression`  
 <span data-ttu-id="81b11-106">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="81b11-106">Any valid expression.</span></span> <span data-ttu-id="81b11-107">Si la valeur de `expression` est en dehors de la plage autorisée par `typename`, Visual Basic lève une exception.</span><span class="sxs-lookup"><span data-stu-id="81b11-107">If the value of `expression` is outside the range allowed by `typename`, Visual Basic throws an exception.</span></span>  
  
 `typename`  
 <span data-ttu-id="81b11-108">Toute expression qui est autorisée dans un `As` clause dans un `Dim` instruction, autrement dit, le nom de n’importe quel type de données objet, structure, classe ou interface.</span><span class="sxs-lookup"><span data-stu-id="81b11-108">Any expression that is legal within an `As` clause in a `Dim` statement, that is, the name of any data type, object, structure, class, or interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="81b11-109">Notes</span><span class="sxs-lookup"><span data-stu-id="81b11-109">Remarks</span></span>  
  
> [!TIP]
>  <span data-ttu-id="81b11-110">Vous pouvez également utiliser les fonctions suivantes pour effectuer une conversion de type :</span><span class="sxs-lookup"><span data-stu-id="81b11-110">You can also use the following functions to perform a type conversion:</span></span>  
>   
>  -   <span data-ttu-id="81b11-111">Fonctions de conversion de type comme `CByte`, `CDbl`, et `CInt` qui effectuent une conversion vers un type de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="81b11-111">Type conversion functions such as `CByte`, `CDbl`, and `CInt` that perform a conversion to a specific data type.</span></span> <span data-ttu-id="81b11-112">Pour plus d’informations, consultez [les fonctions de Conversion de Type](../../../visual-basic/language-reference/functions/type-conversion-functions.md).</span><span class="sxs-lookup"><span data-stu-id="81b11-112">For more information, see [Type Conversion Functions](../../../visual-basic/language-reference/functions/type-conversion-functions.md).</span></span>  
> -   <span data-ttu-id="81b11-113">[Opérateur DirectCast](../../../visual-basic/language-reference/operators/directcast-operator.md) ou [opérateur TryCast](../../../visual-basic/language-reference/operators/trycast-operator.md).</span><span class="sxs-lookup"><span data-stu-id="81b11-113">[DirectCast Operator](../../../visual-basic/language-reference/operators/directcast-operator.md) or [TryCast Operator](../../../visual-basic/language-reference/operators/trycast-operator.md).</span></span> <span data-ttu-id="81b11-114">Ces opérateurs requièrent qu’un type hérite ou implémenter l’autre type.</span><span class="sxs-lookup"><span data-stu-id="81b11-114">These operators require that one type inherit from or implement the other type.</span></span> <span data-ttu-id="81b11-115">Ils peuvent fournir des performances légèrement supérieures que `CType` lors de la conversion vers et depuis le `Object` type de données.</span><span class="sxs-lookup"><span data-stu-id="81b11-115">They can provide somewhat better performance than `CType` when converting to and from the `Object` data type.</span></span>  
  
 <span data-ttu-id="81b11-116">`CType` est compilé "inline", ce qui signifie que le code de conversion fait partie du code qui évalue l’expression.</span><span class="sxs-lookup"><span data-stu-id="81b11-116">`CType` is compiled inline, which means that the conversion code is part of the code that evaluates the expression.</span></span> <span data-ttu-id="81b11-117">Dans certains cas, le code s’exécute plus rapidement, car aucune procédure n’est appelées pour effectuer la conversion.</span><span class="sxs-lookup"><span data-stu-id="81b11-117">In some cases, the code runs faster because no procedures are called to perform the conversion.</span></span>  
  
 <span data-ttu-id="81b11-118">Si aucune conversion n’est définie à partir de `expression` à `typename` (par exemple, à partir de `Integer` à `Date`), Visual Basic affiche un message d’erreur de compilation.</span><span class="sxs-lookup"><span data-stu-id="81b11-118">If no conversion is defined from `expression` to `typename` (for example, from `Integer` to `Date`), Visual Basic displays a compile-time error message.</span></span>  
  
 <span data-ttu-id="81b11-119">Si une conversion échoue au moment de l’exécution, l’exception appropriée est levée.</span><span class="sxs-lookup"><span data-stu-id="81b11-119">If a conversion fails at run time, the appropriate exception is thrown.</span></span> <span data-ttu-id="81b11-120">Si une conversion restrictive échoue, un <xref:System.OverflowException> est le résultat le plus courant.</span><span class="sxs-lookup"><span data-stu-id="81b11-120">If a narrowing conversion fails, an <xref:System.OverflowException> is the most common result.</span></span> <span data-ttu-id="81b11-121">Si la conversion n’est pas définie, un <xref:System.InvalidCastException> dans levée.</span><span class="sxs-lookup"><span data-stu-id="81b11-121">If the conversion is undefined, an <xref:System.InvalidCastException> in thrown.</span></span> <span data-ttu-id="81b11-122">Par exemple, cela peut se produire si `expression` est de type `Object` et son type au moment de l’exécution n’a pas de conversion `typename`.</span><span class="sxs-lookup"><span data-stu-id="81b11-122">For example, this can happen  if `expression` is of type `Object` and its run-time type has no conversion to `typename`.</span></span>  
  
 <span data-ttu-id="81b11-123">Si le type de données de `expression` ou `typename` est une classe ou une structure que vous avez définie, vous pouvez définir `CType` sur cette classe ou structure comme un opérateur de conversion.</span><span class="sxs-lookup"><span data-stu-id="81b11-123">If the data type of `expression` or `typename` is a class or structure you've defined, you can define `CType` on that class or structure as a conversion operator.</span></span> <span data-ttu-id="81b11-124">Cela rend `CType` agissent comme un *opérateur surchargé*.</span><span class="sxs-lookup"><span data-stu-id="81b11-124">This makes `CType` act as an *overloaded operator*.</span></span> <span data-ttu-id="81b11-125">Si vous procédez ainsi, vous pouvez contrôler le comportement des conversions vers et à partir de votre classe ou structure, y compris les exceptions pouvant être levées.</span><span class="sxs-lookup"><span data-stu-id="81b11-125">If you do this, you can control the behavior of conversions to and from your class or structure, including the exceptions that can be thrown.</span></span>  
  
## <a name="overloading"></a><span data-ttu-id="81b11-126">Surcharge</span><span class="sxs-lookup"><span data-stu-id="81b11-126">Overloading</span></span>  
 <span data-ttu-id="81b11-127">Le `CType` peut également être surchargé sur une classe ou structure définie en dehors de votre code.</span><span class="sxs-lookup"><span data-stu-id="81b11-127">The `CType` operator can also be overloaded on a class or structure defined outside your code.</span></span> <span data-ttu-id="81b11-128">Si votre code convertit vers ou à partir d’une classe ou une structure, veillez à ce que vous comprenez le comportement de ses `CType` opérateur.</span><span class="sxs-lookup"><span data-stu-id="81b11-128">If your code converts to or from such a class or structure, be sure you understand the behavior of its `CType` operator.</span></span> <span data-ttu-id="81b11-129">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="81b11-129">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="converting-dynamic-objects"></a><span data-ttu-id="81b11-130">Conversion d’objets dynamiques</span><span class="sxs-lookup"><span data-stu-id="81b11-130">Converting Dynamic Objects</span></span>  
 <span data-ttu-id="81b11-131">Conversions de type des objets dynamiques sont effectuées par les conversions dynamiques définies par l’utilisateur qui utilisent le <xref:System.Dynamic.DynamicObject.TryConvert%2A> ou <xref:System.Dynamic.DynamicMetaObject.BindConvert%2A> méthodes.</span><span class="sxs-lookup"><span data-stu-id="81b11-131">Type conversions of dynamic objects are performed by user-defined dynamic conversions that use the <xref:System.Dynamic.DynamicObject.TryConvert%2A> or <xref:System.Dynamic.DynamicMetaObject.BindConvert%2A> methods.</span></span> <span data-ttu-id="81b11-132">Si vous travaillez avec des objets dynamiques, utilisez le <xref:Microsoft.VisualBasic.Conversion.CTypeDynamic%2A> méthode pour convertir l’objet dynamique.</span><span class="sxs-lookup"><span data-stu-id="81b11-132">If you're working with dynamic objects, use the <xref:Microsoft.VisualBasic.Conversion.CTypeDynamic%2A> method to convert the dynamic object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="81b11-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="81b11-133">Example</span></span>  
 <span data-ttu-id="81b11-134">L’exemple suivant utilise le `CType` fonction pour convertir une expression à la `Single` type de données.</span><span class="sxs-lookup"><span data-stu-id="81b11-134">The following example uses the `CType` function to convert an expression to the `Single` data type.</span></span>  
  
 [!code-vb[VbVbalrFunctions#24](../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/ctype-function_1.vb)]  
  
 <span data-ttu-id="81b11-135">Pour obtenir des exemples supplémentaires, consultez [Conversions implicites et explicites](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md).</span><span class="sxs-lookup"><span data-stu-id="81b11-135">For additional examples, see [Implicit and Explicit Conversions](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81b11-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81b11-136">See also</span></span>
- <xref:System.OverflowException>
- <xref:System.InvalidCastException>
- [<span data-ttu-id="81b11-137">Fonctions de conversion de types</span><span class="sxs-lookup"><span data-stu-id="81b11-137">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [<span data-ttu-id="81b11-138">Fonctions de conversion</span><span class="sxs-lookup"><span data-stu-id="81b11-138">Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/conversion-functions.md)
- [<span data-ttu-id="81b11-139">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="81b11-139">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)
- [<span data-ttu-id="81b11-140">Guide pratique pour Définir un opérateur de Conversion</span><span class="sxs-lookup"><span data-stu-id="81b11-140">How to: Define a Conversion Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="81b11-141">Conversion de type dans le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="81b11-141">Type Conversion in the .NET Framework</span></span>](../../../standard/base-types/type-conversion.md)
