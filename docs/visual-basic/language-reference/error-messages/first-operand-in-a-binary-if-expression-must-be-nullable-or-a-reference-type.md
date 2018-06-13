---
title: Le premier opérande d’un fichier binaire &#39;si&#39; expression doit être nullable ou un type référence
ms.date: 07/20/2015
f1_keywords:
- bc33107
- vbc33107
helpviewer_keywords:
- BC33107
ms.assetid: 493c8899-3f6b-4471-8eb6-9284e8492768
ms.openlocfilehash: 76078d315b2c32a2a29aa652a65b463622afec36
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33590827"
---
# <a name="first-operand-in-a-binary-39if39-expression-must-be-nullable-or-a-reference-type"></a><span data-ttu-id="52b40-102">Le premier opérande d’un fichier binaire &#39;si&#39; expression doit être nullable ou un type référence</span><span class="sxs-lookup"><span data-stu-id="52b40-102">First operand in a binary &#39;If&#39; expression must be nullable or a reference type</span></span>
<span data-ttu-id="52b40-103">Un `If` expression peut prendre deux ou trois arguments.</span><span class="sxs-lookup"><span data-stu-id="52b40-103">An `If` expression can take either two or three arguments.</span></span> <span data-ttu-id="52b40-104">Lorsque vous envoyez uniquement deux arguments, le premier argument doit être un type référence ou un type nullable.</span><span class="sxs-lookup"><span data-stu-id="52b40-104">When you send only two arguments, the first argument must be a reference type or a nullable type.</span></span> <span data-ttu-id="52b40-105">Si le premier argument évalue à une valeur autre que `Nothing`, sa valeur est retournée.</span><span class="sxs-lookup"><span data-stu-id="52b40-105">If the first argument evaluates to anything other than `Nothing`, its value is returned.</span></span> <span data-ttu-id="52b40-106">Si le premier argument prend la valeur `Nothing`, le deuxième argument est évalué et retourné.</span><span class="sxs-lookup"><span data-stu-id="52b40-106">If the first argument evaluates to `Nothing`, the second argument is evaluated and returned.</span></span>  
  
 <span data-ttu-id="52b40-107">Par exemple, le code suivant contient deux `If` expressions, une avec trois arguments et l’autre avec deux arguments.</span><span class="sxs-lookup"><span data-stu-id="52b40-107">For example, the following code contains two `If` expressions, one with three arguments and one with two arguments.</span></span> <span data-ttu-id="52b40-108">Les expressions calculer et retournent la même valeur.</span><span class="sxs-lookup"><span data-stu-id="52b40-108">The expressions calculate and return the same value.</span></span>  
  
```vb  
' firstChoice is a nullable value type.  
Dim firstChoice? As Integer = Nothing  
Dim secondChoice As Integer = 1128  
' If expression with three arguments.  
Console.WriteLine(If(firstChoice IsNot Nothing, firstChoice, secondChoice))  
' If expression with two arguments.  
Console.WriteLine(If(firstChoice, secondChoice))  
```  
  
 <span data-ttu-id="52b40-109">Les expressions suivantes provoquent cette erreur :</span><span class="sxs-lookup"><span data-stu-id="52b40-109">The following expressions cause this error:</span></span>  
  
```vb  
Dim choice1 = 4  
Dim choice2 = 5  
Dim booleanVar = True  
  
' Not valid.  
'Console.WriteLine(If(choice1 < choice2, 1))  
' Not valid.  
'Console.WriteLine(If(booleanVar, "Test returns True."))  
```  
  
 <span data-ttu-id="52b40-110">**ID d’erreur :** BC33107</span><span class="sxs-lookup"><span data-stu-id="52b40-110">**Error ID:** BC33107</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="52b40-111">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="52b40-111">To correct this error</span></span>  
  
-   <span data-ttu-id="52b40-112">Si vous ne pouvez pas modifier le code afin que le premier argument est un type nullable ou un type référence, envisagez de convertir à un argument de trois `If` expression, ou à un `If...Then...Else` instruction.</span><span class="sxs-lookup"><span data-stu-id="52b40-112">If you cannot change the code so that the first argument is a nullable type or reference type, consider converting to a three-argument `If` expression, or to an `If...Then...Else` statement.</span></span>  
  
```vb  
Console.WriteLine(If(choice1 < choice2, 1, 2))  
Console.WriteLine(If(booleanVar, "Test returns True.", "Test returns False."))  
```  
  
## <a name="see-also"></a><span data-ttu-id="52b40-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52b40-113">See Also</span></span>  
 [<span data-ttu-id="52b40-114">If (opérateur)</span><span class="sxs-lookup"><span data-stu-id="52b40-114">If Operator</span></span>](../../../visual-basic/language-reference/operators/if-operator.md)  
 [<span data-ttu-id="52b40-115">If...Then...Else (instruction)</span><span class="sxs-lookup"><span data-stu-id="52b40-115">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)  
 [<span data-ttu-id="52b40-116">Types valeur Nullable</span><span class="sxs-lookup"><span data-stu-id="52b40-116">Nullable Value Types</span></span>](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
