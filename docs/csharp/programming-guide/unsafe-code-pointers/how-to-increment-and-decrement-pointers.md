---
title: 'Comment : incrémenter et décrémenter des pointeurs (Guide de programmation C#)'
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], increment and decrement
- pointer expressions [C#], increment and decrement
ms.assetid: 1b8b9281-44ee-485a-9045-3db38a4b4b89
ms.openlocfilehash: 39cefc5dcebf1331a5e0ac0fadb8284e9041eb27
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44206469"
---
# <a name="how-to-increment-and-decrement-pointers-c-programming-guide"></a><span data-ttu-id="3ef9f-102">Comment : incrémenter et décrémenter des pointeurs (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="3ef9f-102">How to: Increment and Decrement Pointers (C# Programming Guide)</span></span>
<span data-ttu-id="3ef9f-103">Utilisez les opérateurs d’incrémentation et de décrémentation, `++` et `--`, pour changer l’emplacement du pointeur de [sizeof](../../../csharp/language-reference/keywords/sizeof.md) (`pointer-type`) pour un pointeur de type pointer-type\*.</span><span class="sxs-lookup"><span data-stu-id="3ef9f-103">Use the increment and the decrement operators, `++` and `--`, to change the pointer location by [sizeof](../../../csharp/language-reference/keywords/sizeof.md) (`pointer-type`) for a pointer of type pointer-type\*.</span></span> <span data-ttu-id="3ef9f-104">Les expressions d’incrémentation et de décrémentation prennent la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="3ef9f-104">The increment and decrement expressions take the following form:</span></span>  
  
```  
++p;  
p++;  
--p;  
p--;  
```  
  
 <span data-ttu-id="3ef9f-105">Les opérateurs d’incrémentation et de décrémentation peuvent être appliqués aux pointeurs de tout type à l’exception du type `void*`.</span><span class="sxs-lookup"><span data-stu-id="3ef9f-105">The increment and decrement operators can be applied to pointers of any type except the type `void*`.</span></span>  
  
 <span data-ttu-id="3ef9f-106">L’application de l’opérateur d’incrémentation à un pointeur de type `pointer-type` a pour effet d’ajouter [sizeof](../../../csharp/language-reference/keywords/sizeof.md) (`pointer-type`) à l’adresse contenue dans la variable pointeur.</span><span class="sxs-lookup"><span data-stu-id="3ef9f-106">The effect of applying the increment operator to a pointer of the type `pointer-type` is to add [sizeof](../../../csharp/language-reference/keywords/sizeof.md) (`pointer-type`) to the address that is contained in the pointer variable.</span></span>  
  
 <span data-ttu-id="3ef9f-107">L’application de l’opérateur de décrémentation à un pointeur de type `pointer-type` a pour effet de soustraire `sizeof` (`pointer-type`) à l’adresse contenue dans la variable pointeur.</span><span class="sxs-lookup"><span data-stu-id="3ef9f-107">The effect of applying the decrement operator to a pointer of the type `pointer-type` is to subtract `sizeof` (`pointer-type`) from the address that is contained in the pointer variable.</span></span>  
  
 <span data-ttu-id="3ef9f-108">Aucune exception n’est générée si l’opération produit un dépassement de capacité sur le domaine du pointeur, et le résultat dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="3ef9f-108">No exceptions are generated when the operation overflows the domain of the pointer, and the result depends on the implementation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3ef9f-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="3ef9f-109">Example</span></span>  
 <span data-ttu-id="3ef9f-110">Dans cet exemple, vous parcourez un tableau en incrémentant le pointeur de la taille de `int`.</span><span class="sxs-lookup"><span data-stu-id="3ef9f-110">In this example, you step through an array by incrementing the pointer by the size of `int`.</span></span> <span data-ttu-id="3ef9f-111">À chaque étape, vous affichez l’adresse et le contenu de l’élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="3ef9f-111">With each step, you display the address and the content of the array element.</span></span>  
  
 [!code-csharp[csProgGuidePointers#3](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-increment-and-decrement-pointers_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#13](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/how-to-increment-and-decrement-pointers_2.cs)]  
  
<span data-ttu-id="3ef9f-112">**Value:0 @ Address:12860272**
**Value:1 @ Address:12860276**
**Value:2 @ Address:12860280**
**Value:3 @ Address:12860284**
**Value:4 @ Address:12860288**</span><span class="sxs-lookup"><span data-stu-id="3ef9f-112">**Value:0 @ Address:12860272**
**Value:1 @ Address:12860276**
**Value:2 @ Address:12860280**
**Value:3 @ Address:12860284**
**Value:4 @ Address:12860288**</span></span>

## <a name="see-also"></a><span data-ttu-id="3ef9f-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ef9f-113">See Also</span></span>

- [<span data-ttu-id="3ef9f-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="3ef9f-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="3ef9f-115">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="3ef9f-115">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [<span data-ttu-id="3ef9f-116">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="3ef9f-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="3ef9f-117">Manipulation de pointeurs</span><span class="sxs-lookup"><span data-stu-id="3ef9f-117">Manipulating Pointers</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)  
- [<span data-ttu-id="3ef9f-118">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="3ef9f-118">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [<span data-ttu-id="3ef9f-119">Types</span><span class="sxs-lookup"><span data-stu-id="3ef9f-119">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
- [<span data-ttu-id="3ef9f-120">unsafe</span><span class="sxs-lookup"><span data-stu-id="3ef9f-120">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
- [<span data-ttu-id="3ef9f-121">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="3ef9f-121">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [<span data-ttu-id="3ef9f-122">stackalloc</span><span class="sxs-lookup"><span data-stu-id="3ef9f-122">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
