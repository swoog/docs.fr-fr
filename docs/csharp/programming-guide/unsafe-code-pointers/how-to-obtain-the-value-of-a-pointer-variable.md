---
title: 'Guide pratique : Obtenir la valeur d’une variable de pointeur – Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointer expressions [C#], indirection
- pointers [C#], indirection
- variables [C#], pointers
- pointers [C#], * operator
ms.assetid: 460a813a-4995-44c1-9de2-213b91dc7668
ms.openlocfilehash: 9a10bcc809f3ecbc9a0fa9b917940b8e030fab8f
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65635103"
---
# <a name="how-to-obtain-the-value-of-a-pointer-variable-c-programming-guide"></a><span data-ttu-id="33592-102">Guide pratique : Obtenir la valeur d’une variable de pointeur (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="33592-102">How to: obtain the value of a pointer variable (C# Programming Guide)</span></span>

<span data-ttu-id="33592-103">Utilisez l’opérateur d’indirection de pointeur pour obtenir la variable à l’emplacement désigné par un pointeur.</span><span class="sxs-lookup"><span data-stu-id="33592-103">Use the pointer indirection operator to obtain the variable at the location pointed to by a pointer.</span></span> <span data-ttu-id="33592-104">L’expression prend la forme suivante, `p` étant un type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="33592-104">The expression takes the following form, where `p` is a pointer type:</span></span>  

```csharp
*p;  
```

<span data-ttu-id="33592-105">Vous ne pouvez pas utiliser l’opérateur d’indirection unaire sur une expression d’un autre type que le type de pointeur.</span><span class="sxs-lookup"><span data-stu-id="33592-105">You cannot use the unary indirection operator on an expression of any type other than the pointer type.</span></span> <span data-ttu-id="33592-106">Par ailleurs, vous ne pouvez pas l’appliquer à un pointeur [void](../../../csharp/language-reference/keywords/void.md).</span><span class="sxs-lookup"><span data-stu-id="33592-106">Also, you cannot apply it to a [void](../../../csharp/language-reference/keywords/void.md) pointer.</span></span>  

<span data-ttu-id="33592-107">Quand vous appliquez l’opérateur d’indirection à un pointeur [null](../../../csharp/language-reference/keywords/null.md), le résultat dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="33592-107">When you apply the indirection operator to a [null](../../../csharp/language-reference/keywords/null.md) pointer, the result depends on the implementation.</span></span>  

## <a name="example"></a><span data-ttu-id="33592-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="33592-108">Example</span></span>

<span data-ttu-id="33592-109">Dans l’exemple suivant, une variable de type `char` est accessible via des pointeurs de types différents.</span><span class="sxs-lookup"><span data-stu-id="33592-109">In the following example, a variable of the type `char` is accessed by using pointers of different types.</span></span> <span data-ttu-id="33592-110">Notez que l’adresse de `theChar` peut varier d’une exécution à l’autre, car l’adresse physique allouée à une variable peut changer.</span><span class="sxs-lookup"><span data-stu-id="33592-110">Note that the address of `theChar` will vary from run to run, because the physical address allocated to a variable can change.</span></span>  

 [!code-csharp[csProgGuidePointers#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers2.cs#5)]  

 [!code-csharp[csProgGuidePointers#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuidePointers/CS/Pointers.cs#6)]  
  
<span data-ttu-id="33592-111">**Valeur de theChar = Z**</span><span class="sxs-lookup"><span data-stu-id="33592-111">**Value of theChar = Z**</span></span>  
<span data-ttu-id="33592-112">**Address of theChar = 12F718**</span><span class="sxs-lookup"><span data-stu-id="33592-112">**Address of theChar = 12F718**</span></span>  
<span data-ttu-id="33592-113">**Value of pChar = Z**</span><span class="sxs-lookup"><span data-stu-id="33592-113">**Value of pChar = Z**</span></span>  
<span data-ttu-id="33592-114">**Value of pInt = 90**</span><span class="sxs-lookup"><span data-stu-id="33592-114">**Value of pInt = 90**</span></span>  

## <a name="see-also"></a><span data-ttu-id="33592-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33592-115">See also</span></span>

- [<span data-ttu-id="33592-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="33592-116">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="33592-117">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="33592-117">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="33592-118">Types</span><span class="sxs-lookup"><span data-stu-id="33592-118">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="33592-119">unsafe</span><span class="sxs-lookup"><span data-stu-id="33592-119">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="33592-120">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="33592-120">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="33592-121">stackalloc</span><span class="sxs-lookup"><span data-stu-id="33592-121">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
