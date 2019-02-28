---
title: Considérations sur les surcharges de procédures (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- signatures [Visual Basic], ParamArray arguments
- ParamArray keyword [Visual Basic], parameter arrays
- ParamArray keyword [Visual Basic], arguments and signatures
- function overloading [Visual Basic], implicit overloads for ParamArray
- ParamArray keyword [Visual Basic], signatures
- Visual Basic code, procedures
- arguments [Visual Basic], parameter arrays
- procedures [Visual Basic], overloading
- parameters [Visual Basic], lists
- function overloading [Visual Basic], typeless programming
- typeless programming
- function overloading [Visual Basic], restrictions
- arguments [Visual Basic], optional
- optional arguments [Visual Basic], overloading
- signatures [Visual Basic], procedure
- parameter lists [Visual Basic]
- parameter arrays [Visual Basic], overloading arguments
- Visual Basic code, parameter lists
- procedure overloading [Visual Basic], considerations
- Option Explicit statement [Visual Basic]
- restrictions [Visual Basic], overloading procedures
- procedures [Visual Basic], parameter lists
ms.assetid: a2001248-10d0-42c5-b0ce-eeedc987319f
ms.openlocfilehash: 8dfee8a8678fb00fcded4b7da57c3b200ef64d69
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56979531"
---
# <a name="considerations-in-overloading-procedures-visual-basic"></a><span data-ttu-id="6282a-102">Considérations sur les surcharges de procédures (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6282a-102">Considerations in Overloading Procedures (Visual Basic)</span></span>
<span data-ttu-id="6282a-103">Lorsque vous surchargez une procédure, vous devez utiliser un autre *signature* pour chaque version surchargée.</span><span class="sxs-lookup"><span data-stu-id="6282a-103">When you overload a procedure, you must use a different *signature* for each overloaded version.</span></span> <span data-ttu-id="6282a-104">Cela signifie généralement que chaque version doit spécifier une liste de paramètres différente.</span><span class="sxs-lookup"><span data-stu-id="6282a-104">This usually means each version must specify a different parameter list.</span></span> <span data-ttu-id="6282a-105">Pour plus d’informations, consultez « Signature différente » dans [surcharge de procédure](./procedure-overloading.md).</span><span class="sxs-lookup"><span data-stu-id="6282a-105">For more information, see "Different Signature" in [Procedure Overloading](./procedure-overloading.md).</span></span>  
  
 <span data-ttu-id="6282a-106">Vous pouvez surcharger un `Function` procédure avec un `Sub` procédure et inversement, à condition qu’ils ont des signatures différentes.</span><span class="sxs-lookup"><span data-stu-id="6282a-106">You can overload a `Function` procedure with a `Sub` procedure, and vice versa, provided they have different signatures.</span></span> <span data-ttu-id="6282a-107">Deux surcharges ne peuvent pas différer uniquement par un a une valeur de retournée et l’autre n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="6282a-107">Two overloads cannot differ only in that one has a return value and the other does not.</span></span>  
  
 <span data-ttu-id="6282a-108">Vous pouvez surcharger une propriété de la même façon que vous surchargez une procédure et avec les mêmes restrictions.</span><span class="sxs-lookup"><span data-stu-id="6282a-108">You can overload a property the same way you overload a procedure, and with the same restrictions.</span></span> <span data-ttu-id="6282a-109">Toutefois, vous ne pouvez pas surcharger une procédure avec une propriété, ou vice versa.</span><span class="sxs-lookup"><span data-stu-id="6282a-109">However, you cannot overload a procedure with a property, or vice versa.</span></span>  
  
## <a name="alternatives-to-overloaded-versions"></a><span data-ttu-id="6282a-110">Alternatives aux Versions surchargées</span><span class="sxs-lookup"><span data-stu-id="6282a-110">Alternatives to Overloaded Versions</span></span>  
 <span data-ttu-id="6282a-111">Vous devez parfois des alternatives aux versions surchargées, en particulier lorsque la présence d’arguments est facultative ou leur nombre est variable.</span><span class="sxs-lookup"><span data-stu-id="6282a-111">You sometimes have alternatives to overloaded versions, particularly when the presence of arguments is optional or their number is variable.</span></span>  
  
 <span data-ttu-id="6282a-112">N’oubliez pas que les arguments facultatifs ne sont pas nécessairement prises en charge par tous les langages et tableaux de paramètres sont limités à Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6282a-112">Keep in mind that optional arguments are not necessarily supported by all languages, and parameter arrays are limited to Visual Basic.</span></span> <span data-ttu-id="6282a-113">Si vous écrivez une procédure qui est susceptible d’être appelée à partir du code écrit dans un des différents langages, les versions surchargées offrent la plus grande flexibilité.</span><span class="sxs-lookup"><span data-stu-id="6282a-113">If you are writing a procedure that is likely to be called from code written in any of several different languages, overloaded versions offer the greatest flexibility.</span></span>  
  
### <a name="overloads-and-optional-arguments"></a><span data-ttu-id="6282a-114">Surcharges et Arguments facultatifs</span><span class="sxs-lookup"><span data-stu-id="6282a-114">Overloads and Optional Arguments</span></span>  
 <span data-ttu-id="6282a-115">Lorsque le code appelant peut éventuellement fournir ou omettre un ou plusieurs arguments, vous pouvez définir plusieurs versions surchargées ou utiliser des paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="6282a-115">When the calling code can optionally supply or omit one or more arguments, you can define multiple overloaded versions or use optional parameters.</span></span>  
  
#### <a name="when-to-use-overloaded-versions"></a><span data-ttu-id="6282a-116">Quand utiliser des Versions surchargées</span><span class="sxs-lookup"><span data-stu-id="6282a-116">When to Use Overloaded Versions</span></span>  
 <span data-ttu-id="6282a-117">Vous pouvez envisager de définir une série de versions surchargées dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="6282a-117">You can consider defining a series of overloaded versions in the following cases:</span></span>  
  
-   <span data-ttu-id="6282a-118">La logique dans le code de procédure est considérablement différente selon que le code appelant fournit un argument facultatif ou non.</span><span class="sxs-lookup"><span data-stu-id="6282a-118">The logic in the procedure code is significantly different depending on whether the calling code supplies an optional argument or not.</span></span>  
  
-   <span data-ttu-id="6282a-119">Le code de procédure ne peut pas vérifier de manière fiable si le code appelant a fourni un argument facultatif.</span><span class="sxs-lookup"><span data-stu-id="6282a-119">The procedure code cannot reliably test whether the calling code has supplied an optional argument.</span></span> <span data-ttu-id="6282a-120">C’est le cas, par exemple, s’il n’existe aucun candidat possible pour une valeur par défaut que le code appelant n’était pas supposé fournir.</span><span class="sxs-lookup"><span data-stu-id="6282a-120">This is the case, for example, if there is no possible candidate for a default value that the calling code could not be expected to supply.</span></span>  
  
#### <a name="when-to-use-optional-parameters"></a><span data-ttu-id="6282a-121">Quand utiliser les paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="6282a-121">When to Use Optional Parameters</span></span>  
 <span data-ttu-id="6282a-122">Vous préférerez peut-être un ou plusieurs paramètres facultatifs dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="6282a-122">You might prefer one or more optional parameters in the following cases:</span></span>  
  
-   <span data-ttu-id="6282a-123">La seule action requise lorsque le code appelant ne fournit pas un argument facultatif consiste à définir le paramètre à une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="6282a-123">The only required action when the calling code does not supply an optional argument is to set the parameter to a default value.</span></span> <span data-ttu-id="6282a-124">Dans ce cas, le code de procédure peut être moins compliqué si vous définissez une version unique avec un ou plusieurs `Optional` paramètres.</span><span class="sxs-lookup"><span data-stu-id="6282a-124">In such a case, the procedure code can be less complicated if you define a single version with one or more `Optional` parameters.</span></span>  
  
 <span data-ttu-id="6282a-125">Pour plus d’informations, consultez [paramètres facultatifs](./optional-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6282a-125">For more information, see [Optional Parameters](./optional-parameters.md).</span></span>  
  
### <a name="overloads-and-paramarrays"></a><span data-ttu-id="6282a-126">Surcharges et ParamArrays</span><span class="sxs-lookup"><span data-stu-id="6282a-126">Overloads and ParamArrays</span></span>  
 <span data-ttu-id="6282a-127">Lorsque le code appelant peut passer un nombre variable d’arguments, vous pouvez définir plusieurs versions surchargées ou utiliser un tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="6282a-127">When the calling code can pass a variable number of arguments, you can define multiple overloaded versions or use a parameter array.</span></span>  
  
#### <a name="when-to-use-overloaded-versions"></a><span data-ttu-id="6282a-128">Quand utiliser des Versions surchargées</span><span class="sxs-lookup"><span data-stu-id="6282a-128">When to Use Overloaded Versions</span></span>  
 <span data-ttu-id="6282a-129">Vous pouvez envisager de définir une série de versions surchargées dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="6282a-129">You can consider defining a series of overloaded versions in the following cases:</span></span>  
  
-   <span data-ttu-id="6282a-130">Vous savez que le code appelant passe jamais plus qu’un petit nombre de valeurs au tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="6282a-130">You know that the calling code never passes more than a small number of values to the parameter array.</span></span>  
  
-   <span data-ttu-id="6282a-131">La logique dans le code de procédure est considérablement différente selon le nombre de valeurs transmet le code appelant.</span><span class="sxs-lookup"><span data-stu-id="6282a-131">The logic in the procedure code is significantly different depending on how many values the calling code passes.</span></span>  
  
-   <span data-ttu-id="6282a-132">Le code appelant peut passer des valeurs de différents types de données.</span><span class="sxs-lookup"><span data-stu-id="6282a-132">The calling code can pass values of different data types.</span></span>  
  
#### <a name="when-to-use-a-parameter-array"></a><span data-ttu-id="6282a-133">Quand utiliser un tableau de paramètres</span><span class="sxs-lookup"><span data-stu-id="6282a-133">When to Use a Parameter Array</span></span>  
 <span data-ttu-id="6282a-134">Il est préférable par un `ParamArray` paramètre dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="6282a-134">You are better served by a `ParamArray` parameter in the following cases:</span></span>  
  
-   <span data-ttu-id="6282a-135">Vous n’êtes pas en mesure de prédire combien de valeurs le code appelant peut passer au tableau de paramètres, et il peut être un grand nombre.</span><span class="sxs-lookup"><span data-stu-id="6282a-135">You are not able to predict how many values the calling code can pass to the parameter array, and it could be a large number.</span></span>  
  
-   <span data-ttu-id="6282a-136">La logique de la procédure se prête à l’itération sur toutes les valeurs que le code appelant passe, essentiellement les mêmes opérations sur chaque valeur.</span><span class="sxs-lookup"><span data-stu-id="6282a-136">The procedure logic lends itself to iterating through all the values the calling code passes, performing essentially the same operations on every value.</span></span>  
  
 <span data-ttu-id="6282a-137">Pour plus d’informations, consultez [tableaux de paramètres](./parameter-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="6282a-137">For more information, see [Parameter Arrays](./parameter-arrays.md).</span></span>  
  
## <a name="implicit-overloads-for-optional-parameters"></a><span data-ttu-id="6282a-138">Surcharges implicites pour les paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="6282a-138">Implicit Overloads for Optional Parameters</span></span>  
 <span data-ttu-id="6282a-139">Une procédure avec un [facultatif](../../../../visual-basic/language-reference/modifiers/optional.md) paramètre équivaut à deux procédures surchargées, une avec le paramètre facultatif et l’autre sans.</span><span class="sxs-lookup"><span data-stu-id="6282a-139">A procedure with an [Optional](../../../../visual-basic/language-reference/modifiers/optional.md) parameter is equivalent to two overloaded procedures, one with the optional parameter and one without it.</span></span> <span data-ttu-id="6282a-140">Vous ne pouvez pas surcharger une procédure avec une liste de paramètres correspondant aux deux.</span><span class="sxs-lookup"><span data-stu-id="6282a-140">You cannot overload such a procedure with a parameter list corresponding to either of these.</span></span> <span data-ttu-id="6282a-141">Les déclarations suivantes illustrent ce principe.</span><span class="sxs-lookup"><span data-stu-id="6282a-141">The following declarations illustrate this.</span></span>  
  
 [!code-vb[VbVbcnProcedures#58](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#58)]  
  
 [!code-vb[VbVbcnProcedures#60](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#60)]  
  
 [!code-vb[VbVbcnProcedures#61](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#61)]  
  
 <span data-ttu-id="6282a-142">Pour une procédure avec plus d’un paramètre facultatif, il existe un ensemble de surcharges implicites, est arrivé à logique, comme dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="6282a-142">For a procedure with more than one optional parameter, there is a set of implicit overloads, arrived at by logic similar to that in the preceding example.</span></span>  
  
## <a name="implicit-overloads-for-a-paramarray-parameter"></a><span data-ttu-id="6282a-143">Surcharges implicites pour un paramètre ParamArray</span><span class="sxs-lookup"><span data-stu-id="6282a-143">Implicit Overloads for a ParamArray Parameter</span></span>  
 <span data-ttu-id="6282a-144">Le compilateur considère qu’une procédure avec un [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) paramètre possède un nombre infini de surcharges, qui se différencient selon ce que le code appelant passe au tableau de paramètres, comme suit :</span><span class="sxs-lookup"><span data-stu-id="6282a-144">The compiler considers a procedure with a [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) parameter to have an infinite number of overloads, differing from each other in what the calling code passes to the parameter array, as follows:</span></span>  
  
-   <span data-ttu-id="6282a-145">Une surcharge lorsque le code appelant ne fournit pas un argument à la `ParamArray`</span><span class="sxs-lookup"><span data-stu-id="6282a-145">One overload for when the calling code does not supply an argument to the `ParamArray`</span></span>  
  
-   <span data-ttu-id="6282a-146">Une surcharge lorsque le code appelant fournit un tableau unidimensionnel de la `ParamArray` type d’élément</span><span class="sxs-lookup"><span data-stu-id="6282a-146">One overload for when the calling code supplies a one-dimensional array of the `ParamArray` element type</span></span>  
  
-   <span data-ttu-id="6282a-147">Pour chaque entier positif, une surcharge lorsque le code appelant fournit ce nombre d’arguments, chacun de la `ParamArray` type d’élément</span><span class="sxs-lookup"><span data-stu-id="6282a-147">For every positive integer, one overload for when the calling code supplies that number of arguments, each of the `ParamArray` element type</span></span>  
  
 <span data-ttu-id="6282a-148">Les déclarations suivantes illustrent ces surcharges implicites.</span><span class="sxs-lookup"><span data-stu-id="6282a-148">The following declarations illustrate these implicit overloads.</span></span>  
  
 [!code-vb[VbVbcnProcedures#68](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#68)]  
  
 [!code-vb[VbVbcnProcedures#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#70)]  
  
 <span data-ttu-id="6282a-149">Vous ne pouvez pas surcharger une procédure avec une liste de paramètres qui accepte un tableau unidimensionnel pour le tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="6282a-149">You cannot overload such a procedure with a parameter list that takes a one-dimensional array for the parameter array.</span></span> <span data-ttu-id="6282a-150">Toutefois, vous pouvez utiliser les signatures des autres surcharges implicites.</span><span class="sxs-lookup"><span data-stu-id="6282a-150">However, you can use the signatures of the other implicit overloads.</span></span> <span data-ttu-id="6282a-151">Les déclarations suivantes illustrent ce principe.</span><span class="sxs-lookup"><span data-stu-id="6282a-151">The following declarations illustrate this.</span></span>  
  
 [!code-vb[VbVbcnProcedures#71](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#71)]  
  
## <a name="typeless-programming-as-an-alternative-to-overloading"></a><span data-ttu-id="6282a-152">Programmation sans type comme Alternative à la surcharge</span><span class="sxs-lookup"><span data-stu-id="6282a-152">Typeless Programming as an Alternative to Overloading</span></span>  
 <span data-ttu-id="6282a-153">Si vous souhaitez autoriser le code appelant à passer différents types de données à un paramètre, une autre approche consiste à la programmation sans type.</span><span class="sxs-lookup"><span data-stu-id="6282a-153">If you want to allow the calling code to pass different data types to a parameter, an alternative approach is typeless programming.</span></span> <span data-ttu-id="6282a-154">Vous pouvez définir le commutateur de vérification de type `Off` avec soit le [Option Strict, instruction](../../../../visual-basic/language-reference/statements/option-strict-statement.md) ou [/optionstrict](../../../../visual-basic/reference/command-line-compiler/optionstrict.md) option du compilateur.</span><span class="sxs-lookup"><span data-stu-id="6282a-154">You can set the type checking switch to `Off` with either the [Option Strict Statement](../../../../visual-basic/language-reference/statements/option-strict-statement.md) or the [/optionstrict](../../../../visual-basic/reference/command-line-compiler/optionstrict.md) compiler option.</span></span> <span data-ttu-id="6282a-155">Puis vous n’êtes pas obligé de déclarer le type de données du paramètre.</span><span class="sxs-lookup"><span data-stu-id="6282a-155">Then you do not have to declare the parameter's data type.</span></span> <span data-ttu-id="6282a-156">Toutefois, cette approche présente les inconvénients suivants par rapport à la surcharge :</span><span class="sxs-lookup"><span data-stu-id="6282a-156">However, this approach has the following disadvantages compared to overloading:</span></span>  
  
-   <span data-ttu-id="6282a-157">Programmation sans type génère un code d’exécution moins efficace.</span><span class="sxs-lookup"><span data-stu-id="6282a-157">Typeless programming produces less efficient execution code.</span></span>  
  
-   <span data-ttu-id="6282a-158">La procédure doit tester pour chaque type de données que pouvant être passés.</span><span class="sxs-lookup"><span data-stu-id="6282a-158">The procedure must test for every data type it anticipates being passed.</span></span>  
  
-   <span data-ttu-id="6282a-159">Le compilateur ne peut pas signaler une erreur si le code appelant passe un type de données par la procédure ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="6282a-159">The compiler cannot signal an error if the calling code passes a data type that the procedure does not support.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6282a-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6282a-160">See also</span></span>
- [<span data-ttu-id="6282a-161">Procédures</span><span class="sxs-lookup"><span data-stu-id="6282a-161">Procedures</span></span>](./index.md)
- [<span data-ttu-id="6282a-162">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="6282a-162">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="6282a-163">Procédures de dépannage</span><span class="sxs-lookup"><span data-stu-id="6282a-163">Troubleshooting Procedures</span></span>](./troubleshooting-procedures.md)
- [<span data-ttu-id="6282a-164">Guide pratique pour Définir plusieurs Versions d’une procédure</span><span class="sxs-lookup"><span data-stu-id="6282a-164">How to: Define Multiple Versions of a Procedure</span></span>](./how-to-define-multiple-versions-of-a-procedure.md)
- [<span data-ttu-id="6282a-165">Guide pratique pour Appeler une procédure surchargée</span><span class="sxs-lookup"><span data-stu-id="6282a-165">How to: Call an Overloaded Procedure</span></span>](./how-to-call-an-overloaded-procedure.md)
- [<span data-ttu-id="6282a-166">Guide pratique pour Surcharger une procédure qui accepte des paramètres optionnels</span><span class="sxs-lookup"><span data-stu-id="6282a-166">How to: Overload a Procedure that Takes Optional Parameters</span></span>](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [<span data-ttu-id="6282a-167">Guide pratique pour Surcharger une procédure qui accepte un nombre indéfini de paramètres</span><span class="sxs-lookup"><span data-stu-id="6282a-167">How to: Overload a Procedure that Takes an Indefinite Number of Parameters</span></span>](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)
- [<span data-ttu-id="6282a-168">Résolution de surcharge</span><span class="sxs-lookup"><span data-stu-id="6282a-168">Overload Resolution</span></span>](./overload-resolution.md)
- [<span data-ttu-id="6282a-169">Overloads</span><span class="sxs-lookup"><span data-stu-id="6282a-169">Overloads</span></span>](../../../../visual-basic/language-reference/modifiers/overloads.md)
