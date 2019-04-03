---
title: Byval (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ByVal
- ByVal
helpviewer_keywords:
- ByVal keyword [Visual Basic], contexts
- ByVal keyword [Visual Basic]
ms.assetid: 1eaf4e58-b305-4785-9e3d-e416b9c75598
ms.openlocfilehash: 5e534eac2300327d4c54c5ce93d8b2c6c538e794
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58832492"
---
# <a name="byval-visual-basic"></a><span data-ttu-id="2f0f9-102">Byval (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2f0f9-102">ByVal (Visual Basic)</span></span>
<span data-ttu-id="2f0f9-103">Spécifie qu’un argument est passé de sorte que la procédure ou propriété appelée ne peut pas modifier la valeur d’une variable sous-jacente à l’argument dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="2f0f9-103">Specifies that an argument is passed in such a way that the called procedure or property cannot change the value of a variable underlying the argument in the calling code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2f0f9-104">Notes</span><span class="sxs-lookup"><span data-stu-id="2f0f9-104">Remarks</span></span>  
 <span data-ttu-id="2f0f9-105">Le modificateur `ByVal` peut être utilisé dans les contextes suivants :</span><span class="sxs-lookup"><span data-stu-id="2f0f9-105">The `ByVal` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="2f0f9-106">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="2f0f9-106">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 [<span data-ttu-id="2f0f9-107">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="2f0f9-107">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [<span data-ttu-id="2f0f9-108">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="2f0f9-108">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 [<span data-ttu-id="2f0f9-109">Property (instruction)</span><span class="sxs-lookup"><span data-stu-id="2f0f9-109">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [<span data-ttu-id="2f0f9-110">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="2f0f9-110">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="example"></a><span data-ttu-id="2f0f9-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="2f0f9-111">Example</span></span>  
 <span data-ttu-id="2f0f9-112">L’exemple suivant illustre l’utilisation de la `ByVal` mécanisme avec un argument de type de référence de passage de paramètres.</span><span class="sxs-lookup"><span data-stu-id="2f0f9-112">The following example demonstrates the use of the `ByVal` parameter passing mechanism with a reference type argument.</span></span> <span data-ttu-id="2f0f9-113">Dans l’exemple, l’argument est `c1`, une instance de classe `Class1`.</span><span class="sxs-lookup"><span data-stu-id="2f0f9-113">In the example, the argument is `c1`, an instance of class `Class1`.</span></span> <span data-ttu-id="2f0f9-114">`ByVal` empêche le code dans les procédures de modification de la valeur sous-jacente de l’argument de référence, `c1`, mais ne protège ne pas les champs accessibles et les propriétés de `c1`.</span><span class="sxs-lookup"><span data-stu-id="2f0f9-114">`ByVal` prevents the code in the procedures from changing the underlying value of the reference argument, `c1`, but does not protect the accessible fields and properties of `c1`.</span></span>  
  
 [!code-vb[VbVbalrKeywords#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class5.vb#10)]  
  
## <a name="see-also"></a><span data-ttu-id="2f0f9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f0f9-115">See also</span></span>

- [<span data-ttu-id="2f0f9-116">Mots clés</span><span class="sxs-lookup"><span data-stu-id="2f0f9-116">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
- [<span data-ttu-id="2f0f9-117">Passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="2f0f9-117">Passing Arguments by Value and by Reference</span></span>](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
