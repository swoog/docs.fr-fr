---
title: 'Procédure : Surcharger une procédure qui accepte un nombre indéfini de paramètres (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], parameters
- procedure overloading [Visual Basic], indefinite number of parameters
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- procedure parameters
- procedures [Visual Basic], overloading
- procedures [Visual Basic], multiple versions
ms.assetid: c7042de2-2422-4039-94e8-ac298896af69
ms.openlocfilehash: bae420e88a74fbe3f7e8ad3592133fdcaf191029
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58838987"
---
# <a name="how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters-visual-basic"></a><span data-ttu-id="4cef2-102">Procédure : Surcharger une procédure qui accepte un nombre indéfini de paramètres (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4cef2-102">How to: Overload a Procedure that Takes an Indefinite Number of Parameters (Visual Basic)</span></span>
<span data-ttu-id="4cef2-103">Si une procédure possède un [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) paramètre, vous ne pouvez pas définir une version surchargée acceptant un tableau unidimensionnel pour le tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4cef2-103">If a procedure has a [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) parameter, you cannot define an overloaded version taking a one-dimensional array for the parameter array.</span></span> <span data-ttu-id="4cef2-104">Pour plus d’informations, consultez « Implicite des surcharges pour un paramètre ParamArray » dans [considérations dans les procédures de surcharge](./considerations-in-overloading-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="4cef2-104">For more information, see "Implicit Overloads for a ParamArray Parameter" in [Considerations in Overloading Procedures](./considerations-in-overloading-procedures.md).</span></span>  
  
### <a name="to-overload-a-procedure-that-takes-a-variable-number-of-parameters"></a><span data-ttu-id="4cef2-105">Surcharger une procédure qui accepte un nombre variable de paramètres</span><span class="sxs-lookup"><span data-stu-id="4cef2-105">To overload a procedure that takes a variable number of parameters</span></span>  
  
