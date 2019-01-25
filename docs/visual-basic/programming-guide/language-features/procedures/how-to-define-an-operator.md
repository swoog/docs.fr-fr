---
title: 'Procédure : Définir un opérateur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- Visual Basic code, operators
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- operator procedures [Visual Basic], about operator procedures
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: d4b0e253-092a-4e6e-9fe2-01f562140a29
ms.openlocfilehash: fb150298562c1ec91f73f3c8075f4f8a4fc20b27
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54679524"
---
# <a name="how-to-define-an-operator-visual-basic"></a><span data-ttu-id="7cbf4-102">Procédure : Définir un opérateur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7cbf4-102">How to: Define an Operator (Visual Basic)</span></span>
<span data-ttu-id="7cbf4-103">Si vous avez défini une classe ou structure, vous pouvez définir le comportement d’un opérateur standard (tel que `*`, `<>`, ou `And`) lorsqu’au moins des opérandes est du type de votre classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-103">If you have defined a class or structure, you can define the behavior of a standard operator (such as `*`, `<>`, or `And`) when one or both of the operands is of the type of your class or structure.</span></span>  
  
 <span data-ttu-id="7cbf4-104">Définissez l’opérateur standard comme une procédure d’opérateur dans la classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-104">Define the standard operator as an operator procedure within the class or structure.</span></span> <span data-ttu-id="7cbf4-105">Toutes les procédures d’opérateur doivent être `Public` `Shared`.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-105">All operator procedures must be `Public` `Shared`.</span></span>  
  
 <span data-ttu-id="7cbf4-106">Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-106">Defining an operator on a class or structure is also called *overloading* the operator.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7cbf4-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="7cbf4-107">Example</span></span>  
 <span data-ttu-id="7cbf4-108">L’exemple suivant définit la `+` opérateur pour une structure appelée `height`.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-108">The following example defines the `+` operator for a structure called `height`.</span></span> <span data-ttu-id="7cbf4-109">La structure utilise des hauteurs mesurées en mètres et de centimètres.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-109">The structure uses heights measured in feet and inches.</span></span> <span data-ttu-id="7cbf4-110">Un *pouce* est 2,54 centimètres et l’autre *foot* est de 12 pouces.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-110">One *inch* is 2.54 centimeters, and one *foot* is 12 inches.</span></span> <span data-ttu-id="7cbf4-111">Pour garantir des valeurs normalisées (pouces < 12.0), le constructeur effectue *modulo* 12 arithmétique.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-111">To ensure normalized values (inches < 12.0), the constructor performs *modulo* 12 arithmetic.</span></span> <span data-ttu-id="7cbf4-112">Le `+` opérateur utilise le constructeur pour générer des valeurs normalisées.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-112">The `+` operator uses the constructor to generate normalized values.</span></span>  
  
 [!code-vb[VbVbcnProcedures#25](./codesnippet/VisualBasic/how-to-define-an-operator_1.vb)]  
  
 <span data-ttu-id="7cbf4-113">Vous pouvez tester la structure `height` par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="7cbf4-113">You can test the structure `height` with the following code.</span></span>  
  
 [!code-vb[VbVbcnProcedures#26](./codesnippet/VisualBasic/how-to-define-an-operator_2.vb)]  
  
 <span data-ttu-id="7cbf4-114">Pour obtenir plus d’informations et des exemples, consultez [Surcharge d’opérateur dans Visual Basic 2005](https://msdn.microsoft.com/library/ms379613(v=vs.80).aspx).</span><span class="sxs-lookup"><span data-stu-id="7cbf4-114">For more information and examples, see [Operator Overloading in Visual Basic 2005](https://msdn.microsoft.com/library/ms379613(v=vs.80).aspx).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7cbf4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cbf4-115">See also</span></span>
- [<span data-ttu-id="7cbf4-116">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="7cbf4-116">Operator Procedures</span></span>](./operator-procedures.md)
- [<span data-ttu-id="7cbf4-117">Guide pratique pour Définir un opérateur de Conversion</span><span class="sxs-lookup"><span data-stu-id="7cbf4-117">How to: Define a Conversion Operator</span></span>](./how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="7cbf4-118">Guide pratique pour Appeler une procédure d’opérateur</span><span class="sxs-lookup"><span data-stu-id="7cbf4-118">How to: Call an Operator Procedure</span></span>](./how-to-call-an-operator-procedure.md)
- [<span data-ttu-id="7cbf4-119">Guide pratique pour Utiliser une classe qui définit des opérateurs</span><span class="sxs-lookup"><span data-stu-id="7cbf4-119">How to: Use a Class that Defines Operators</span></span>](./how-to-use-a-class-that-defines-operators.md)
- [<span data-ttu-id="7cbf4-120">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="7cbf4-120">Operator Statement</span></span>](../../../../visual-basic/language-reference/statements/operator-statement.md)
- [<span data-ttu-id="7cbf4-121">Structure (instruction)</span><span class="sxs-lookup"><span data-stu-id="7cbf4-121">Structure Statement</span></span>](../../../../visual-basic/language-reference/statements/structure-statement.md)
- [<span data-ttu-id="7cbf4-122">Guide pratique pour déclarer une structure</span><span class="sxs-lookup"><span data-stu-id="7cbf4-122">How to: Declare a Structure</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [<span data-ttu-id="7cbf4-123">Mod (opérateur)</span><span class="sxs-lookup"><span data-stu-id="7cbf4-123">Mod Operator</span></span>](../../../../visual-basic/language-reference/operators/mod-operator.md)
