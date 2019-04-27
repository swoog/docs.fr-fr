---
title: 'Procédure : Forcer un Argument d’être passés par valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- procedure arguments
- Visual Basic code, procedures
- arguments [Visual Basic], ByVal
- arguments [Visual Basic], passing by value
- procedure parameters
- procedures [Visual Basic], calling
- arguments [Visual Basic], in parentheses
- procedure arguments [Visual Basic], in parentheses
- arguments [Visual Basic], changing value
ms.assetid: 77b4f2d2-1055-4c2f-a521-874d1db86946
ms.openlocfilehash: 497ae11b858b7d164ba3b5607ff2109254a154de
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61863621"
---
# <a name="how-to-force-an-argument-to-be-passed-by-value-visual-basic"></a><span data-ttu-id="b7b6a-102">Procédure : Forcer un Argument d’être passés par valeur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b7b6a-102">How to: Force an Argument to Be Passed by Value (Visual Basic)</span></span>
<span data-ttu-id="b7b6a-103">La déclaration de procédure détermine le mécanisme de passage.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-103">The procedure declaration determines the passing mechanism.</span></span> <span data-ttu-id="b7b6a-104">Si un paramètre est déclaré [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), Visual Basic s’attend à passer l’argument correspondant par référence.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-104">If a parameter is declared [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), Visual Basic expects to pass the corresponding argument by reference.</span></span> <span data-ttu-id="b7b6a-105">Ainsi, la procédure modifier la valeur de l’élément de programmation sous-jacent à l’argument dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-105">This allows the procedure to change the value of the programming element underlying the argument in the calling code.</span></span> <span data-ttu-id="b7b6a-106">Si vous souhaitez protéger l’élément sous-jacent contre une telle modification, vous pouvez remplacer le `ByRef` appeler de mécanisme de passage dans la procédure en plaçant le nom de l’argument entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-106">If you wish to protect the underlying element against such change, you can override the `ByRef` passing mechanism in the procedure call by enclosing the argument name in parentheses.</span></span> <span data-ttu-id="b7b6a-107">Ces parenthèses sont ajoutent les parenthèses entourant la liste d’arguments de l’appel.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-107">These parentheses are in addition to the parentheses enclosing the argument list in the call.</span></span>  
  
 <span data-ttu-id="b7b6a-108">Le code appelant ne peut pas remplacer un [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) mécanisme.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-108">The calling code cannot override a [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) mechanism.</span></span>  
  
### <a name="to-force-an-argument-to-be-passed-by-value"></a><span data-ttu-id="b7b6a-109">Pour forcer un argument à passer par valeur</span><span class="sxs-lookup"><span data-stu-id="b7b6a-109">To force an argument to be passed by value</span></span>  
  
-   <span data-ttu-id="b7b6a-110">Si le paramètre correspondant est déclaré `ByVal` dans la procédure, vous n’avez pas besoin de prendre des mesures supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-110">If the corresponding parameter is declared `ByVal` in the procedure, you do not need to take any additional steps.</span></span> <span data-ttu-id="b7b6a-111">Visual Basic doit déjà passer l’argument par valeur.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-111">Visual Basic already expects to pass the argument by value.</span></span>  
  
