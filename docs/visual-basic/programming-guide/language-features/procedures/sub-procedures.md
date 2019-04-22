---
title: Procédures Sub (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Sub procedures [Visual Basic], about Sub procedures
- statement blocks
- Sub procedures [Visual Basic], calling
- procedures [Visual Basic], calling
- Sub procedures [Visual Basic], syntax
- Sub procedures
- procedures [Visual Basic], Sub
- syntax [Visual Basic], Sub procedures
ms.assetid: 6a0a4958-ed0a-4d3d-8d31-0772c82bda58
ms.openlocfilehash: b70594e002bbf08f0890586e78df901ccb26c7ce
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58843101"
---
# <a name="sub-procedures-visual-basic"></a><span data-ttu-id="f12bf-102">Procédures Sub (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f12bf-102">Sub Procedures (Visual Basic)</span></span>
<span data-ttu-id="f12bf-103">Un `Sub` procédure est une série d’instructions Visual Basic délimitée par le `Sub` et `End Sub` instructions.</span><span class="sxs-lookup"><span data-stu-id="f12bf-103">A `Sub` procedure is a series of Visual Basic statements enclosed by the `Sub` and `End Sub` statements.</span></span> <span data-ttu-id="f12bf-104">Le `Sub` procédure effectue une tâche, puis retourne le contrôle au code appelant, mais il ne retourne pas une valeur au code appelant.</span><span class="sxs-lookup"><span data-stu-id="f12bf-104">The `Sub` procedure performs a task and then returns control to the calling code, but it does not return a value to the calling code.</span></span>  
  
 <span data-ttu-id="f12bf-105">Chaque fois que la procédure est appelée, ses instructions sont exécutées, en commençant par la première instruction exécutable après le `Sub` instruction et se terminant par la première `End Sub`, `Exit Sub`, ou `Return` instruction rencontrée.</span><span class="sxs-lookup"><span data-stu-id="f12bf-105">Each time the procedure is called, its statements are executed, starting with the first executable statement after the `Sub` statement and ending with the first `End Sub`, `Exit Sub`, or `Return` statement encountered.</span></span>  
  
 <span data-ttu-id="f12bf-106">Vous pouvez définir un `Sub` procédure dans les modules, les classes et structures.</span><span class="sxs-lookup"><span data-stu-id="f12bf-106">You can define a `Sub` procedure in modules, classes, and structures.</span></span> <span data-ttu-id="f12bf-107">Par défaut, il est `Public`, ce qui signifie que vous pouvez l’appeler depuis n’importe où dans votre application qui a accès au module, classe ou structure dans laquelle vous l’avez définie.</span><span class="sxs-lookup"><span data-stu-id="f12bf-107">By default, it is `Public`, which means you can call it from anywhere in your application that has access to the module, class, or structure in which you defined it.</span></span> <span data-ttu-id="f12bf-108">Le terme, *méthode*, décrit une `Sub` ou `Function` procédure qui est accessible depuis l’extérieur de sa définition de module, classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="f12bf-108">The term, *method*, describes a `Sub` or `Function` procedure that is accessed from outside its defining module, class, or structure.</span></span> <span data-ttu-id="f12bf-109">Pour plus d’informations, consultez [Procédures](./index.md).</span><span class="sxs-lookup"><span data-stu-id="f12bf-109">For more information, see [Procedures](./index.md).</span></span>  
  
 <span data-ttu-id="f12bf-110">Un `Sub` procédure peut prendre des arguments, tels que les constantes, variables ou expressions qui sont passées par le code appelant.</span><span class="sxs-lookup"><span data-stu-id="f12bf-110">A `Sub` procedure can take arguments, such as constants, variables, or expressions, which are passed to it by the calling code.</span></span>  
  
## <a name="declaration-syntax"></a><span data-ttu-id="f12bf-111">Syntaxe de déclaration</span><span class="sxs-lookup"><span data-stu-id="f12bf-111">Declaration Syntax</span></span>  
 <span data-ttu-id="f12bf-112">La syntaxe pour déclarer un `Sub` procédure est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f12bf-112">The syntax for declaring a `Sub` procedure is as follows:</span></span>  
  
 <span data-ttu-id="f12bf-113">`[` *modificateurs* `] Sub` *subname* `[(` *parameterlist* `)]`</span><span class="sxs-lookup"><span data-stu-id="f12bf-113">`[` *modifiers* `] Sub`  *subname* `[(` *parameterlist* `)]`</span></span>  
  
 `' Statements of the Sub procedure.`  
  
 `End Sub`  
  
 <span data-ttu-id="f12bf-114">Le `modifiers` peut spécifier de niveau d’accès et des informations sur la surcharge, substitution, le partage et l’occultation.</span><span class="sxs-lookup"><span data-stu-id="f12bf-114">The `modifiers` can specify access level and information about overloading, overriding, sharing, and shadowing.</span></span> <span data-ttu-id="f12bf-115">Pour plus d’informations, consultez [Sub, instruction](../../../../visual-basic/language-reference/statements/sub-statement.md).</span><span class="sxs-lookup"><span data-stu-id="f12bf-115">For more information, see [Sub Statement](../../../../visual-basic/language-reference/statements/sub-statement.md).</span></span>  
  
## <a name="parameter-declaration"></a><span data-ttu-id="f12bf-116">Déclaration de paramètre</span><span class="sxs-lookup"><span data-stu-id="f12bf-116">Parameter Declaration</span></span>  
 <span data-ttu-id="f12bf-117">Vous déclarez chaque paramètre de procédure de la même façon pour comment vous déclarez une variable, en spécifiant le type de données et le nom de paramètre.</span><span class="sxs-lookup"><span data-stu-id="f12bf-117">You declare each procedure parameter similarly to how you declare a variable, specifying the parameter name and data type.</span></span> <span data-ttu-id="f12bf-118">Vous pouvez également spécifier le mécanisme de passage et indique si le paramètre est facultatif ou un tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f12bf-118">You can also specify the passing mechanism, and whether the parameter is optional or a parameter array.</span></span>  
  
 <span data-ttu-id="f12bf-119">La syntaxe pour chaque paramètre dans la liste de paramètres est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f12bf-119">The syntax for each parameter in the parameter list is as follows:</span></span>  
  
 <span data-ttu-id="f12bf-120">`[Optional] [ByVal | ByRef] [ParamArray]`  *parametername*  `As`  *datatype*</span><span class="sxs-lookup"><span data-stu-id="f12bf-120">`[Optional] [ByVal | ByRef] [ParamArray]`  *parametername*  `As`  *datatype*</span></span>  
  
 <span data-ttu-id="f12bf-121">Si le paramètre est facultatif, vous devez également fournir une valeur par défaut dans le cadre de sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="f12bf-121">If the parameter is optional, you must also supply a default value as part of its declaration.</span></span> <span data-ttu-id="f12bf-122">La syntaxe de spécification d’une valeur par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f12bf-122">The syntax for specifying a default value is as follows:</span></span>  
  
 <span data-ttu-id="f12bf-123">`Optional [ByVal | ByRef]`  *parametername*  `As`  *datatype*  `=`  *defaultvalue*</span><span class="sxs-lookup"><span data-stu-id="f12bf-123">`Optional [ByVal | ByRef]`  *parametername*  `As`  *datatype*  `=`  *defaultvalue*</span></span>  
  
### <a name="parameters-as-local-variables"></a><span data-ttu-id="f12bf-124">Paramètres en tant que Variables locales</span><span class="sxs-lookup"><span data-stu-id="f12bf-124">Parameters as Local Variables</span></span>  
 <span data-ttu-id="f12bf-125">Lorsque le contrôle passe à la procédure, chaque paramètre est traité comme une variable locale.</span><span class="sxs-lookup"><span data-stu-id="f12bf-125">When control passes to the procedure, each parameter is treated as a local variable.</span></span> <span data-ttu-id="f12bf-126">Cela signifie que sa durée de vie est identique à celui de la procédure et son étendue est l’ensemble de la procédure.</span><span class="sxs-lookup"><span data-stu-id="f12bf-126">This means that its lifetime is the same as that of the procedure, and its scope is the whole procedure.</span></span>  
  
## <a name="calling-syntax"></a><span data-ttu-id="f12bf-127">Syntaxe d’appel</span><span class="sxs-lookup"><span data-stu-id="f12bf-127">Calling Syntax</span></span>  
 <span data-ttu-id="f12bf-128">Vous appelez un `Sub` procédure explicitement avec une instruction d’appel autonome.</span><span class="sxs-lookup"><span data-stu-id="f12bf-128">You invoke a `Sub` procedure explicitly with a stand-alone calling statement.</span></span> <span data-ttu-id="f12bf-129">Vous ne pouvez pas l’appeler à l’aide de son nom dans une expression.</span><span class="sxs-lookup"><span data-stu-id="f12bf-129">You cannot call it by using its name in an expression.</span></span> <span data-ttu-id="f12bf-130">Vous devez fournir des valeurs pour tous les arguments qui ne sont pas facultatives, et vous devez placer la liste d’arguments entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="f12bf-130">You must provide values for all arguments that are not optional, and you must enclose the argument list in parentheses.</span></span> <span data-ttu-id="f12bf-131">Si aucun argument n’est fourni, vous pouvez éventuellement omettre les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="f12bf-131">If no arguments are supplied, you can optionally omit the parentheses.</span></span> <span data-ttu-id="f12bf-132">L’utilisation de la `Call` mot clé est facultative mais pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="f12bf-132">The use of the `Call` keyword is optional but not recommended.</span></span>  
  
 <span data-ttu-id="f12bf-133">La syntaxe pour un appel à une `Sub` procédure est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f12bf-133">The syntax for a call to a `Sub` procedure is as follows:</span></span>  
  
 <span data-ttu-id="f12bf-134">`[Call]`  *subname* `[(` *argumentlist* `)]`</span><span class="sxs-lookup"><span data-stu-id="f12bf-134">`[Call]`  *subname* `[(` *argumentlist* `)]`</span></span>  
  
 <span data-ttu-id="f12bf-135">Vous pouvez appeler un `Sub` méthode à partir en dehors de la classe qui le définit.</span><span class="sxs-lookup"><span data-stu-id="f12bf-135">You can call a `Sub` method from outside the class that defines it.</span></span> <span data-ttu-id="f12bf-136">Tout d’abord, vous devez utiliser le `New` mot clé pour créer une instance de la classe, ou appelez une méthode qui retourne une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="f12bf-136">First, you have to use the `New` keyword to create an instance of the class, or call a method that returns an instance of the class.</span></span> <span data-ttu-id="f12bf-137">Pour plus d’informations, consultez [nouvel opérateur](../../../../visual-basic/language-reference/operators/new-operator.md).</span><span class="sxs-lookup"><span data-stu-id="f12bf-137">For more information, see [New Operator](../../../../visual-basic/language-reference/operators/new-operator.md).</span></span> <span data-ttu-id="f12bf-138">Ensuite, vous pouvez utiliser la syntaxe suivante pour appeler le `Sub` méthode sur l’objet d’instance :</span><span class="sxs-lookup"><span data-stu-id="f12bf-138">Then, you can use the following syntax to call the `Sub` method on the instance object:</span></span>  
  
 <span data-ttu-id="f12bf-139">*Objet*. *MethodName*`[(`*argumentlist*`)]`</span><span class="sxs-lookup"><span data-stu-id="f12bf-139">*Object*.*methodname*`[(`*argumentlist*`)]`</span></span>  
  
### <a name="illustration-of-declaration-and-call"></a><span data-ttu-id="f12bf-140">Illustration de déclaration et d’appel</span><span class="sxs-lookup"><span data-stu-id="f12bf-140">Illustration of Declaration and Call</span></span>  
 <span data-ttu-id="f12bf-141">Ce qui suit `Sub` procédure indique à l’opérateur la tâche que l’application est sur le point d’effectuer et affiche également un horodatage.</span><span class="sxs-lookup"><span data-stu-id="f12bf-141">The following `Sub` procedure tells the computer operator which task the application is about to perform, and also displays a time stamp.</span></span> <span data-ttu-id="f12bf-142">Au lieu de répéter ce code au début de chaque tâche, l’application appelle simplement `tellOperator` à partir de différents emplacements.</span><span class="sxs-lookup"><span data-stu-id="f12bf-142">Instead of duplicating this code at the start of every task, the application just calls `tellOperator` from various locations.</span></span> <span data-ttu-id="f12bf-143">Chaque appel passe une chaîne dans le `task` argument qui identifie la tâche en cours de démarrage.</span><span class="sxs-lookup"><span data-stu-id="f12bf-143">Each call passes a string in the `task` argument that identifies the task being started.</span></span>  
  
 [!code-vb[VbVbcnProcedures#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#2)]  
  
 <span data-ttu-id="f12bf-144">L’exemple suivant montre un appel typique à `tellOperator`.</span><span class="sxs-lookup"><span data-stu-id="f12bf-144">The following example shows a typical call to `tellOperator`.</span></span>  
  
 [!code-vb[VbVbcnProcedures#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="f12bf-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f12bf-145">See also</span></span>

- [<span data-ttu-id="f12bf-146">Procédures</span><span class="sxs-lookup"><span data-stu-id="f12bf-146">Procedures</span></span>](./index.md)
- [<span data-ttu-id="f12bf-147">Procédures Function</span><span class="sxs-lookup"><span data-stu-id="f12bf-147">Function Procedures</span></span>](./function-procedures.md)
- [<span data-ttu-id="f12bf-148">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="f12bf-148">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="f12bf-149">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="f12bf-149">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="f12bf-150">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="f12bf-150">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="f12bf-151">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="f12bf-151">Sub Statement</span></span>](../../../../visual-basic/language-reference/statements/sub-statement.md)
- [<span data-ttu-id="f12bf-152">Guide pratique pour Appeler une procédure qui ne retourne pas de valeur</span><span class="sxs-lookup"><span data-stu-id="f12bf-152">How to: Call a Procedure that Does Not Return a Value</span></span>](./how-to-call-a-procedure-that-does-not-return-a-value.md)
- [<span data-ttu-id="f12bf-153">Guide pratique pour Appeler un gestionnaire d’événements en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f12bf-153">How to: Call an Event Handler in Visual Basic</span></span>](./how-to-call-an-event-handler.md)
