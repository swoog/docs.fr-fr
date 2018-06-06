---
title: Procédures d'opérateur (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], operator
- Visual Basic code, operators
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- overloaded operators [Visual Basic]
- operator overloading
- operator procedures
ms.assetid: 8c513d38-246b-4fb7-8b75-29e1364e555b
ms.openlocfilehash: 5b4641ce8509e3111a11ed803d36194d5a301bce
ms.sourcegitcommit: fc70fcb9c789b6a4aefcdace46f3643fd076450f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34805709"
---
# <a name="operator-procedures-visual-basic"></a><span data-ttu-id="53675-102">Procédures d'opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="53675-102">Operator Procedures (Visual Basic)</span></span>
<span data-ttu-id="53675-103">Une procédure d’opérateur est une série d’instructions Visual Basic qui définissent le comportement d’un opérateur standard (tel que `*`, `<>`, ou `And`) sur une classe ou une structure que vous avez définie.</span><span class="sxs-lookup"><span data-stu-id="53675-103">An operator procedure is a series of Visual Basic statements that define the behavior of a standard operator (such as `*`, `<>`, or `And`) on a class or structure you have defined.</span></span> <span data-ttu-id="53675-104">Également appelé *surcharge d’opérateur*.</span><span class="sxs-lookup"><span data-stu-id="53675-104">This is also called *operator overloading*.</span></span>  
  
## <a name="when-to-define-operator-procedures"></a><span data-ttu-id="53675-105">Quand définir des procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="53675-105">When to Define Operator Procedures</span></span>  
 <span data-ttu-id="53675-106">Lorsque vous avez défini une classe ou structure, vous pouvez déclarer des variables comme étant du type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="53675-106">When you have defined a class or structure, you can declare variables to be of the type of that class or structure.</span></span> <span data-ttu-id="53675-107">Cette variable doit parfois participer à une opération dans le cadre d’une expression.</span><span class="sxs-lookup"><span data-stu-id="53675-107">Sometimes such a variable needs to participate in an operation as part of an expression.</span></span> <span data-ttu-id="53675-108">Pour ce faire, il doit être un opérande d’un opérateur.</span><span class="sxs-lookup"><span data-stu-id="53675-108">To do this, it must be an operand of an operator.</span></span>  
  
 <span data-ttu-id="53675-109">Visual Basic définit les opérateurs uniquement sur ses types de données fondamentaux.</span><span class="sxs-lookup"><span data-stu-id="53675-109">Visual Basic defines operators only on its fundamental data types.</span></span> <span data-ttu-id="53675-110">Vous pouvez définir le comportement d’un opérateur lorsqu’une ou les deux opérandes sont du type de votre classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="53675-110">You can define the behavior of an operator when one or both of the operands are of the type of your class or structure.</span></span>  
  
 <span data-ttu-id="53675-111">Pour plus d’informations, consultez [Operator, instruction](../../../../visual-basic/language-reference/statements/operator-statement.md).</span><span class="sxs-lookup"><span data-stu-id="53675-111">For more information, see [Operator Statement](../../../../visual-basic/language-reference/statements/operator-statement.md).</span></span>  
  
## <a name="types-of-operator-procedure"></a><span data-ttu-id="53675-112">Types de procédure d’opérateur</span><span class="sxs-lookup"><span data-stu-id="53675-112">Types of Operator Procedure</span></span>  
 <span data-ttu-id="53675-113">Une procédure d’opérateur peut être un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="53675-113">An operator procedure can be one of the following types:</span></span>  
  
-   <span data-ttu-id="53675-114">Définition d’un opérateur unaire où l’argument est du type de votre classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="53675-114">A definition of a unary operator where the argument is of the type of your class or structure.</span></span>  
  
-   <span data-ttu-id="53675-115">Définition d’un opérateur binaire, où au moins un des arguments est du type de votre classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="53675-115">A definition of a binary operator where at least one of the arguments is of the type of your class or structure.</span></span>  
  
-   <span data-ttu-id="53675-116">Définition d’un opérateur de conversion où l’argument est du type de votre classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="53675-116">A definition of a conversion operator where the argument is of the type of your class or structure.</span></span>  
  
-   <span data-ttu-id="53675-117">Définition d’un opérateur de conversion qui retourne le type de votre classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="53675-117">A definition of a conversion operator that returns the type of your class or structure.</span></span>  
  
 <span data-ttu-id="53675-118">Les opérateurs de conversion sont toujours unaires, et vous utilisez toujours `CType` comme l’opérateur que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="53675-118">Conversion operators are always unary, and you always use `CType` as the operator you are defining.</span></span>  
  
