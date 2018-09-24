---
title: "Comment : obtenir la valeur d'une variable de pointeur (Guide de programmation C#)"
ms.date: 07/20/2015
helpviewer_keywords:
- pointer expressions [C#], indirection
- pointers [C#], indirection
- variables [C#], pointers
- pointers [C#], * operator
ms.assetid: 460a813a-4995-44c1-9de2-213b91dc7668
ms.openlocfilehash: 66f341e193a0f018adb76a40617f85266519e602
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45746586"
---
# <a name="how-to-obtain-the-value-of-a-pointer-variable-c-programming-guide"></a><span data-ttu-id="e07e9-102">Comment : obtenir la valeur d'une variable de pointeur (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="e07e9-102">How to: Obtain the Value of a Pointer Variable (C# Programming Guide)</span></span>
<span data-ttu-id="e07e9-103">Utilisez l’opérateur d’indirection de pointeur pour obtenir la variable à l’emplacement désigné par un pointeur.</span><span class="sxs-lookup"><span data-stu-id="e07e9-103">Use the pointer indirection operator to obtain the variable at the location pointed to by a pointer.</span></span> <span data-ttu-id="e07e9-104">L’expression prend la forme suivante, `p` étant un type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="e07e9-104">The expression takes the following form, where `p` is a pointer type:</span></span>  
  
```  
*p;  
```  
  
 <span data-ttu-id="e07e9-105">Vous ne pouvez pas utiliser l’opérateur d’indirection unaire sur une expression d’un autre type que le type de pointeur.</span><span class="sxs-lookup"><span data-stu-id="e07e9-105">You cannot use the unary indirection operator on an expression of any type other than the pointer type.</span></span> <span data-ttu-id="e07e9-106">Par ailleurs, vous ne pouvez pas l’appliquer à un pointeur [void](../../../csharp/language-reference/keywords/void.md).</span><span class="sxs-lookup"><span data-stu-id="e07e9-106">Also, you cannot apply it to a [void](../../../csharp/language-reference/keywords/void.md) pointer.</span></span>  
  
 <span data-ttu-id="e07e9-107">Quand vous appliquez l’opérateur d’indirection à un pointeur [null](../../../csharp/language-reference/keywords/null.md), le résultat dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="e07e9-107">When you apply the indirection operator to a [null](../../../csharp/language-reference/keywords/null.md) pointer, the result depends on the implementation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e07e9-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="e07e9-108">Example</span></span>  
 <span data-ttu-id="e07e9-109">Dans l’exemple suivant, une variable de type `char` est accessible via des pointeurs de types différents.</span><span class="sxs-lookup"><span data-stu-id="e07e9-109">In the following example, a variable of the type `char` is accessed by using pointers of different types.</span></span> <span data-ttu-id="e07e9-110">Notez que l’adresse de `theChar` peut varier d’une exécution à l’autre, car l’adresse physique allouée à une variable peut changer.</span><span class="sxs-lookup"><span data-stu-id="e07e9-110">Note that the address of `theChar` will vary from run to run, because the physical address allocated to a variable can change.</span></span>  
  
 [!code-csharp[csProgGuidePointers#5](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-obtain-the-value-of-a-pointer-variable_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#6](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-obtain-the-value-of-a-pointer-variable_2.cs)]  
  
<span data-ttu-id="e07e9-111">**Valeur de theChar = Z**
**Adresse de theChar = 12F718**
**Valeur de pChar = Z**
**Valeur de pInt = 90**</span><span class="sxs-lookup"><span data-stu-id="e07e9-111">**Value of theChar = Z**
**Address of theChar = 12F718**
**Value of pChar = Z**
**Value of pInt = 90**</span></span>

## <a name="see-also"></a><span data-ttu-id="e07e9-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e07e9-112">See Also</span></span>

- [<span data-ttu-id="e07e9-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="e07e9-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="e07e9-114">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="e07e9-114">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [<span data-ttu-id="e07e9-115">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="e07e9-115">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [<span data-ttu-id="e07e9-116">Types</span><span class="sxs-lookup"><span data-stu-id="e07e9-116">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
- [<span data-ttu-id="e07e9-117">unsafe</span><span class="sxs-lookup"><span data-stu-id="e07e9-117">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
- [<span data-ttu-id="e07e9-118">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="e07e9-118">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [<span data-ttu-id="e07e9-119">stackalloc</span><span class="sxs-lookup"><span data-stu-id="e07e9-119">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