1.  <span data-ttu-id="4cef2-106">S’assurer que la procédure et les avantages de logique de code à partir de l’appel surchargées versions plus d’à partir d’un `ParamArray` paramètre.</span><span class="sxs-lookup"><span data-stu-id="4cef2-106">Ascertain that the procedure and calling code logic benefits from overloaded versions more than from a `ParamArray` parameter.</span></span> <span data-ttu-id="4cef2-107">Consultez « Surcharges et ParamArrays » dans [considérations sur les surcharges de procédures](./considerations-in-overloading-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="4cef2-107">See "Overloads and ParamArrays" in [Considerations in Overloading Procedures](./considerations-in-overloading-procedures.md).</span></span>  
  
2.  <span data-ttu-id="4cef2-108">Déterminer les numéros des valeurs fournies que la procédure doit accepter dans la partie variable de la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4cef2-108">Determine which numbers of supplied values the procedure should accept in the variable part of the parameter list.</span></span> <span data-ttu-id="4cef2-109">Cela peut inclure le cas d’aucune valeur, et il peut inclure le cas d’un tableau unidimensionnel unique.</span><span class="sxs-lookup"><span data-stu-id="4cef2-109">This might include the case of no value, and it might include the case of a single one-dimensional array.</span></span>  
  
3.  <span data-ttu-id="4cef2-110">Pour chaque nombre acceptable de valeurs fournies, écrivez un `Sub` ou `Function` instruction de déclaration qui définit la liste des paramètres correspondants.</span><span class="sxs-lookup"><span data-stu-id="4cef2-110">For each acceptable number of supplied values, write a `Sub` or `Function` declaration statement that defines the corresponding parameter list.</span></span> <span data-ttu-id="4cef2-111">N’utilisez pas le `Optional` ou `ParamArray` mot clé dans la version surchargée.</span><span class="sxs-lookup"><span data-stu-id="4cef2-111">Do not use either the `Optional` or the `ParamArray` keyword in this overloaded version.</span></span>  
  
4.  <span data-ttu-id="4cef2-112">Dans chaque déclaration, faites précéder le `Sub` ou `Function` mot clé avec le [surcharges](../../../../visual-basic/language-reference/modifiers/overloads.md) mot clé.</span><span class="sxs-lookup"><span data-stu-id="4cef2-112">In each declaration, precede the `Sub` or `Function` keyword with the [Overloads](../../../../visual-basic/language-reference/modifiers/overloads.md) keyword.</span></span>  
  
5.  <span data-ttu-id="4cef2-113">Après chaque déclaration, écrivez le code de procédure qui doit s’exécuter lorsque le code appelant fournit des valeurs correspondant à la liste des paramètres de cette déclaration.</span><span class="sxs-lookup"><span data-stu-id="4cef2-113">Following each declaration, write the procedure code that should execute when the calling code supplies values corresponding to that declaration's parameter list.</span></span>  
  
6.  <span data-ttu-id="4cef2-114">Terminez chaque procédure par le `End Sub` ou `End Function` instruction comme il convient.</span><span class="sxs-lookup"><span data-stu-id="4cef2-114">Terminate each procedure with the `End Sub` or `End Function` statement as appropriate.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4cef2-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="4cef2-115">Example</span></span>  
 <span data-ttu-id="4cef2-116">L’exemple suivant montre une procédure définie avec un [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) paramètre, puis sur un ensemble de procédures surchargées équivalent.</span><span class="sxs-lookup"><span data-stu-id="4cef2-116">The following example shows a procedure defined with a [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) parameter, and then an equivalent set of overloaded procedures.</span></span>  
  
 [!code-vb[VbVbcnProcedures#69](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#69)]  
  
 [!code-vb[VbVbcnProcedures#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#70)]  
  
 <span data-ttu-id="4cef2-117">Vous ne pouvez pas surcharger une procédure avec une liste de paramètres qui accepte un tableau unidimensionnel pour le tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="4cef2-117">You cannot overload such a procedure with a parameter list that takes a one-dimensional array for the parameter array.</span></span> <span data-ttu-id="4cef2-118">Toutefois, vous pouvez utiliser les signatures des autres surcharges implicites.</span><span class="sxs-lookup"><span data-stu-id="4cef2-118">However, you can use the signatures of the other implicit overloads.</span></span> <span data-ttu-id="4cef2-119">Les déclarations suivantes illustrent ce principe.</span><span class="sxs-lookup"><span data-stu-id="4cef2-119">The following declarations illustrate this.</span></span>  
  
 [!code-vb[VbVbcnProcedures#71](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#71)]  
  
 <span data-ttu-id="4cef2-120">Le code dans les versions surchargées n’a pas tester si le code appelant a fourni une ou plusieurs valeurs pour le `ParamArray` paramètre, ou si c’est le cas, combien.</span><span class="sxs-lookup"><span data-stu-id="4cef2-120">The code in the overloaded versions does not have to test whether the calling code supplied one or more values for the `ParamArray` parameter, or if so, how many.</span></span> <span data-ttu-id="4cef2-121">Visual Basic passe le contrôle à la version correspondant à la liste d’arguments appelante.</span><span class="sxs-lookup"><span data-stu-id="4cef2-121">Visual Basic passes control to the version matching the calling argument list.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="4cef2-122">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="4cef2-122">Compiling the Code</span></span>  
 <span data-ttu-id="4cef2-123">Car une procédure avec un `ParamArray` paramètre équivaut à un ensemble de versions surchargées, vous ne pouvez pas surcharger une procédure avec une liste de paramètres correspondant à chacune de ces surcharges implicites.</span><span class="sxs-lookup"><span data-stu-id="4cef2-123">Because a procedure with a `ParamArray` parameter is equivalent to a set of overloaded versions, you cannot overload such a procedure with a parameter list corresponding to any of these implicit overloads.</span></span> <span data-ttu-id="4cef2-124">Pour plus d’informations, consultez [considérations dans les procédures de surcharge](./considerations-in-overloading-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="4cef2-124">For more information, see [Considerations in Overloading Procedures](./considerations-in-overloading-procedures.md).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="4cef2-125">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="4cef2-125">.NET Framework Security</span></span>  
 <span data-ttu-id="4cef2-126">Chaque fois que vous avez affaire à un tableau qui peut s’avérer indéfiniment volumineux, il existe un risque de saturer la capacité interne de votre application.</span><span class="sxs-lookup"><span data-stu-id="4cef2-126">Whenever you deal with an array which can be indefinitely large, there is a risk of overrunning some internal capacity of your application.</span></span> <span data-ttu-id="4cef2-127">Si vous acceptez un tableau de paramètres, vous devez tester la longueur du tableau passé par le code appelant à celui-ci et prendre les mesures appropriées si elle est trop grande pour votre application.</span><span class="sxs-lookup"><span data-stu-id="4cef2-127">If you accept a parameter array, you should test for the length of the array the calling code passed to it, and take appropriate steps if it is too large for your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4cef2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cef2-128">See also</span></span>

- [<span data-ttu-id="4cef2-129">Procédures</span><span class="sxs-lookup"><span data-stu-id="4cef2-129">Procedures</span></span>](./index.md)
- [<span data-ttu-id="4cef2-130">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="4cef2-130">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="4cef2-131">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="4cef2-131">Optional Parameters</span></span>](./optional-parameters.md)
- [<span data-ttu-id="4cef2-132">tableaux de paramètres</span><span class="sxs-lookup"><span data-stu-id="4cef2-132">Parameter Arrays</span></span>](./parameter-arrays.md)
- [<span data-ttu-id="4cef2-133">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="4cef2-133">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="4cef2-134">Procédures de dépannage</span><span class="sxs-lookup"><span data-stu-id="4cef2-134">Troubleshooting Procedures</span></span>](./troubleshooting-procedures.md)
- [<span data-ttu-id="4cef2-135">Guide pratique pour Définir plusieurs Versions d’une procédure</span><span class="sxs-lookup"><span data-stu-id="4cef2-135">How to: Define Multiple Versions of a Procedure</span></span>](./how-to-define-multiple-versions-of-a-procedure.md)
- [<span data-ttu-id="4cef2-136">Guide pratique pour Appeler une procédure surchargée</span><span class="sxs-lookup"><span data-stu-id="4cef2-136">How to: Call an Overloaded Procedure</span></span>](./how-to-call-an-overloaded-procedure.md)
- [<span data-ttu-id="4cef2-137">Guide pratique pour Surcharger une procédure qui accepte des paramètres optionnels</span><span class="sxs-lookup"><span data-stu-id="4cef2-137">How to: Overload a Procedure that Takes Optional Parameters</span></span>](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [<span data-ttu-id="4cef2-138">Résolution de surcharge</span><span class="sxs-lookup"><span data-stu-id="4cef2-138">Overload Resolution</span></span>](./overload-resolution.md)
