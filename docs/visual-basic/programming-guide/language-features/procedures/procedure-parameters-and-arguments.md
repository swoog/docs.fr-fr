---
title: Paramètres et arguments d’une procédure (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], argument lists
- values [Visual Basic], passing to procedures
- arguments [Visual Basic], passing
- procedures [Visual Basic], parameters
- Visual Basic code, argument lists
- Visual Basic code, procedures
- parameters [Visual Basic], Visual Basic procedures
- parameters [Visual Basic], lists
- arguments [Visual Basic], Visual Basic procedures
- arguments [Visual Basic], procedures
- parameter lists [Visual Basic]
- Visual Basic code, parameter lists
- argument lists [Visual Basic]
- procedures [Visual Basic], parameter lists
ms.assetid: ff275aff-aa13-40df-bd4c-63486db8c1e9
ms.openlocfilehash: 42f85ed98f399c96f89879129b085f25ab117096
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54731736"
---
# <a name="procedure-parameters-and-arguments-visual-basic"></a><span data-ttu-id="ab2b5-102">Paramètres et arguments d’une procédure (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ab2b5-102">Procedure Parameters and Arguments (Visual Basic)</span></span>
<span data-ttu-id="ab2b5-103">Dans la plupart des cas, une procédure a besoin d’informations sur les circonstances dans lesquelles elle a été appelée.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-103">In most cases, a procedure needs some information about the circumstances in which it has been called.</span></span> <span data-ttu-id="ab2b5-104">Une procédure qui effectue les tâches répétitives ou partagées utilise des informations différentes pour chaque appel.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-104">A procedure that performs repeated or shared tasks uses different information for each call.</span></span> <span data-ttu-id="ab2b5-105">Ces informations se composent des variables, constantes et expressions que vous passez à la procédure lorsque vous l’appelez.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-105">This information consists of variables, constants, and expressions that you pass to the procedure when you call it.</span></span>  
  
 <span data-ttu-id="ab2b5-106">Un *paramètre* représente une valeur de la procédure suppose que vous fournissez lorsque vous l’appelez.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-106">A *parameter* represents a value that the procedure expects you to supply when you call it.</span></span> <span data-ttu-id="ab2b5-107">Déclaration de la procédure définit ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-107">The procedure's declaration defines its parameters.</span></span>  
  
 <span data-ttu-id="ab2b5-108">Vous pouvez définir une procédure sans paramètres, un seul paramètre, ou plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-108">You can define a procedure with no parameters, one parameter, or more than one.</span></span> <span data-ttu-id="ab2b5-109">La partie de la définition de procédure qui spécifie les paramètres est appelée le *liste de paramètres*.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-109">The part of the procedure definition that specifies the parameters is called the *parameter list*.</span></span>  
  
 <span data-ttu-id="ab2b5-110">Un *argument* représente la valeur que vous fournissez à un paramètre de procédure lorsque vous appelez la procédure.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-110">An *argument* represents the value you supply to a procedure parameter when you call the procedure.</span></span> <span data-ttu-id="ab2b5-111">Le code appelant fournit les arguments lorsqu’il appelle la procédure.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-111">The calling code supplies the arguments when it calls the procedure.</span></span> <span data-ttu-id="ab2b5-112">La partie de l’appel de procédure qui spécifie les arguments est appelée le *liste d’arguments*.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-112">The part of the procedure call that specifies the arguments is called the *argument list*.</span></span>  
  
 <span data-ttu-id="ab2b5-113">L’illustration suivante montre le code appelant la procédure `safeSquareRoot` à partir de deux emplacements différents.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-113">The following illustration shows code calling the procedure `safeSquareRoot` from two different places.</span></span> <span data-ttu-id="ab2b5-114">Le premier appel passe la valeur de la variable `x` (4.0) au paramètre `number`et la valeur de retour dans `root` (2.0) est affectée à la variable `y`.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-114">The first call passes the value of the variable `x` (4.0) to the parameter `number`, and the return value in `root` (2.0) is assigned to the variable `y`.</span></span> <span data-ttu-id="ab2b5-115">Le deuxième appel passe la valeur de littéral 9.0 à `number`et assigne la valeur de retournée (3.0) à la variable `z`.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-115">The second call passes the literal value 9.0 to `number`, and assigns the return value (3.0) to variable `z`.</span></span>  
  
 <span data-ttu-id="ab2b5-116">![Diagramme graphique du passage d’argument au paramètre](./media/parametersargue.gif "ParametersArgue")</span><span class="sxs-lookup"><span data-stu-id="ab2b5-116">![Graphic diagram of passing argument to parameter](./media/parametersargue.gif "ParametersArgue")</span></span>  
