---
title: 'Comment : définir un opérateur de conversion (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
ms.openlocfilehash: 24bbe41af67f757cae661a78d482a423ff0ffd85
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33648471"
---
# <a name="how-to-define-a-conversion-operator-visual-basic"></a><span data-ttu-id="101e7-102">Comment : définir un opérateur de conversion (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="101e7-102">How to: Define a Conversion Operator (Visual Basic)</span></span>
<span data-ttu-id="101e7-103">Si vous avez défini une classe ou structure, vous pouvez définir un opérateur de conversion de type entre le type de votre classe ou structure et un autre type de données (tel que `Integer`, `Double`, ou `String`).</span><span class="sxs-lookup"><span data-stu-id="101e7-103">If you have defined a class or structure, you can define a type conversion operator between the type of your class or structure and another data type (such as `Integer`, `Double`, or `String`).</span></span>  
  
 <span data-ttu-id="101e7-104">Définir la conversion de type comme un [CType, fonction](../../../../visual-basic/language-reference/functions/ctype-function.md) procédure au sein de la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="101e7-104">Define the type conversion as a [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) procedure within the class or structure.</span></span> <span data-ttu-id="101e7-105">Toutes les procédures de conversion doivent être `Public Shared`, et chacune d’elles doit spécifier [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) ou [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md).</span><span class="sxs-lookup"><span data-stu-id="101e7-105">All conversion procedures must be `Public Shared`, and each one must specify either [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) or [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md).</span></span>  
  
 <span data-ttu-id="101e7-106">Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="101e7-106">Defining an operator on a class or structure is also called *overloading* the operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="101e7-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="101e7-107">Example</span></span>  
 <span data-ttu-id="101e7-108">L’exemple suivant définit les opérateurs de conversion entre une structure appelée `digit` et un `Byte`.</span><span class="sxs-lookup"><span data-stu-id="101e7-108">The following example defines conversion operators between a structure called `digit` and a `Byte`.</span></span>  
  
 [!code-vb[VbVbcnProcedures#27](./codesnippet/VisualBasic/how-to-define-a-conversion-operator_1.vb)]  
  
 <span data-ttu-id="101e7-109">Vous pouvez tester la structure `digit` par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="101e7-109">You can test the structure `digit` with the following code.</span></span>  
  
 [!code-vb[VbVbcnProcedures#28](./codesnippet/VisualBasic/how-to-define-a-conversion-operator_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="101e7-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="101e7-110">See Also</span></span>  
 [<span data-ttu-id="101e7-111">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="101e7-111">Operator Procedures</span></span>](./operator-procedures.md)  
 [<span data-ttu-id="101e7-112">Guide pratique : définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="101e7-112">How to: Define an Operator</span></span>](./how-to-define-an-operator.md)  
 [<span data-ttu-id="101e7-113">Guide pratique : appeler une procédure d’opérateur</span><span class="sxs-lookup"><span data-stu-id="101e7-113">How to: Call an Operator Procedure</span></span>](./how-to-call-an-operator-procedure.md)  
 [<span data-ttu-id="101e7-114">Guide pratique : utiliser une classe qui définit des opérateurs</span><span class="sxs-lookup"><span data-stu-id="101e7-114">How to: Use a Class that Defines Operators</span></span>](./how-to-use-a-class-that-defines-operators.md)  
 [<span data-ttu-id="101e7-115">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="101e7-115">Operator Statement</span></span>](../../../../visual-basic/language-reference/statements/operator-statement.md)  
 [<span data-ttu-id="101e7-116">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="101e7-116">Structure Statement</span></span>](../../../../visual-basic/language-reference/statements/structure-statement.md)  
 [<span data-ttu-id="101e7-117">Guide pratique : déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="101e7-117">How to: Declare a Structure</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)  
 [<span data-ttu-id="101e7-118">Conversions implicites et explicites</span><span class="sxs-lookup"><span data-stu-id="101e7-118">Implicit and Explicit Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)  
 [<span data-ttu-id="101e7-119">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="101e7-119">Widening and Narrowing Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