-   <span data-ttu-id="b7b6a-112">Si le paramètre correspondant est déclaré `ByRef` dans la procédure, mettez l’argument entre parenthèses dans l’appel de procédure.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-112">If the corresponding parameter is declared `ByRef` in the procedure, enclose the argument in parentheses in the procedure call.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b7b6a-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="b7b6a-113">Example</span></span>  
 <span data-ttu-id="b7b6a-114">L’exemple suivant substitue un `ByRef` déclaration de paramètre.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-114">The following example overrides a `ByRef` parameter declaration.</span></span> <span data-ttu-id="b7b6a-115">Dans l’appel qui force `ByVal`, notez les deux niveaux de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-115">In the call that forces `ByVal`, note the two levels of parentheses.</span></span>  
  
 [!code-vb[VbVbcnProcedures#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#39)]  
  
 [!code-vb[VbVbcnProcedures#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#40)]  
  
 <span data-ttu-id="b7b6a-116">Lorsque `str` est placée entre parenthèses supplémentaires dans la liste d’arguments, le `setNewString` procédure ne peut pas modifier sa valeur dans le code appelant, et `MsgBox` affiche « Ne peut pas être remplacé si passé ByVal ».</span><span class="sxs-lookup"><span data-stu-id="b7b6a-116">When `str` is enclosed in extra parentheses within the argument list, the `setNewString` procedure cannot change its value in the calling code, and `MsgBox` displays "Cannot be replaced if passed ByVal".</span></span> <span data-ttu-id="b7b6a-117">Lorsque `str` n’est pas placée entre parenthèses supplémentaires, la procédure peut le modifier, et `MsgBox` affiche « Il s’agit d’une nouvelle valeur pour l’argument inString. »</span><span class="sxs-lookup"><span data-stu-id="b7b6a-117">When `str` is not enclosed in extra parentheses, the procedure can change it, and `MsgBox` displays "This is a new value for the inString argument."</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="b7b6a-118">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="b7b6a-118">Compiling the Code</span></span>  
 <span data-ttu-id="b7b6a-119">Lorsque vous passez une variable par référence, vous devez utiliser le `ByRef` mot clé pour spécifier ce mécanisme.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-119">When you pass a variable by reference, you must use the `ByRef` keyword to specify this mechanism.</span></span>  
  
 <span data-ttu-id="b7b6a-120">La valeur par défaut en Visual Basic consiste à passer des arguments par valeur.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-120">The default in Visual Basic is to pass arguments by value.</span></span> <span data-ttu-id="b7b6a-121">Toutefois, il est conseillé en programmation pour inclure le [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) ou [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) keyword avec chaque paramètre déclaré.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-121">However, it is good programming practice to include either the [ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) or [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md) keyword with every declared parameter.</span></span> <span data-ttu-id="b7b6a-122">Cela rend votre code plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-122">This makes your code easier to read.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="b7b6a-123">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="b7b6a-123">Robust Programming</span></span>  
 <span data-ttu-id="b7b6a-124">Si une procédure déclare un paramètre [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), l’exécution correcte du code peut dépendre de la possibilité de modifier l’élément sous-jacent dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-124">If a procedure declares a parameter [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md), the correct execution of the code might depend on being able to change the underlying element in the calling code.</span></span> <span data-ttu-id="b7b6a-125">Si le code appelant substitue ce mécanisme appelant en plaçant l’argument entre parenthèses, ou s’il passe un argument non modifiable, la procédure ne peut pas modifier l’élément sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-125">If the calling code overrides this calling mechanism by enclosing the argument in parentheses, or if it passes a nonmodifiable argument, the procedure cannot change the underlying element.</span></span> <span data-ttu-id="b7b6a-126">Cela peut produire des résultats inattendus dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-126">This might produce unexpected results in the calling code.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="b7b6a-127">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="b7b6a-127">.NET Framework Security</span></span>  
 <span data-ttu-id="b7b6a-128">Il y a toujours un risque de permettre à une procédure modifier la valeur sous-jacente à un argument dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-128">There is always a potential risk in allowing a procedure to change the value underlying an argument in the calling code.</span></span> <span data-ttu-id="b7b6a-129">Assurez-vous que cette valeur pour être modifié et être prêt à vérifier la validité avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b7b6a-129">Make sure you expect this value to be changed, and be prepared to check it for validity before using it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7b6a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7b6a-130">See also</span></span>

- [<span data-ttu-id="b7b6a-131">Procédures</span><span class="sxs-lookup"><span data-stu-id="b7b6a-131">Procedures</span></span>](./index.md)
- [<span data-ttu-id="b7b6a-132">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="b7b6a-132">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="b7b6a-133">Guide pratique pour Passer des Arguments à une procédure</span><span class="sxs-lookup"><span data-stu-id="b7b6a-133">How to: Pass Arguments to a Procedure</span></span>](./how-to-pass-arguments-to-a-procedure.md)
- [<span data-ttu-id="b7b6a-134">Passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="b7b6a-134">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="b7b6a-135">Différences entre les arguments modifiables et non modifiables</span><span class="sxs-lookup"><span data-stu-id="b7b6a-135">Differences Between Modifiable and Nonmodifiable Arguments</span></span>](./differences-between-modifiable-and-nonmodifiable-arguments.md)
- [<span data-ttu-id="b7b6a-136">Différences entre le passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="b7b6a-136">Differences Between Passing an Argument By Value and By Reference</span></span>](./differences-between-passing-an-argument-by-value-and-by-reference.md)
- [<span data-ttu-id="b7b6a-137">Guide pratique pour Modifier la valeur d’un Argument de procédure</span><span class="sxs-lookup"><span data-stu-id="b7b6a-137">How to: Change the Value of a Procedure Argument</span></span>](./how-to-change-the-value-of-a-procedure-argument.md)
- [<span data-ttu-id="b7b6a-138">Guide pratique pour Protéger un Argument de procédure contre les modifications de valeur</span><span class="sxs-lookup"><span data-stu-id="b7b6a-138">How to: Protect a Procedure Argument Against Value Changes</span></span>](./how-to-protect-a-procedure-argument-against-value-changes.md)
- [<span data-ttu-id="b7b6a-139">Passage des arguments par position et par nom</span><span class="sxs-lookup"><span data-stu-id="b7b6a-139">Passing Arguments by Position and by Name</span></span>](./passing-arguments-by-position-and-by-name.md)
- [<span data-ttu-id="b7b6a-140">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="b7b6a-140">Value Types and Reference Types</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
