---
title: Opérateur AddressOf (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- AddressOf
- vb.AddressOf
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- addresses, passing to API procedures
ms.assetid: 8105a59d-60d8-4ab5-b221-5899cdfacbf4
ms.openlocfilehash: 4f4f88551b6708ac3d0ee0f0f5bdcbdec1dfaaa9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721065"
---
# <a name="addressof-operator-visual-basic"></a><span data-ttu-id="592d7-102">Opérateur AddressOf (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="592d7-102">AddressOf Operator (Visual Basic)</span></span>
<span data-ttu-id="592d7-103">Crée une instance de délégué de procédure qui fait référence à la procédure spécifique.</span><span class="sxs-lookup"><span data-stu-id="592d7-103">Creates a procedure delegate instance that references the specific procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="592d7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="592d7-104">Syntax</span></span>  
  
```  
AddressOf procedurename  
```  
  
## <a name="parts"></a><span data-ttu-id="592d7-105">Composants</span><span class="sxs-lookup"><span data-stu-id="592d7-105">Parts</span></span>  
 `procedurename`  
 <span data-ttu-id="592d7-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="592d7-106">Required.</span></span> <span data-ttu-id="592d7-107">Indique la procédure à référencer par le délégué de procédure nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="592d7-107">Specifies the procedure to be referenced by the newly created procedure delegate.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="592d7-108">Notes</span><span class="sxs-lookup"><span data-stu-id="592d7-108">Remarks</span></span>  
 <span data-ttu-id="592d7-109">Le `AddressOf` opérateur crée un délégué de fonction qui pointe vers la fonction spécifiée par `procedurename`.</span><span class="sxs-lookup"><span data-stu-id="592d7-109">The `AddressOf` operator creates a function delegate that points to the function specified by `procedurename`.</span></span> <span data-ttu-id="592d7-110">Lorsque la procédure spécifiée est qu'une méthode d’instance puis le délégué de fonction fait référence à l’instance et la méthode.</span><span class="sxs-lookup"><span data-stu-id="592d7-110">When the specified procedure is an instance method then the function delegate refers to both the instance and the method.</span></span> <span data-ttu-id="592d7-111">Ensuite, lorsque le délégué de fonction est appelé la méthode spécifiée de l’instance spécifiée est appelée.</span><span class="sxs-lookup"><span data-stu-id="592d7-111">Then, when the function delegate is invoked the specified method of the specified instance is called.</span></span>  
  
 <span data-ttu-id="592d7-112">Le `AddressOf` opérateur peut être utilisé comme opérande d’un constructeur délégué ou il peut être utilisé dans un contexte dans lequel le type du délégué peut être déterminé par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="592d7-112">The `AddressOf` operator can be used as the operand of a delegate constructor or it can be used in a context in which the type of the delegate can be determined by the compiler.</span></span>  
  
## <a name="example"></a><span data-ttu-id="592d7-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="592d7-113">Example</span></span>  
 <span data-ttu-id="592d7-114">Cet exemple utilise le `AddressOf` opérateur pour désigner un délégué pour gérer le `Click` événements d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="592d7-114">This example uses the `AddressOf` operator to designate a delegate to handle the `Click` event of a button.</span></span>  
  
 [!code-vb[VbVbalrDelegates#8](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/addressof-operator_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="592d7-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="592d7-115">Example</span></span>  
 <span data-ttu-id="592d7-116">L’exemple suivant utilise le `AddressOf` opérateur pour désigner la fonction de démarrage d’un thread.</span><span class="sxs-lookup"><span data-stu-id="592d7-116">The following example uses the `AddressOf` operator to designate the startup function for a thread.</span></span>  
  
 [!code-vb[VbVbalrDelegates#9](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/addressof-operator_2.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="592d7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="592d7-117">See also</span></span>
- [<span data-ttu-id="592d7-118">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="592d7-118">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)
- [<span data-ttu-id="592d7-119">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="592d7-119">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
- [<span data-ttu-id="592d7-120">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="592d7-120">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)
- [<span data-ttu-id="592d7-121">Délégués</span><span class="sxs-lookup"><span data-stu-id="592d7-121">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