## <a name="declaration-syntax"></a><span data-ttu-id="53675-119">Syntaxe de déclaration</span><span class="sxs-lookup"><span data-stu-id="53675-119">Declaration Syntax</span></span>  
 <span data-ttu-id="53675-120">La syntaxe de déclaration d’une procédure d’opérateur est la suivante :</span><span class="sxs-lookup"><span data-stu-id="53675-120">The syntax for declaring an operator procedure is as follows:</span></span>  
  
 <span data-ttu-id="53675-121">`Public Shared`   `[Widening | Narrowing]`   `Operator`  *symbole_opérateur* `(` *operand1*`[,`*operand2* `]) As` *type de données*</span><span class="sxs-lookup"><span data-stu-id="53675-121">`Public Shared`   `[Widening | Narrowing]`   `Operator`  *operatorsymbol*  `(` *operand1*  `[,`  *operand2* `]) As`  *datatype*</span></span>  
  
 `' Statements of the operator procedure.`  
  
 `End Operator`  
  
 <span data-ttu-id="53675-122">Vous utilisez la `Widening` ou `Narrowing` mot clé uniquement sur un opérateur de conversion de type.</span><span class="sxs-lookup"><span data-stu-id="53675-122">You use the `Widening` or `Narrowing` keyword only on a type conversion operator.</span></span> <span data-ttu-id="53675-123">Le symbole d’opérateur est toujours [CType, fonction](../../../../visual-basic/language-reference/functions/ctype-function.md) pour un opérateur de conversion de type.</span><span class="sxs-lookup"><span data-stu-id="53675-123">The operator symbol is always [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) for a type conversion operator.</span></span>  
  
 <span data-ttu-id="53675-124">Vous déclarez deux opérandes pour définir un opérateur binaire, et un seul opérande pour définir un opérateur unaire, y compris un opérateur de conversion de type.</span><span class="sxs-lookup"><span data-stu-id="53675-124">You declare two operands to define a binary operator, and you declare one operand to define a unary operator, including a type conversion operator.</span></span> <span data-ttu-id="53675-125">Tous les opérandes doivent être déclarés `ByVal`.</span><span class="sxs-lookup"><span data-stu-id="53675-125">All operands must be declared `ByVal`.</span></span>  
  
 <span data-ttu-id="53675-126">Vous déclarez chaque opérande de la même manière que vous déclarez des paramètres pour [procédures Sub](./sub-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="53675-126">You declare each operand the same way you declare parameters for [Sub Procedures](./sub-procedures.md).</span></span>  
  
### <a name="data-type"></a><span data-ttu-id="53675-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="53675-127">Data Type</span></span>  
 <span data-ttu-id="53675-128">Étant donné que vous définissez un opérateur sur une classe ou une structure que vous avez définie, au moins un des opérandes doit être du type de données de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="53675-128">Because you are defining an operator on a class or structure you have defined, at least one of the operands must be of the data type of that class or structure.</span></span> <span data-ttu-id="53675-129">Pour un opérateur de conversion de type, l’opérande ou le type de retour doit être du type de données de la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="53675-129">For a type conversion operator, either the operand or the return type must be of the data type of the class or structure.</span></span>  
  
 <span data-ttu-id="53675-130">Pour plus d’informations, consultez [Operator, instruction](../../../../visual-basic/language-reference/statements/operator-statement.md).</span><span class="sxs-lookup"><span data-stu-id="53675-130">For more details, see [Operator Statement](../../../../visual-basic/language-reference/statements/operator-statement.md).</span></span>  
  
## <a name="calling-syntax"></a><span data-ttu-id="53675-131">Syntaxe d’appel</span><span class="sxs-lookup"><span data-stu-id="53675-131">Calling Syntax</span></span>  
 <span data-ttu-id="53675-132">Vous appelez une procédure d’opérateur implicitement en utilisant le symbole d’opérateur dans une expression.</span><span class="sxs-lookup"><span data-stu-id="53675-132">You invoke an operator procedure implicitly by using the operator symbol in an expression.</span></span> <span data-ttu-id="53675-133">Vous fournissez les opérandes de la même façon que pour les opérateurs prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="53675-133">You supply the operands the same way you do for predefined operators.</span></span>  
  
 <span data-ttu-id="53675-134">La syntaxe d’un appel implicite à une procédure d’opérateur est la suivante :</span><span class="sxs-lookup"><span data-stu-id="53675-134">The syntax for an implicit call to an operator procedure is as follows:</span></span>  
  
 <span data-ttu-id="53675-135">`Dim testStruct As`  *nom_structure*</span><span class="sxs-lookup"><span data-stu-id="53675-135">`Dim testStruct As`  *structurename*</span></span>  
  
 <span data-ttu-id="53675-136">`Dim testNewStruct As`  *nom_structure*`= testStruct`*symbole_opérateur*  `10`</span><span class="sxs-lookup"><span data-stu-id="53675-136">`Dim testNewStruct As`  *structurename*  `= testStruct`  *operatorsymbol*  `10`</span></span>  
  
### <a name="illustration-of-declaration-and-call"></a><span data-ttu-id="53675-137">Illustration de déclaration et d’appel</span><span class="sxs-lookup"><span data-stu-id="53675-137">Illustration of Declaration and Call</span></span>  
 <span data-ttu-id="53675-138">La structure suivante stocke une valeur entière 128 bits signée comme parties constitutives de poids fort et de poids faible.</span><span class="sxs-lookup"><span data-stu-id="53675-138">The following structure stores a signed 128-bit integer value as the constituent high-order and low-order parts.</span></span> <span data-ttu-id="53675-139">Il définit les `+` opérateur pour ajouter deux `veryLong` les valeurs et générer résultant `veryLong` valeur.</span><span class="sxs-lookup"><span data-stu-id="53675-139">It defines the `+` operator to add two `veryLong` values and generate a resulting `veryLong` value.</span></span>  
  
 [!code-vb[VbVbcnProcedures#23](./codesnippet/VisualBasic/operator-procedures_1.vb)]  
  
 <span data-ttu-id="53675-140">L’exemple suivant montre un appel classique à la `+` opérateur défini sur `veryLong`.</span><span class="sxs-lookup"><span data-stu-id="53675-140">The following example shows a typical call to the `+` operator defined on `veryLong`.</span></span>  
  
 [!code-vb[VbVbcnProcedures#24](./codesnippet/VisualBasic/operator-procedures_2.vb)]  
  
 <span data-ttu-id="53675-141">Pour obtenir plus d’informations et des exemples, consultez [Surcharge d’opérateur dans Visual Basic 2005](https://msdn.microsoft.com/library/ms379613(v=vs.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="53675-141">For more information and examples, see [Operator Overloading in Visual Basic 2005](https://msdn.microsoft.com/library/ms379613(v=vs.80).aspx).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53675-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53675-142">See Also</span></span>  
 [<span data-ttu-id="53675-143">Procédures</span><span class="sxs-lookup"><span data-stu-id="53675-143">Procedures</span></span>](./index.md)  
 [<span data-ttu-id="53675-144">Procédures Sub</span><span class="sxs-lookup"><span data-stu-id="53675-144">Sub Procedures</span></span>](./sub-procedures.md)  
 [<span data-ttu-id="53675-145">Procédures Function</span><span class="sxs-lookup"><span data-stu-id="53675-145">Function Procedures</span></span>](./function-procedures.md)  
 [<span data-ttu-id="53675-146">Procédures de propriété</span><span class="sxs-lookup"><span data-stu-id="53675-146">Property Procedures</span></span>](./property-procedures.md)  
 [<span data-ttu-id="53675-147">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="53675-147">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)  
 [<span data-ttu-id="53675-148">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="53675-148">Operator Statement</span></span>](../../../../visual-basic/language-reference/statements/operator-statement.md)  
 [<span data-ttu-id="53675-149">Guide pratique : définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="53675-149">How to: Define an Operator</span></span>](./how-to-define-an-operator.md)  
 [<span data-ttu-id="53675-150">Guide pratique : définir un opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="53675-150">How to: Define a Conversion Operator</span></span>](./how-to-define-a-conversion-operator.md)  
 [<span data-ttu-id="53675-151">Guide pratique : appeler une procédure d’opérateur</span><span class="sxs-lookup"><span data-stu-id="53675-151">How to: Call an Operator Procedure</span></span>](./how-to-call-an-operator-procedure.md)  
 [<span data-ttu-id="53675-152">Guide pratique : utiliser une classe qui définit des opérateurs</span><span class="sxs-lookup"><span data-stu-id="53675-152">How to: Use a Class that Defines Operators</span></span>](./how-to-use-a-class-that-defines-operators.md)
