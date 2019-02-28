---
title: 'Procédure : Définir un opérateur de Conversion (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
ms.openlocfilehash: fe5c314fe4e39c8a06803037da29b51148188e14
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56974638"
---
# <a name="how-to-define-a-conversion-operator-visual-basic"></a><span data-ttu-id="16fea-102">Procédure : Définir un opérateur de Conversion (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="16fea-102">How to: Define a Conversion Operator (Visual Basic)</span></span>
<span data-ttu-id="16fea-103">Si vous avez défini une classe ou structure, vous pouvez définir un opérateur de conversion de type entre le type de votre classe ou une structure et un autre type de données (tel que `Integer`, `Double`, ou `String`).</span><span class="sxs-lookup"><span data-stu-id="16fea-103">If you have defined a class or structure, you can define a type conversion operator between the type of your class or structure and another data type (such as `Integer`, `Double`, or `String`).</span></span>  
  
 <span data-ttu-id="16fea-104">Définir la conversion de type comme un [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) procédure au sein de la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="16fea-104">Define the type conversion as a [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) procedure within the class or structure.</span></span> <span data-ttu-id="16fea-105">Toutes les procédures de conversion doivent être `Public Shared`, et chacune d’elles doit spécifier [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) ou [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md).</span><span class="sxs-lookup"><span data-stu-id="16fea-105">All conversion procedures must be `Public Shared`, and each one must specify either [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) or [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md).</span></span>  
  
 <span data-ttu-id="16fea-106">Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="16fea-106">Defining an operator on a class or structure is also called *overloading* the operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="16fea-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="16fea-107">Example</span></span>  
 <span data-ttu-id="16fea-108">L’exemple suivant définit les opérateurs de conversion entre une structure appelée `digit` et un `Byte`.</span><span class="sxs-lookup"><span data-stu-id="16fea-108">The following example defines conversion operators between a structure called `digit` and a `Byte`.</span></span>  
  
 [!code-vb[VbVbcnProcedures#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#27)]  
  
 <span data-ttu-id="16fea-109">Vous pouvez tester la structure `digit` par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="16fea-109">You can test the structure `digit` with the following code.</span></span>  
  
 [!code-vb[VbVbcnProcedures#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#28)]  
  
## <a name="see-also"></a><span data-ttu-id="16fea-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16fea-110">See also</span></span>
- [<span data-ttu-id="16fea-111">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="16fea-111">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="16fea-112">Guide pratique pour Définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="16fea-112">How to: Define an Operator</span></span>](./how-to-define-an-operator.md)
- [<span data-ttu-id="16fea-113">Guide pratique pour Appeler une procédure d’opérateur</span><span class="sxs-lookup"><span data-stu-id="16fea-113">How to: Call an Operator Procedure</span></span>](./how-to-call-an-operator-procedure.md)
- [<span data-ttu-id="16fea-114">Guide pratique pour Utiliser une classe qui définit des opérateurs</span><span class="sxs-lookup"><span data-stu-id="16fea-114">How to: Use a Class that Defines Operators</span></span>](./how-to-use-a-class-that-defines-operators.md)
- [<span data-ttu-id="16fea-115">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="16fea-115">Operator Statement</span></span>](../../../../visual-basic/language-reference/statements/operator-statement.md)
- [<span data-ttu-id="16fea-116">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="16fea-116">Structure Statement</span></span>](../../../../visual-basic/language-reference/statements/structure-statement.md)
- [<span data-ttu-id="16fea-117">Guide pratique pour déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="16fea-117">How to: Declare a Structure</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="16fea-118">Conversions implicites et explicites</span><span class="sxs-lookup"><span data-stu-id="16fea-118">Implicit and Explicit Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [<span data-ttu-id="16fea-119">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="16fea-119">Widening and Narrowing Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
