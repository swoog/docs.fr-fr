---
title: 'Procédure : Passer des procédures à une autre procédure en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- delegates [Visual Basic], passing procedures
ms.assetid: 5adbba15-5a1d-413f-ab3e-3ff6cc0a4669
ms.openlocfilehash: 312c0e0f100e85256ad4ca856ccf7f35dbaa36dc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61973279"
---
# <a name="how-to-pass-procedures-to-another-procedure-in-visual-basic"></a><span data-ttu-id="dfad0-102">Procédure : Passer des procédures à une autre procédure en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dfad0-102">How to: Pass Procedures to Another Procedure in Visual Basic</span></span>
<span data-ttu-id="dfad0-103">Cet exemple montre comment utiliser des délégués pour passer d’une procédure à une autre procédure.</span><span class="sxs-lookup"><span data-stu-id="dfad0-103">This example shows how to use delegates to pass a procedure to another procedure.</span></span>  
  
 <span data-ttu-id="dfad0-104">Un délégué est un type que vous pouvez utiliser comme tout autre type dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dfad0-104">A delegate is a type that you can use like any other type in Visual Basic.</span></span> <span data-ttu-id="dfad0-105">Le `AddressOf` opérateur retourne un objet délégué lorsqu’il est appliqué à un nom de procédure.</span><span class="sxs-lookup"><span data-stu-id="dfad0-105">The `AddressOf` operator returns a delegate object when applied to a procedure name.</span></span>  
  
 <span data-ttu-id="dfad0-106">Cet exemple comporte une procédure avec un paramètre de délégué qui peut prendre une référence à une autre procédure, obtenue avec la `AddressOf` opérateur.</span><span class="sxs-lookup"><span data-stu-id="dfad0-106">This example has a procedure with a delegate parameter that can take a reference to another procedure, obtained with the `AddressOf` operator.</span></span>  
  
### <a name="create-the-delegate-and-matching-procedures"></a><span data-ttu-id="dfad0-107">Créer le délégué et les procédures correspondantes</span><span class="sxs-lookup"><span data-stu-id="dfad0-107">Create the delegate and matching procedures</span></span>  
  
1. <span data-ttu-id="dfad0-108">Créez un délégué nommé `MathOperator`.</span><span class="sxs-lookup"><span data-stu-id="dfad0-108">Create a delegate named `MathOperator`.</span></span>  
  
     [!code-vb[VbVbalrDelegates#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#1)]  
  
2. <span data-ttu-id="dfad0-109">Créez une procédure nommée `AddNumbers` avec des paramètres et la valeur de retour qui correspondent à celles de `MathOperator`, de sorte que les signatures correspondent.</span><span class="sxs-lookup"><span data-stu-id="dfad0-109">Create a procedure named `AddNumbers` with parameters and return value that match those of `MathOperator`, so that the signatures match.</span></span>  
  
     [!code-vb[VbVbalrDelegates#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#2)]  
  
3. <span data-ttu-id="dfad0-110">Créez une procédure nommée `SubtractNumbers` avec une signature qui correspond à `MathOperator`.</span><span class="sxs-lookup"><span data-stu-id="dfad0-110">Create a procedure named `SubtractNumbers` with a signature that matches `MathOperator`.</span></span>  
  
     [!code-vb[VbVbalrDelegates#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#3)]  
  
4. <span data-ttu-id="dfad0-111">Créez une procédure nommée `DelegateTest` qui prend un délégué en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="dfad0-111">Create a procedure named `DelegateTest` that takes a delegate as a parameter.</span></span>  
  
     <span data-ttu-id="dfad0-112">Cette procédure peut accepter une référence à `AddNumbers` ou `SubtractNumbers`, car leurs signatures correspondent à la `MathOperator` signature.</span><span class="sxs-lookup"><span data-stu-id="dfad0-112">This procedure can accept a reference to `AddNumbers` or `SubtractNumbers`, because their signatures match the `MathOperator` signature.</span></span>  
  
     [!code-vb[VbVbalrDelegates#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#4)]  
  
5. <span data-ttu-id="dfad0-113">Créez une procédure nommée `Test` qui appelle `DelegateTest` une autre fois avec le délégué pour `AddNumbers` en tant que paramètre, puis à nouveau avec le délégué pour `SubtractNumbers` en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="dfad0-113">Create a procedure named `Test` that calls `DelegateTest` once with the delegate for `AddNumbers` as a parameter, and again with the delegate for `SubtractNumbers` as a parameter.</span></span>  
  
     [!code-vb[VbVbalrDelegates#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#5)]  
  
     <span data-ttu-id="dfad0-114">Lorsque `Test` est appelée, elle affiche d’abord le résultat de `AddNumbers` agissant sur `5` et `3`, qui est 8.</span><span class="sxs-lookup"><span data-stu-id="dfad0-114">When `Test` is called, it first displays the result of `AddNumbers` acting on `5` and `3`, which is 8.</span></span> <span data-ttu-id="dfad0-115">Puis le résultat de `SubtractNumbers` agissant sur `9` et `3` s’affiche, qui est 6.</span><span class="sxs-lookup"><span data-stu-id="dfad0-115">Then the result of `SubtractNumbers` acting on `9` and `3` is displayed, which is 6.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfad0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfad0-116">See also</span></span>

- [<span data-ttu-id="dfad0-117">Délégués</span><span class="sxs-lookup"><span data-stu-id="dfad0-117">Delegates</span></span>](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [<span data-ttu-id="dfad0-118">AddressOf (opérateur)</span><span class="sxs-lookup"><span data-stu-id="dfad0-118">AddressOf Operator</span></span>](../../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="dfad0-119">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="dfad0-119">Delegate Statement</span></span>](../../../../visual-basic/language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="dfad0-120">Guide pratique pour Appeler une méthode déléguée</span><span class="sxs-lookup"><span data-stu-id="dfad0-120">How to: Invoke a Delegate Method</span></span>](../../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)
