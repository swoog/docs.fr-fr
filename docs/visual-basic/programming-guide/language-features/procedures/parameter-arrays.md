---
title: Tableaux de paramètres (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- parameter arrays [Visual Basic], about parameter arrays
- ParamArray keyword [Visual Basic], parameter arrays
- Visual Basic code, procedures
- parameters [Visual Basic], parameter arrays
- arguments [Visual Basic], parameter arrays
- procedures [Visual Basic], indefinite number of argument values
- arrays [Visual Basic], parameter arrays
ms.assetid: c43edfae-9114-4096-9ebc-8c5c957a1067
ms.openlocfilehash: 8ea4c77056701b8f61c1ed5a53cf20d98ae913bc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791948"
---
# <a name="parameter-arrays-visual-basic"></a><span data-ttu-id="d8427-102">Tableaux de paramètres (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8427-102">Parameter Arrays (Visual Basic)</span></span>
<span data-ttu-id="d8427-103">En règle générale, vous ne pouvez pas appeler une procédure avec plus d’arguments que spécifie la déclaration de procédure.</span><span class="sxs-lookup"><span data-stu-id="d8427-103">Usually, you cannot call a procedure with more arguments than the procedure declaration specifies.</span></span> <span data-ttu-id="d8427-104">Lorsque vous avez besoin d’un nombre indéfini d’arguments, vous pouvez déclarer un *tableau de paramètres*, ce qui permet à la procédure d’accepter un tableau de valeurs pour un paramètre.</span><span class="sxs-lookup"><span data-stu-id="d8427-104">When you need an indefinite number of arguments, you can declare a *parameter array*, which allows a procedure to accept an array of values for a parameter.</span></span> <span data-ttu-id="d8427-105">Il est inutile de connaître le nombre d’éléments dans le tableau de paramètres lorsque vous définissez la procédure.</span><span class="sxs-lookup"><span data-stu-id="d8427-105">You do not have to know the number of elements in the parameter array when you define the procedure.</span></span> <span data-ttu-id="d8427-106">La taille du tableau est déterminée individuellement par chaque appel à la procédure.</span><span class="sxs-lookup"><span data-stu-id="d8427-106">The array size is determined individually by each call to the procedure.</span></span>  
  
## <a name="declaring-a-paramarray"></a><span data-ttu-id="d8427-107">Déclaration d’un paramètre ParamArray</span><span class="sxs-lookup"><span data-stu-id="d8427-107">Declaring a ParamArray</span></span>  
 <span data-ttu-id="d8427-108">Vous utilisez le [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) mot clé pour désigner un tableau de paramètres dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d8427-108">You use the [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) keyword to denote a parameter array in the parameter list.</span></span> <span data-ttu-id="d8427-109">Les règles suivantes s'appliquent :</span><span class="sxs-lookup"><span data-stu-id="d8427-109">The following rules apply:</span></span>  
  
- <span data-ttu-id="d8427-110">Une procédure peut définir qu’un seul tableau de paramètres, et il doit être le dernier paramètre dans la définition de procédure.</span><span class="sxs-lookup"><span data-stu-id="d8427-110">A procedure can define only one parameter array, and it must be the last parameter in the procedure definition.</span></span>  
  
- <span data-ttu-id="d8427-111">Le tableau de paramètres doit être passé par valeur.</span><span class="sxs-lookup"><span data-stu-id="d8427-111">The parameter array must be passed by value.</span></span> <span data-ttu-id="d8427-112">Il est conseillé d’inclure explicitement les [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) mot clé dans la définition de procédure.</span><span class="sxs-lookup"><span data-stu-id="d8427-112">It is good programming practice to explicitly include the [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) keyword in the procedure definition.</span></span>  
  
- <span data-ttu-id="d8427-113">Le tableau de paramètres est automatiquement facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8427-113">The parameter array is automatically optional.</span></span> <span data-ttu-id="d8427-114">Sa valeur par défaut est un tableau unidimensionnel vide du type d’élément du tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d8427-114">Its default value is an empty one-dimensional array of the parameter array's element type.</span></span>  
  
- <span data-ttu-id="d8427-115">Tous les paramètres précédant le tableau de paramètres doivent être requis.</span><span class="sxs-lookup"><span data-stu-id="d8427-115">All parameters preceding the parameter array must be required.</span></span> <span data-ttu-id="d8427-116">Le tableau de paramètres doit être le seul paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8427-116">The parameter array must be the only optional parameter.</span></span>  
  
## <a name="calling-a-paramarray"></a><span data-ttu-id="d8427-117">Appel d’un ParamArray</span><span class="sxs-lookup"><span data-stu-id="d8427-117">Calling a ParamArray</span></span>  
 <span data-ttu-id="d8427-118">Lorsque vous appelez une procédure qui définit un tableau de paramètres, vous pouvez fournir l’argument dans l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8427-118">When you call a procedure that defines a parameter array, you can supply the argument in any one of the following ways:</span></span>  
  
- <span data-ttu-id="d8427-119">Aucune valeur, ce qui signifie que vous pouvez omettre le [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) argument.</span><span class="sxs-lookup"><span data-stu-id="d8427-119">Nothing — that is, you can omit the [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) argument.</span></span> <span data-ttu-id="d8427-120">Dans ce cas, un tableau vide est passé à la procédure.</span><span class="sxs-lookup"><span data-stu-id="d8427-120">In this case, an empty array is passed to the procedure.</span></span> <span data-ttu-id="d8427-121">Vous pouvez également passer le [rien](../../../../visual-basic/language-reference/nothing.md) mot clé, avec le même effet.</span><span class="sxs-lookup"><span data-stu-id="d8427-121">You can also pass the [Nothing](../../../../visual-basic/language-reference/nothing.md) keyword, with the same effect.</span></span>  
  
- <span data-ttu-id="d8427-122">Une liste d’un nombre arbitraire d’arguments, séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="d8427-122">A list of an arbitrary number of arguments, separated by commas.</span></span> <span data-ttu-id="d8427-123">Le type de données de chaque argument doit être implicitement convertible en le `ParamArray` type d’élément.</span><span class="sxs-lookup"><span data-stu-id="d8427-123">The data type of each argument must be implicitly convertible to the `ParamArray` element type.</span></span>  
  
- <span data-ttu-id="d8427-124">Un tableau avec le même type d’élément en tant que type d’élément du tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d8427-124">An array with the same element type as the parameter array's element type.</span></span>  
  
 <span data-ttu-id="d8427-125">Dans tous les cas, le code au sein de la procédure traite le tableau de paramètres comme un tableau unidimensionnel avec des éléments du même type de données en tant que le `ParamArray` type de données.</span><span class="sxs-lookup"><span data-stu-id="d8427-125">In all cases, the code within the procedure treats the parameter array as a one-dimensional array with elements of the same data type as the `ParamArray` data type.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d8427-126">Chaque fois que vous avez affaire à un tableau qui peut s’avérer indéfiniment volumineux, il existe un risque de saturer la capacité interne de votre application.</span><span class="sxs-lookup"><span data-stu-id="d8427-126">Whenever you deal with an array which can be indefinitely large, there is a risk of overrunning some internal capacity of your application.</span></span> <span data-ttu-id="d8427-127">Si vous acceptez un tableau de paramètres, vous devez tester la taille du tableau passé le code appelant.</span><span class="sxs-lookup"><span data-stu-id="d8427-127">If you accept a parameter array, you should test for the size of the array that the calling code passed to it.</span></span> <span data-ttu-id="d8427-128">Prendre les mesures appropriées si elle est trop grande pour votre application.</span><span class="sxs-lookup"><span data-stu-id="d8427-128">Take appropriate steps if it is too large for your application.</span></span> <span data-ttu-id="d8427-129">Pour plus d’informations, consultez [tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md).</span><span class="sxs-lookup"><span data-stu-id="d8427-129">For more information, see [Arrays](../../../../visual-basic/programming-guide/language-features/arrays/index.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d8427-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8427-130">Example</span></span>  
 <span data-ttu-id="d8427-131">L’exemple suivant définit et appelle la fonction `calcSum`.</span><span class="sxs-lookup"><span data-stu-id="d8427-131">The following example defines and calls the function `calcSum`.</span></span> <span data-ttu-id="d8427-132">Le `ParamArray` modificateur du paramètre `args` permet à la fonction d’accepter un nombre variable d’arguments.</span><span class="sxs-lookup"><span data-stu-id="d8427-132">The `ParamArray` modifier for the parameter `args` enables the function to accept a variable number of arguments.</span></span>  
  
 [!code-vb[VbVbalrStatements#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#26)]  
  
 <span data-ttu-id="d8427-133">L’exemple suivant définit une procédure avec un tableau de paramètres et génère les valeurs de tous les éléments du tableau passés au tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d8427-133">The following example defines a procedure with a parameter array, and outputs the values of all the array elements passed to the parameter array.</span></span>  
  
 [!code-vb[VbVbcnProcedures#48](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#48)]  
  
 [!code-vb[VbVbcnProcedures#49](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#49)]  
  
## <a name="see-also"></a><span data-ttu-id="d8427-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8427-134">See also</span></span>

- <xref:Microsoft.VisualBasic.Information.UBound%2A>
- [<span data-ttu-id="d8427-135">Procédures</span><span class="sxs-lookup"><span data-stu-id="d8427-135">Procedures</span></span>](./index.md)
- [<span data-ttu-id="d8427-136">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="d8427-136">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="d8427-137">Passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="d8427-137">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="d8427-138">Passage des arguments par position et par nom</span><span class="sxs-lookup"><span data-stu-id="d8427-138">Passing Arguments by Position and by Name</span></span>](./passing-arguments-by-position-and-by-name.md)
- [<span data-ttu-id="d8427-139">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="d8427-139">Optional Parameters</span></span>](./optional-parameters.md)
- [<span data-ttu-id="d8427-140">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="d8427-140">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="d8427-141">Tableaux</span><span class="sxs-lookup"><span data-stu-id="d8427-141">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [<span data-ttu-id="d8427-142">Optional</span><span class="sxs-lookup"><span data-stu-id="d8427-142">Optional</span></span>](../../../../visual-basic/language-reference/modifiers/optional.md)
