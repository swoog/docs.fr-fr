---
title: Passage des arguments par position et par nom (Visual Basic)
ms.date: 02/01/2018
helpviewer_keywords:
- arguments [Visual Basic], passing by name
- procedures [Visual Basic], arguments
- := passing arguments
- procedure arguments
- Visual Basic code, procedures
- named arguments [Visual Basic], passing arguments
- arguments [Visual Basic], passing by position
- Function procedures [Visual Basic], passing arguments
- named parameters [Visual Basic], passing arguments
- named arguments
- passing parameters [Visual Basic], named parameter arguments
- passing parameters [Visual Basic], by position
- procedures [Visual Basic], calling
- named parameters
- Sub procedures [Visual Basic], passing arguments
- argument passing
- passing parameters [Visual Basic], by name
- argument passing [Visual Basic], by position
- arguments [Visual Basic], listing by name
ms.assetid: 1ad7358f-1da9-48da-a95b-f3c7ed41eff3
ms.openlocfilehash: bdaa0351e288b85a3e35818c0f53ef4d772932e5
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50183865"
---
# <a name="passing-arguments-by-position-and-by-name-visual-basic"></a><span data-ttu-id="c47d9-102">Passage des arguments par position et par nom (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c47d9-102">Passing Arguments by Position and by Name (Visual Basic)</span></span>
<span data-ttu-id="c47d9-103">Lorsque vous appelez un `Sub` ou `Function` procédure, vous pouvez passer des arguments *par position* , dans l’ordre dans lequel ils apparaissent dans la définition de la procédure, ou vous pouvez les transmettre *par nom*, sans vu les positionner.</span><span class="sxs-lookup"><span data-stu-id="c47d9-103">When you call a `Sub` or `Function` procedure, you can pass arguments *by position* — in the order in which they appear in the procedure's definition — or you can pass them *by name*, without regard to position.</span></span>  
  
 <span data-ttu-id="c47d9-104">Quand vous passez un argument par nom, vous spécifiez l’argument déclaré de le nom suivi d’un signe deux-points et un signe égal (`:=`), suivie de la valeur d’argument.</span><span class="sxs-lookup"><span data-stu-id="c47d9-104">When you pass an argument by name, you specify the argument's declared name followed by a colon and an equal sign (`:=`), followed by the argument value.</span></span> <span data-ttu-id="c47d9-105">Vous pouvez fournir des arguments nommés dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="c47d9-105">You can supply named arguments in any order.</span></span>  
  
 <span data-ttu-id="c47d9-106">Par exemple, ce qui suit `Sub` procédure accepte trois arguments :</span><span class="sxs-lookup"><span data-stu-id="c47d9-106">For example, the following `Sub` procedure takes three arguments:</span></span>  
  
 [!code-vb[SampleProcedure](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#1)]  
  
 <span data-ttu-id="c47d9-107">Lorsque vous appelez cette procédure, vous pouvez fournir les arguments par position, par nom ou à l’aide d’un mélange des deux.</span><span class="sxs-lookup"><span data-stu-id="c47d9-107">When you call this procedure, you can supply the arguments by position, by name, or by using a mixture of both.</span></span>  
  
## <a name="passing-arguments-by-position"></a><span data-ttu-id="c47d9-108">Passage des Arguments par Position</span><span class="sxs-lookup"><span data-stu-id="c47d9-108">Passing Arguments by Position</span></span>  
 <span data-ttu-id="c47d9-109">Vous pouvez appeler la `Display` méthode avec ses arguments passés par position et délimités par des virgules, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c47d9-109">You can call the `Display` method with its arguments passed by position and delimited by commas, as shown in the following example:</span></span>  
  
[!code-vb[ByPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#2)] 
  
 <span data-ttu-id="c47d9-110">Si vous omettez un argument facultatif dans une liste d’arguments positionnels, vous devez marquer son emplacement avec une virgule.</span><span class="sxs-lookup"><span data-stu-id="c47d9-110">If you omit an optional argument in a positional argument list, you must hold its place with a comma.</span></span> <span data-ttu-id="c47d9-111">L’exemple suivant appelle la `Display` méthode sans le `age` argument :</span><span class="sxs-lookup"><span data-stu-id="c47d9-111">The following example calls the `Display` method without the `age` argument:</span></span>  
  
[!code-vb[ByPositionWithOptionalArgument](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#3)] 
  
## <a name="passing-arguments-by-name"></a><span data-ttu-id="c47d9-112">Passage des Arguments par nom</span><span class="sxs-lookup"><span data-stu-id="c47d9-112">Passing Arguments by Name</span></span>  
 <span data-ttu-id="c47d9-113">Vous pouvez également appeler `Display` avec les arguments passés par nom, également délimitées par des virgules, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c47d9-113">Alternatively, you can call `Display` with the arguments passed by name, also delimited by commas, as shown in the following example:</span></span>  
  
[!code-vb[ByName](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#4)] 

 <span data-ttu-id="c47d9-114">Passer des arguments par nom de cette façon est particulièrement utile lorsque vous appelez une procédure qui possède plusieurs arguments facultatifs.</span><span class="sxs-lookup"><span data-stu-id="c47d9-114">Passing arguments by name in this way is especially useful when you call a procedure that has more than one optional argument.</span></span> <span data-ttu-id="c47d9-115">Si vous fournissez des arguments par nom, il est inutile d’utiliser des virgules consécutives pour signaler l’absence d’arguments positionnels.</span><span class="sxs-lookup"><span data-stu-id="c47d9-115">If you supply arguments by name, you do not have to use consecutive commas to denote missing positional arguments.</span></span> <span data-ttu-id="c47d9-116">Passer des arguments par nom rend également plus facile de suivre les arguments que vous transmettez et celles qui sont omis.</span><span class="sxs-lookup"><span data-stu-id="c47d9-116">Passing arguments by name also makes it easier to keep track of which arguments you are passing and which ones you are omitting.</span></span>  
  
## <a name="mixing-arguments-by-position-and-by-name"></a><span data-ttu-id="c47d9-117">Mélange d’Arguments par Position et par nom</span><span class="sxs-lookup"><span data-stu-id="c47d9-117">Mixing Arguments by Position and by Name</span></span>  

<span data-ttu-id="c47d9-118">Vous pouvez fournir des arguments par position et par nom dans un seul appel de procédure, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c47d9-118">You can supply arguments both by position and by name in a single procedure call, as shown in the following example:</span></span>  
  
[!code-vb[ByNameAndPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#5)] 
  
 <span data-ttu-id="c47d9-119">Dans l’exemple précédent, aucune virgule supplémentaire n’est nécessaire pour contenir le lieu du omis `age` argument, étant donné que `birth` est passé par nom.</span><span class="sxs-lookup"><span data-stu-id="c47d9-119">In the preceding example, no extra comma is necessary to hold the place of the omitted `age` argument, since `birth` is passed by name.</span></span>  
  
<span data-ttu-id="c47d9-120">Dans les versions de Visual Basic avant la version 15.5, lorsque vous fournissez des arguments par un mélange de position et le nom, les arguments positionnels doivent tous figurer en premier.</span><span class="sxs-lookup"><span data-stu-id="c47d9-120">In versions of Visual Basic before 15.5, when you supply arguments by a mixture of position and name, the positional arguments must all come first.</span></span> <span data-ttu-id="c47d9-121">Une fois que vous fournissez un argument par nom, tous les autres arguments doivent tous être passés par nom.</span><span class="sxs-lookup"><span data-stu-id="c47d9-121">Once you supply an argument by name, any remaining arguments must all be passed by name.</span></span>  <span data-ttu-id="c47d9-122">Par exemple, l’appel suivant à la `Display` méthode affiche l’erreur du compilateur [BC30241 : argument nommé attendu](../../../misc/bc30241.md).</span><span class="sxs-lookup"><span data-stu-id="c47d9-122">For example, the following call to the `Display` method displays compiler error [BC30241: Named argument expected](../../../misc/bc30241.md).</span></span>

[!code-vb[ByNameAndPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#6)] 

<span data-ttu-id="c47d9-123">À partir de Visual Basic 15.5, les arguments positionnels peuvent suivre les arguments nommés si les arguments de position de fin se trouvent dans la position correcte.</span><span class="sxs-lookup"><span data-stu-id="c47d9-123">Starting with Visual Basic 15.5, positional arguments can follow named arguments if the ending positional arguments are in the correct position.</span></span> <span data-ttu-id="c47d9-124">Si compilé sous Visual Basic 15.5, l’appel précédent à la `Display` méthode compile correctement et ne génère plus d’erreur du compilateur [BC30241](../../../misc/bc30241.md).</span><span class="sxs-lookup"><span data-stu-id="c47d9-124">If compiled under Visual Basic 15.5, the previous call to the `Display` method compiles successfully and no longer generates compiler error [BC30241](../../../misc/bc30241.md).</span></span>  

<span data-ttu-id="c47d9-125">Cette possibilité de combiner des arguments nommés et positionnels dans n’importe quel ordre est particulièrement utile lorsque vous souhaitez utiliser un argument nommé pour rendre votre code plus lisible.</span><span class="sxs-lookup"><span data-stu-id="c47d9-125">This ability to mix and match named and positional arguments in any order is particularly useful when you want to use a named argument to make your code more readable.</span></span> <span data-ttu-id="c47d9-126">Par exemple, ce qui suit `Person` constructeur de classe requiert deux arguments de type `Person`, qui peuvent être `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="c47d9-126">For example, the following `Person` class constructor requires two arguments of type `Person`, both of which can be `Nothing`.</span></span> 

[!code-vb[ByNameAndPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#7)] 

<span data-ttu-id="c47d9-127">À l’aide des arguments nommés et positionnels mixtes permet de faire l’intention du code effacer lorsque la valeur de la `father` et `mother` arguments est `Nothing`:</span><span class="sxs-lookup"><span data-stu-id="c47d9-127">Using mixed named and positional arguments helps to make the intent of the code clear when the value of the `father` and `mother` arguments is `Nothing`:</span></span>

[!code-vb[ByNameAndPosition](../../../../../samples/snippets/visualbasic/programming-guide/language-features/passing-named-arguments/module1.vb#8)] 

<span data-ttu-id="c47d9-128">Pour suivre des arguments de position avec des arguments nommés, vous devez ajouter l’élément suivant à votre projet Visual Basic (\*.vbproj) fichier :</span><span class="sxs-lookup"><span data-stu-id="c47d9-128">To follow positional arguments with named arguments, you must add the following element to your Visual Basic project (\*.vbproj) file:</span></span>

```xml
<PropertyGroup>
  <LangVersion>15.5</LangVersion>
</PropertyGroup>
```

<span data-ttu-id="c47d9-129">Pour plus d’informations, consultez [définition de la version de langage Visual Basic](../../../language-reference/configure-language-version.md).</span><span class="sxs-lookup"><span data-stu-id="c47d9-129">For more information see [setting the Visual Basic language version](../../../language-reference/configure-language-version.md).</span></span>

## <a name="restrictions-on-supplying-arguments-by-name"></a><span data-ttu-id="c47d9-130">Restrictions sur la fourniture des Arguments par nom</span><span class="sxs-lookup"><span data-stu-id="c47d9-130">Restrictions on Supplying Arguments by Name</span></span>  

<span data-ttu-id="c47d9-131">Vous ne pouvez pas passer des arguments par nom afin d’éviter d’entrer des arguments requis.</span><span class="sxs-lookup"><span data-stu-id="c47d9-131">You cannot pass arguments by name to avoid entering required arguments.</span></span> <span data-ttu-id="c47d9-132">Vous pouvez omettre les arguments facultatifs uniquement.</span><span class="sxs-lookup"><span data-stu-id="c47d9-132">You can omit only the optional arguments.</span></span>  
  
<span data-ttu-id="c47d9-133">Vous ne pouvez pas passer un tableau de paramètres par nom.</span><span class="sxs-lookup"><span data-stu-id="c47d9-133">You cannot pass a parameter array by name.</span></span> <span data-ttu-id="c47d9-134">Il s’agit, car lorsque vous appelez la procédure, vous fournissez un nombre indéfini de séparées par des virgules des arguments pour le tableau de paramètres, et le compilateur ne peut pas associer plusieurs arguments à un nom unique.</span><span class="sxs-lookup"><span data-stu-id="c47d9-134">This is because when you call the procedure, you supply an indefinite number of comma-separated arguments for the parameter array, and the compiler cannot associate more than one argument with a single name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c47d9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c47d9-135">See Also</span></span>  
 [<span data-ttu-id="c47d9-136">Procédures</span><span class="sxs-lookup"><span data-stu-id="c47d9-136">Procedures</span></span>](./index.md)  
 [<span data-ttu-id="c47d9-137">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="c47d9-137">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)  
 [<span data-ttu-id="c47d9-138">Guide pratique : passer des arguments à une procédure</span><span class="sxs-lookup"><span data-stu-id="c47d9-138">How to: Pass Arguments to a Procedure</span></span>](./how-to-pass-arguments-to-a-procedure.md)  
 [<span data-ttu-id="c47d9-139">Passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="c47d9-139">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)  
 [<span data-ttu-id="c47d9-140">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="c47d9-140">Optional Parameters</span></span>](./optional-parameters.md)  
 [<span data-ttu-id="c47d9-141">tableaux de paramètres</span><span class="sxs-lookup"><span data-stu-id="c47d9-141">Parameter Arrays</span></span>](./parameter-arrays.md)  
 [<span data-ttu-id="c47d9-142">Optional</span><span class="sxs-lookup"><span data-stu-id="c47d9-142">Optional</span></span>](../../../../visual-basic/language-reference/modifiers/optional.md)  
 [<span data-ttu-id="c47d9-143">ParamArray</span><span class="sxs-lookup"><span data-stu-id="c47d9-143">ParamArray</span></span>](../../../../visual-basic/language-reference/modifiers/paramarray.md)
