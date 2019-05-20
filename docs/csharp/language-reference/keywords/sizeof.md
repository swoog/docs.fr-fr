---
title: sizeof - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- sizeof_CSharpKeyword
- sizeof
helpviewer_keywords:
- sizeof keyword [C#]
ms.assetid: c548592c-677c-4f40-a4ce-e613f7529141
ms.openlocfilehash: 8bb6d4a37b2eea3060921937cf15a1fdd1be97b4
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65634009"
---
# <a name="sizeof-c-reference"></a><span data-ttu-id="43808-102">sizeof (référence C#)</span><span class="sxs-lookup"><span data-stu-id="43808-102">sizeof (C# Reference)</span></span>

<span data-ttu-id="43808-103">Permet d’obtenir la taille en octets d’un type non managé.</span><span class="sxs-lookup"><span data-stu-id="43808-103">Used to obtain the size in bytes for an unmanaged type.</span></span>

<span data-ttu-id="43808-104">Les types non managés incluent :</span><span class="sxs-lookup"><span data-stu-id="43808-104">Unmanaged types include:</span></span>

- <span data-ttu-id="43808-105">Les types simples répertoriés dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="43808-105">The simple types that are listed in the following table:</span></span>

   |<span data-ttu-id="43808-106">Expression</span><span class="sxs-lookup"><span data-stu-id="43808-106">Expression</span></span>|<span data-ttu-id="43808-107">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="43808-107">Constant value</span></span>|
   |----------------|--------------------|
   |`sizeof(sbyte)`|<span data-ttu-id="43808-108">1</span><span class="sxs-lookup"><span data-stu-id="43808-108">1</span></span>|
   |`sizeof(byte)`|<span data-ttu-id="43808-109">1</span><span class="sxs-lookup"><span data-stu-id="43808-109">1</span></span>|
   |`sizeof(short)`|<span data-ttu-id="43808-110">2</span><span class="sxs-lookup"><span data-stu-id="43808-110">2</span></span>|
   |`sizeof(ushort)`|<span data-ttu-id="43808-111">2</span><span class="sxs-lookup"><span data-stu-id="43808-111">2</span></span>|
   |`sizeof(int)`|<span data-ttu-id="43808-112">4</span><span class="sxs-lookup"><span data-stu-id="43808-112">4</span></span>|
   |`sizeof(uint)`|<span data-ttu-id="43808-113">4</span><span class="sxs-lookup"><span data-stu-id="43808-113">4</span></span>|
   |`sizeof(long)`|<span data-ttu-id="43808-114">8</span><span class="sxs-lookup"><span data-stu-id="43808-114">8</span></span>|
   |`sizeof(ulong)`|<span data-ttu-id="43808-115">8</span><span class="sxs-lookup"><span data-stu-id="43808-115">8</span></span>|
   |`sizeof(char)`|<span data-ttu-id="43808-116">2 (Unicode)</span><span class="sxs-lookup"><span data-stu-id="43808-116">2 (Unicode)</span></span>|
   |`sizeof(float)`|<span data-ttu-id="43808-117">4</span><span class="sxs-lookup"><span data-stu-id="43808-117">4</span></span>|
   |`sizeof(double)`|<span data-ttu-id="43808-118">8</span><span class="sxs-lookup"><span data-stu-id="43808-118">8</span></span>|
   |`sizeof(decimal)`|<span data-ttu-id="43808-119">16</span><span class="sxs-lookup"><span data-stu-id="43808-119">16</span></span>|
   |`sizeof(bool)`|<span data-ttu-id="43808-120">1</span><span class="sxs-lookup"><span data-stu-id="43808-120">1</span></span>|

- <span data-ttu-id="43808-121">Les types enum.</span><span class="sxs-lookup"><span data-stu-id="43808-121">Enum types.</span></span>

- <span data-ttu-id="43808-122">Les types pointeur.</span><span class="sxs-lookup"><span data-stu-id="43808-122">Pointer types.</span></span>

- <span data-ttu-id="43808-123">Les structs définis par l’utilisateur qui ne contiennent pas de champs d’instance ou de propriétés d’instance implémentées automatiquement qui sont des types référence ou des types construits.</span><span class="sxs-lookup"><span data-stu-id="43808-123">User-defined structs that do not contain any instance fields or auto-implemented instance properties that are reference types or constructed types.</span></span>

<span data-ttu-id="43808-124">L’exemple suivant montre comment extraire la taille d’un `int` :</span><span class="sxs-lookup"><span data-stu-id="43808-124">The following example shows how to retrieve the size of an `int`:</span></span>

```csharp
// Constant value 4:
int intSize = sizeof(int);
```

## <a name="remarks"></a><span data-ttu-id="43808-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="43808-125">Remarks</span></span>

<span data-ttu-id="43808-126">À compter de la version 2.0 de C#, il est possible d’appliquer `sizeof` à des types simples ou enum sans compiler le code dans un contexte [unsafe](unsafe.md).</span><span class="sxs-lookup"><span data-stu-id="43808-126">Starting with version 2.0 of C#, applying `sizeof` to simple or enum types no longer requires that code be compiled in an [unsafe](unsafe.md) context.</span></span>

<span data-ttu-id="43808-127">L’opérateur `sizeof` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="43808-127">The `sizeof` operator cannot be overloaded.</span></span> <span data-ttu-id="43808-128">Les valeurs retournées par l’opérateur `sizeof` sont du type `int`.</span><span class="sxs-lookup"><span data-stu-id="43808-128">The values returned by the `sizeof` operator are of type `int`.</span></span> <span data-ttu-id="43808-129">Le tableau précédent indique les valeurs constantes qui sont substituées aux expressions `sizeof` qui utilisent certains types simples comme opérandes.</span><span class="sxs-lookup"><span data-stu-id="43808-129">The previous table shows the constant values that are substituted for `sizeof` expressions that have certain simple types as operands.</span></span>

<span data-ttu-id="43808-130">Pour tous les autres types, y compris les structs, l’opérateur `sizeof` peut être utilisé uniquement dans les blocs de code unsafe.</span><span class="sxs-lookup"><span data-stu-id="43808-130">For all other types, including structs, the `sizeof` operator can be used only in unsafe code blocks.</span></span> <span data-ttu-id="43808-131">Bien que vous puissiez utiliser la méthode <xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType>, la valeur retournée par cette méthode n’est pas toujours identique à celle retournée par `sizeof`.</span><span class="sxs-lookup"><span data-stu-id="43808-131">Although you can use the <xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> method, the value returned by this method is not always the same as the value returned by `sizeof`.</span></span> <span data-ttu-id="43808-132"><xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> retourne la taille après que le type a été marshalé, alors que `sizeof` retourne la taille telle qu’elle a été allouée par le Common Language Runtime, dont la marge intérieure.</span><span class="sxs-lookup"><span data-stu-id="43808-132"><xref:System.Runtime.InteropServices.Marshal.SizeOf%2A?displayProperty=nameWithType> returns the size after the type has been marshaled, whereas `sizeof` returns the size as it has been allocated by the common language runtime, including any padding.</span></span>

## <a name="example"></a><span data-ttu-id="43808-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="43808-133">Example</span></span>

[!code-csharp[csrefKeywordsOperator#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#11)]

## <a name="c-language-specification"></a><span data-ttu-id="43808-134">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="43808-134">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="43808-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43808-135">See also</span></span>

- [<span data-ttu-id="43808-136">Référence C#</span><span class="sxs-lookup"><span data-stu-id="43808-136">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="43808-137">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="43808-137">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="43808-138">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="43808-138">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="43808-139">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="43808-139">Operator Keywords</span></span>](operator-keywords.md)
- [<span data-ttu-id="43808-140">enum</span><span class="sxs-lookup"><span data-stu-id="43808-140">enum</span></span>](enum.md)
- [<span data-ttu-id="43808-141">Pointeurs et code unsafe</span><span class="sxs-lookup"><span data-stu-id="43808-141">Unsafe Code and Pointers</span></span>](../../programming-guide/unsafe-code-pointers/index.md)
- [<span data-ttu-id="43808-142">Structs</span><span class="sxs-lookup"><span data-stu-id="43808-142">Structs</span></span>](../../programming-guide/classes-and-structs/structs.md)
- [<span data-ttu-id="43808-143">Constantes</span><span class="sxs-lookup"><span data-stu-id="43808-143">Constants</span></span>](../../programming-guide/classes-and-structs/constants.md)
