---
title: Conversions de pointeur (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], conversions
ms.assetid: f0e87502-477a-4ede-a31f-7a3e262e46fb
ms.openlocfilehash: e0c3a409d76468a6e214a96e8bb326a9d906fe18
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33322690"
---
# <a name="pointer-conversions-c-programming-guide"></a><span data-ttu-id="0a081-102">Conversions de pointeur (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="0a081-102">Pointer Conversions (C# Programming Guide)</span></span>
<span data-ttu-id="0a081-103">Le tableau suivant présente les conversions de pointeur implicites prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="0a081-103">The following table shows the predefined implicit pointer conversions.</span></span> <span data-ttu-id="0a081-104">Les conversions implicites peuvent se produire dans de nombreuses situations, comme les appels de méthode et les instructions d’assignation.</span><span class="sxs-lookup"><span data-stu-id="0a081-104">Implicit conversions might occur in many situations, including method invoking and assignment statements.</span></span>  
  
## <a name="implicit-pointer-conversions"></a><span data-ttu-id="0a081-105">Conversions de pointeur implicites</span><span class="sxs-lookup"><span data-stu-id="0a081-105">Implicit pointer conversions</span></span>  
  
|<span data-ttu-id="0a081-106">From</span><span class="sxs-lookup"><span data-stu-id="0a081-106">From</span></span>|<span data-ttu-id="0a081-107">À</span><span class="sxs-lookup"><span data-stu-id="0a081-107">To</span></span>|  
|----------|--------|  
|<span data-ttu-id="0a081-108">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="0a081-108">Any pointer type</span></span>|<span data-ttu-id="0a081-109">void\*</span><span class="sxs-lookup"><span data-stu-id="0a081-109">void\*</span></span>|  
|<span data-ttu-id="0a081-110">null</span><span class="sxs-lookup"><span data-stu-id="0a081-110">null</span></span>|<span data-ttu-id="0a081-111">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="0a081-111">Any pointer type</span></span>|  
  
 <span data-ttu-id="0a081-112">La conversion de pointeur explicite permet d’effectuer des conversions, pour lesquelles il n’existe pas de conversion implicite, à l’aide d’une expression de cast.</span><span class="sxs-lookup"><span data-stu-id="0a081-112">Explicit pointer conversion is used to perform conversions, for which there is no implicit conversion, by using a cast expression.</span></span> <span data-ttu-id="0a081-113">Le tableau suivant liste ces conversions.</span><span class="sxs-lookup"><span data-stu-id="0a081-113">The following table shows these conversions.</span></span>  
  
## <a name="explicit-pointer-conversions"></a><span data-ttu-id="0a081-114">Conversions de pointeur explicites</span><span class="sxs-lookup"><span data-stu-id="0a081-114">Explicit pointer conversions</span></span>  
  
|<span data-ttu-id="0a081-115">From</span><span class="sxs-lookup"><span data-stu-id="0a081-115">From</span></span>|<span data-ttu-id="0a081-116">À</span><span class="sxs-lookup"><span data-stu-id="0a081-116">To</span></span>|  
|----------|--------|  
|<span data-ttu-id="0a081-117">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="0a081-117">Any pointer type</span></span>|<span data-ttu-id="0a081-118">Tout autre type pointeur</span><span class="sxs-lookup"><span data-stu-id="0a081-118">Any other pointer type</span></span>|  
|<span data-ttu-id="0a081-119">sbyte, byte, short, ushort, int, uint, long ou ulong</span><span class="sxs-lookup"><span data-stu-id="0a081-119">sbyte, byte, short, ushort, int, uint, long, or ulong</span></span>|<span data-ttu-id="0a081-120">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="0a081-120">Any pointer type</span></span>|  
|<span data-ttu-id="0a081-121">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="0a081-121">Any pointer type</span></span>|<span data-ttu-id="0a081-122">sbyte, byte, short, ushort, int, uint, long ou ulong</span><span class="sxs-lookup"><span data-stu-id="0a081-122">sbyte, byte, short, ushort, int, uint, long, or ulong</span></span>|  
  
## <a name="example"></a><span data-ttu-id="0a081-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="0a081-123">Example</span></span>  
 <span data-ttu-id="0a081-124">Dans l’exemple suivant, un pointeur vers `int` est converti en pointeur vers `byte`.</span><span class="sxs-lookup"><span data-stu-id="0a081-124">In the following example, a pointer to `int` is converted to a pointer to `byte`.</span></span> <span data-ttu-id="0a081-125">Notez que le pointeur pointe vers l’octet traité le plus faible de la variable.</span><span class="sxs-lookup"><span data-stu-id="0a081-125">Notice that the pointer points to the lowest addressed byte of the variable.</span></span> <span data-ttu-id="0a081-126">Quand vous incrémentez successivement le résultat, jusqu’à la taille de `int` (4 octets), vous pouvez afficher les octets restants de la variable.</span><span class="sxs-lookup"><span data-stu-id="0a081-126">When you successively increment the result, up to the size of `int` (4 bytes), you can display the remaining bytes of the variable.</span></span>  
  
 [!code-csharp[csProgGuidePointers#3](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-conversions_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#4](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-conversions_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="0a081-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a081-127">See Also</span></span>  
 [<span data-ttu-id="0a081-128">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0a081-128">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="0a081-129">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="0a081-129">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
 [<span data-ttu-id="0a081-130">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="0a081-130">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
 [<span data-ttu-id="0a081-131">Types</span><span class="sxs-lookup"><span data-stu-id="0a081-131">Types</span></span>](../../../csharp/language-reference/keywords/types.md)  
 [<span data-ttu-id="0a081-132">unsafe</span><span class="sxs-lookup"><span data-stu-id="0a081-132">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)  
 [<span data-ttu-id="0a081-133">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="0a081-133">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)  
 [<span data-ttu-id="0a081-134">stackalloc</span><span class="sxs-lookup"><span data-stu-id="0a081-134">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