<span data-ttu-id="ab2b5-117">Passage d’un argument à un paramètre</span><span class="sxs-lookup"><span data-stu-id="ab2b5-117">Passing an argument to a parameter</span></span>  
  
 <span data-ttu-id="ab2b5-118">Pour plus d’informations, consultez [différences entre les paramètres et Arguments](./differences-between-parameters-and-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="ab2b5-118">For more information, see [Differences Between Parameters and Arguments](./differences-between-parameters-and-arguments.md).</span></span>  
  
## <a name="parameter-data-type"></a><span data-ttu-id="ab2b5-119">Type de données de paramètre</span><span class="sxs-lookup"><span data-stu-id="ab2b5-119">Parameter Data Type</span></span>  
 <span data-ttu-id="ab2b5-120">Vous définissez un type de données pour un paramètre à l’aide de la `As` clause dans sa déclaration.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-120">You define a data type for a parameter by using the `As` clause in its declaration.</span></span> <span data-ttu-id="ab2b5-121">Par exemple, la fonction suivante accepte une chaîne et un entier.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-121">For example, the following function accepts a string and an integer.</span></span>  
  
 [!code-vb[VbVbcnProcedures#32](./codesnippet/VisualBasic/procedure-parameters-and-arguments_1.vb)]  
  
 <span data-ttu-id="ab2b5-122">Si le commutateur de vérification de type ([Option Strict, instruction](../../../../visual-basic/language-reference/statements/option-strict-statement.md)) est `Off,` le `As` clause est facultative, sauf si un paramètre l’utilise, tous les paramètres doivent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-122">If the type checking switch ([Option Strict Statement](../../../../visual-basic/language-reference/statements/option-strict-statement.md)) is `Off,` the `As` clause is optional, except that if any one parameter uses it, all parameters must use it.</span></span> <span data-ttu-id="ab2b5-123">Si la vérification de type est `On`, le `As` clause est requise pour tous les paramètres de procédure.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-123">If type checking is `On`, the `As` clause is required for all procedure parameters.</span></span>  
  
 <span data-ttu-id="ab2b5-124">Si le code appelant est censé fournir un argument avec un type de données différent de celui de son paramètre correspondant, tel que `Byte` à un `String` paramètre, il doit effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab2b5-124">If the calling code expects to supply an argument with a data type different from that of its corresponding parameter, such as `Byte` to a `String` parameter, it must do one of the following:</span></span>  
  
-   <span data-ttu-id="ab2b5-125">Fournissez uniquement des arguments avec les types de données qui s’étendent vers le type de données de paramètre ;</span><span class="sxs-lookup"><span data-stu-id="ab2b5-125">Supply only arguments with data types that widen to the parameter data type;</span></span>  
  
-   <span data-ttu-id="ab2b5-126">Définissez `Option Strict Off` pour permettre les conversions restrictives implicites ; ou</span><span class="sxs-lookup"><span data-stu-id="ab2b5-126">Set `Option Strict Off` to allow implicit narrowing conversions; or</span></span>  
  
-   <span data-ttu-id="ab2b5-127">Utilisez un mot clé de conversion pour convertir explicitement le type de données.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-127">Use a conversion keyword to explicitly convert the data type.</span></span>  
  
### <a name="type-parameters"></a><span data-ttu-id="ab2b5-128">Paramètres de type</span><span class="sxs-lookup"><span data-stu-id="ab2b5-128">Type Parameters</span></span>  
 <span data-ttu-id="ab2b5-129">Un *procédure générique* définit également un ou plusieurs *paramètres de type* en plus de ses paramètres normaux.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-129">A *generic procedure* also defines one or more *type parameters* in addition to its normal parameters.</span></span> <span data-ttu-id="ab2b5-130">Une procédure générique permet au code appelant à passer différents types de données chaque fois qu’il appelle la procédure, il peut adapter les types de données sur les exigences de chaque appel.</span><span class="sxs-lookup"><span data-stu-id="ab2b5-130">A generic procedure allows the calling code to pass different data types each time it calls the procedure, so it can tailor the data types to the requirements of each individual call.</span></span> <span data-ttu-id="ab2b5-131">Consultez [Generic Procedures in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="ab2b5-131">See [Generic Procedures in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-procedures.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab2b5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab2b5-132">See also</span></span>
- [<span data-ttu-id="ab2b5-133">Procédures</span><span class="sxs-lookup"><span data-stu-id="ab2b5-133">Procedures</span></span>](./index.md)
- [<span data-ttu-id="ab2b5-134">Procédures Sub</span><span class="sxs-lookup"><span data-stu-id="ab2b5-134">Sub Procedures</span></span>](./sub-procedures.md)
- [<span data-ttu-id="ab2b5-135">Procédures Function</span><span class="sxs-lookup"><span data-stu-id="ab2b5-135">Function Procedures</span></span>](./function-procedures.md)
- [<span data-ttu-id="ab2b5-136">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="ab2b5-136">Property Procedures</span></span>](./property-procedures.md)
- [<span data-ttu-id="ab2b5-137">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="ab2b5-137">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="ab2b5-138">Guide pratique pour Définir un paramètre pour une procédure</span><span class="sxs-lookup"><span data-stu-id="ab2b5-138">How to: Define a Parameter for a Procedure</span></span>](./how-to-define-a-parameter-for-a-procedure.md)
- [<span data-ttu-id="ab2b5-139">Guide pratique pour Passer des Arguments à une procédure</span><span class="sxs-lookup"><span data-stu-id="ab2b5-139">How to: Pass Arguments to a Procedure</span></span>](./how-to-pass-arguments-to-a-procedure.md)
- [<span data-ttu-id="ab2b5-140">Passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="ab2b5-140">Passing Arguments by Value and by Reference</span></span>](./passing-arguments-by-value-and-by-reference.md)
- [<span data-ttu-id="ab2b5-141">Surcharge de procédure</span><span class="sxs-lookup"><span data-stu-id="ab2b5-141">Procedure Overloading</span></span>](./procedure-overloading.md)
- [<span data-ttu-id="ab2b5-142">Conversions de type en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ab2b5-142">Type Conversions in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
