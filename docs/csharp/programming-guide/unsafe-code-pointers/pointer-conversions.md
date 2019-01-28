---
title: Conversions de pointeur - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], conversions
ms.assetid: f0e87502-477a-4ede-a31f-7a3e262e46fb
ms.openlocfilehash: 8fa1c1442d146c9d2fbdb2fa969b2e29d7ef765d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498305"
---
# <a name="pointer-conversions-c-programming-guide"></a><span data-ttu-id="dbd40-102">Conversions de pointeur (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="dbd40-102">Pointer Conversions (C# Programming Guide)</span></span>
<span data-ttu-id="dbd40-103">Le tableau suivant présente les conversions de pointeur implicites prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="dbd40-103">The following table shows the predefined implicit pointer conversions.</span></span> <span data-ttu-id="dbd40-104">Les conversions implicites peuvent se produire dans de nombreuses situations, comme les appels de méthode et les instructions d’assignation.</span><span class="sxs-lookup"><span data-stu-id="dbd40-104">Implicit conversions might occur in many situations, including method invoking and assignment statements.</span></span>  
  
## <a name="implicit-pointer-conversions"></a><span data-ttu-id="dbd40-105">Conversions de pointeur implicites</span><span class="sxs-lookup"><span data-stu-id="dbd40-105">Implicit pointer conversions</span></span>  
  
|<span data-ttu-id="dbd40-106">From</span><span class="sxs-lookup"><span data-stu-id="dbd40-106">From</span></span>|<span data-ttu-id="dbd40-107">À</span><span class="sxs-lookup"><span data-stu-id="dbd40-107">To</span></span>|  
|----------|--------|  
|<span data-ttu-id="dbd40-108">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="dbd40-108">Any pointer type</span></span>|<span data-ttu-id="dbd40-109">void\*</span><span class="sxs-lookup"><span data-stu-id="dbd40-109">void\*</span></span>|  
|<span data-ttu-id="dbd40-110">null</span><span class="sxs-lookup"><span data-stu-id="dbd40-110">null</span></span>|<span data-ttu-id="dbd40-111">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="dbd40-111">Any pointer type</span></span>|  
  
 <span data-ttu-id="dbd40-112">La conversion de pointeur explicite permet d’effectuer des conversions, pour lesquelles il n’existe pas de conversion implicite, à l’aide d’une expression de cast.</span><span class="sxs-lookup"><span data-stu-id="dbd40-112">Explicit pointer conversion is used to perform conversions, for which there is no implicit conversion, by using a cast expression.</span></span> <span data-ttu-id="dbd40-113">Le tableau suivant liste ces conversions.</span><span class="sxs-lookup"><span data-stu-id="dbd40-113">The following table shows these conversions.</span></span>  
  
## <a name="explicit-pointer-conversions"></a><span data-ttu-id="dbd40-114">Conversions de pointeur explicites</span><span class="sxs-lookup"><span data-stu-id="dbd40-114">Explicit pointer conversions</span></span>  
  
|<span data-ttu-id="dbd40-115">From</span><span class="sxs-lookup"><span data-stu-id="dbd40-115">From</span></span>|<span data-ttu-id="dbd40-116">À</span><span class="sxs-lookup"><span data-stu-id="dbd40-116">To</span></span>|  
|----------|--------|  
|<span data-ttu-id="dbd40-117">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="dbd40-117">Any pointer type</span></span>|<span data-ttu-id="dbd40-118">Tout autre type pointeur</span><span class="sxs-lookup"><span data-stu-id="dbd40-118">Any other pointer type</span></span>|  
|<span data-ttu-id="dbd40-119">sbyte, byte, short, ushort, int, uint, long ou ulong</span><span class="sxs-lookup"><span data-stu-id="dbd40-119">sbyte, byte, short, ushort, int, uint, long, or ulong</span></span>|<span data-ttu-id="dbd40-120">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="dbd40-120">Any pointer type</span></span>|  
|<span data-ttu-id="dbd40-121">Tout type pointeur</span><span class="sxs-lookup"><span data-stu-id="dbd40-121">Any pointer type</span></span>|<span data-ttu-id="dbd40-122">sbyte, byte, short, ushort, int, uint, long ou ulong</span><span class="sxs-lookup"><span data-stu-id="dbd40-122">sbyte, byte, short, ushort, int, uint, long, or ulong</span></span>|  
  
## <a name="example"></a><span data-ttu-id="dbd40-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="dbd40-123">Example</span></span>  
 <span data-ttu-id="dbd40-124">Dans l’exemple suivant, un pointeur vers `int` est converti en pointeur vers `byte`.</span><span class="sxs-lookup"><span data-stu-id="dbd40-124">In the following example, a pointer to `int` is converted to a pointer to `byte`.</span></span> <span data-ttu-id="dbd40-125">Notez que le pointeur pointe vers l’octet traité le plus faible de la variable.</span><span class="sxs-lookup"><span data-stu-id="dbd40-125">Notice that the pointer points to the lowest addressed byte of the variable.</span></span> <span data-ttu-id="dbd40-126">Quand vous incrémentez successivement le résultat, jusqu’à la taille de `int` (4 octets), vous pouvez afficher les octets restants de la variable.</span><span class="sxs-lookup"><span data-stu-id="dbd40-126">When you successively increment the result, up to the size of `int` (4 bytes), you can display the remaining bytes of the variable.</span></span>  
  
 [!code-csharp[csProgGuidePointers#3](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-conversions_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#4](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-conversions_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="dbd40-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbd40-127">See also</span></span>

- [<span data-ttu-id="dbd40-128">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="dbd40-128">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="dbd40-129">Expressions de pointeur</span><span class="sxs-lookup"><span data-stu-id="dbd40-129">Pointer Expressions</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)
- [<span data-ttu-id="dbd40-130">Types de pointeur</span><span class="sxs-lookup"><span data-stu-id="dbd40-130">Pointer types</span></span>](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)
- [<span data-ttu-id="dbd40-131">Types</span><span class="sxs-lookup"><span data-stu-id="dbd40-131">Types</span></span>](../../../csharp/language-reference/keywords/types.md)
- [<span data-ttu-id="dbd40-132">unsafe</span><span class="sxs-lookup"><span data-stu-id="dbd40-132">unsafe</span></span>](../../../csharp/language-reference/keywords/unsafe.md)
- [<span data-ttu-id="dbd40-133">fixed, instruction</span><span class="sxs-lookup"><span data-stu-id="dbd40-133">fixed Statement</span></span>](../../../csharp/language-reference/keywords/fixed-statement.md)
- [<span data-ttu-id="dbd40-134">stackalloc</span><span class="sxs-lookup"><span data-stu-id="dbd40-134">stackalloc</span></span>](../../../csharp/language-reference/keywords/stackalloc.md)
