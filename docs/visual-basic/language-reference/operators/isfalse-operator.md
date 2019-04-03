---
title: Opérateur IsFalse (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.isfalse
helpviewer_keywords:
- AndAlso operator [Visual Basic]
- IsFalse operator [Visual Basic]
ms.assetid: 37fc9dbf-e5cc-4570-b93f-7213447974df
ms.openlocfilehash: 9f25c406038486224c2c4708c86ef86889c44c15
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58818486"
---
# <a name="isfalse-operator-visual-basic"></a><span data-ttu-id="fde59-102">Opérateur IsFalse (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fde59-102">IsFalse Operator (Visual Basic)</span></span>
<span data-ttu-id="fde59-103">Détermine si une expression est `False`.</span><span class="sxs-lookup"><span data-stu-id="fde59-103">Determines whether an expression is `False`.</span></span>  
  
 <span data-ttu-id="fde59-104">Vous ne pouvez pas appeler `IsFalse` explicitement dans votre code, mais le Visual Basic compilateur peut l’utiliser pour générer le code à partir de `AndAlso` clauses.</span><span class="sxs-lookup"><span data-stu-id="fde59-104">You cannot call `IsFalse` explicitly in your code, but the Visual Basic compiler can use it to generate code from `AndAlso` clauses.</span></span> <span data-ttu-id="fde59-105">Si vous définissez une classe ou une structure et ensuite utiliser une variable de ce type dans un `AndAlso` clause, vous devez définir `IsFalse` sur cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="fde59-105">If you define a class or structure and then use a variable of that type in an `AndAlso` clause, you must define `IsFalse` on that class or structure.</span></span>  
  
 <span data-ttu-id="fde59-106">Le compilateur considère les `IsFalse` et `IsTrue` opérateurs comme un *mis en correspondance de paire*.</span><span class="sxs-lookup"><span data-stu-id="fde59-106">The compiler considers the `IsFalse` and `IsTrue` operators as a *matched pair*.</span></span> <span data-ttu-id="fde59-107">Cela signifie que si vous définissez un d’eux, vous devez également définir le.</span><span class="sxs-lookup"><span data-stu-id="fde59-107">This means that if you define one of them, you must also define the other one.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fde59-108">Le `IsFalse` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsque son opérande a le type de cette classe ou structure.</span><span class="sxs-lookup"><span data-stu-id="fde59-108">The `IsFalse` operator can be *overloaded*, which means that a class or structure can redefine its behavior when its operand has the type of that class or structure.</span></span> <span data-ttu-id="fde59-109">Si votre code utilise cet opérateur sur une telle classe ou structure, veillez à ce que vous comprenez son comportement redéfini.</span><span class="sxs-lookup"><span data-stu-id="fde59-109">If your code uses this operator on such a class or structure, be sure you understand its redefined behavior.</span></span> <span data-ttu-id="fde59-110">Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span><span class="sxs-lookup"><span data-stu-id="fde59-110">For more information, see [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="fde59-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="fde59-111">Example</span></span>  
 <span data-ttu-id="fde59-112">L’exemple de code suivant définit le contour d’une structure qui contient les définitions pour le `IsFalse` et `IsTrue` opérateurs.</span><span class="sxs-lookup"><span data-stu-id="fde59-112">The following code example defines the outline of a structure that includes definitions for the `IsFalse` and `IsTrue` operators.</span></span>  
  
 [!code-vb[VbVbalrOperators#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#28)]  
  
## <a name="see-also"></a><span data-ttu-id="fde59-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fde59-113">See also</span></span>

- [<span data-ttu-id="fde59-114">IsTrue (opérateur)</span><span class="sxs-lookup"><span data-stu-id="fde59-114">IsTrue Operator</span></span>](../../../visual-basic/language-reference/operators/istrue-operator.md)
- [<span data-ttu-id="fde59-115">Guide pratique pour Définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="fde59-115">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [<span data-ttu-id="fde59-116">AndAlso (opérateur)</span><span class="sxs-lookup"><span data-stu-id="fde59-116">AndAlso Operator</span></span>](../../../visual-basic/language-reference/operators/andalso-operator.md)
